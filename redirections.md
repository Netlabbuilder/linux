
**Standard Streams**

| Stream / Type   | Abbreviation | File Descriptor | Default                                          |
|-----------------| -------------|-----------------|------------------------------------------------- |
| Standard Input  | stdin        | 0               | Accepts input (usaully from the keyboard)        |
| Standard Output | stdout       | 1               | Outputs data (usually to the terminal)           |
| Standard Error	| stderr       | 2               | Outputs error messages (usually to the terminal) |

**Output Redirection**

- Redirect stdout to a file with `>`, here is `output.txt` file as an example, it also overwrites output.txt with the output:

  ```
  [hungtx@linux ~]$ ls > output.txt
  ```
- Append stdout to a file with `>>`:

  ```
  [hungtx@linux ~]$ ls >> output.txt
  ```

- Redirect stderr to a file with `2>`, here is `output.txt` file as an example:

  ```
  [hungtx@linux ~]$ uname -w 2> error.txt
  ```

- Redirect both stdout and stderr to the same file with `>` and `2>&1`:

  ```
  [hungtx@linux ~]$ ls -l output.txt non_file.txt > error.txt 2>&1
  [hungtx@linux ~]$ cat error.txt 
  ls: cannot access 'non_file.txt': No such file or directory
  -rw-r--r--. 1 hungtx hungtx 212 Apr 14 18:15 output.txt
  [hungtx@linux ~]$
  ```
  or with `&>`
  ```
  [hungtx@linux ~]$ ls -l output.txt non_file.txt &> error.txt 
  [hungtx@linux ~]$ cat error.txt 
  ls: cannot access 'non_file.txt': No such file or directory
  -rw-r--r--. 1 hungtx hungtx 212 Apr 14 18:15 output.txt
  [hungtx@linux ~]$
  ```

**Input Redirection**

- Redirect a file as input instead of typing with `<`:
  ```
  [hungtx@linux ~]$ cat data.txt 
  009
  001
  007
  [hungtx@linux ~]$ sort < data.txt 
  001
  007
  009
  [hungtx@linux ~]$ sort -r < data.txt 
  009
  007
  001
  [hungtx@linux ~]$
  ```
- `xargs` takes input (usually from stdin) and turns it into command-line arguments
  ```
  [hungtx@linux ~]$ ls -l data*.txt
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data1.txt
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data2.txt
  [hungtx@linux ~]$ 
  [hungtx@linux ~]$ cat demo.txt 
  data1.txt
  data2.txt
  [hungtx@linux ~]$
  ```
  - Use `xargs` this way:
  ```  
  [hungtx@linux ~]$ xargs ls -l < demo.txt
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data1.txt
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data2.txt
  [hungtx@linux ~]$
  ```
  - Or use `xargs` this way:
  ```
  [hungtx@linux ~]$ cat demo.txt | xargs ls -l
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data1.txt
  -rw-r--r--. 1 hungtx hungtx 0 Apr 14 21:21 data2.txt
  [hungtx@linux ~]$
  ```
