
| Stream / Type   | Abbreviation | File Descriptor | Default                                          |
|-----------------| -------------|-----------------|------------------------------------------------- |
| Standard Input  | stdin        | 0               | Accepts input (usaully from the keyboard)        |
| Standard Output | stdout       | 1               | Outputs data (usually to the terminal)           |
| Standard Error	 | stderr       | 2               | Outputs error messages (usually to the terminal) |

**Output Redirection:**

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
