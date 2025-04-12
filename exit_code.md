Common exit status codes:

| Exit Code   | Description                                                             |
| ----------- | ----------------------------------------------------------------------- |
| 0           | Success (no errors)                                                     |
| 1           | General error (catch-all for failure)                                   |
| 2           | Misuse of shell builtins - such as invalid options or missing arguments |
| 126         | Command found but not executable                                        |
| 127         | Command not found                                                       |

The exit status of the last command is available in the special parameter `$?`.

To print the exist status of the last command, use `echo $?`:

- Exit code = 0
  ```
  [hungtx@linux ~]$ uname
  Linux
  [hungtx@linux ~]$ echo $?
  0
  [hungtx@linux ~]$
  ```
- Exit code = 1
  ```
  [hungtx@linux ~]$ uname -w
  uname: invalid option -- 'w'
  Try 'uname --help' for more information.
  [hungtx@linux ~]$ echo $?
  1
  [hungtx@linux ~]$
  ```
- Exit code = 2
  ```
  [hungtx@linux ~]$ ls hungtx
  ls: cannot access 'hungtx': No such file or directory
  [hungtx@linux ~]$ echo $?
  2
  [hungtx@linux ~]$
  ```
- Exit code = 126
  ```
  hungtx@linux bash_scripts]$ ls -l testcode_126.sh 
  -rw-r--r--. 1 hungtx hungtx 25 Apr 12 19:30 testcode_126.sh
  [hungtx@linux bash_scripts]$ 
  [hungtx@linux bash_scripts]$ ./testcode_126.sh
  bash: ./testcode_126.sh: Permission denied
  [hungtx@linux bash_scripts]$ echo $?
  126
  [hungtx@linux bash_scripts]$
  ```

- Exit code = 127
  ```
  [hungtx@linux ~]$ unaming
  bash: unaming: command not found...
  [hungtx@linux ~]$ echo $?
  127
  [hungtx@linux ~]$
  ```

