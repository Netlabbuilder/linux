# The command prompt symbol ($ or #) indicates the type of user currently logged in:
# $ (Dollar Sign)
Used for a regular user (non-root).
# # (Hash or Pound Sign)
Used for the root user.
# To view the definition of your command prompt, use the command: echo $PS1

The [\u \h \W]\$] parts all have special meanings.
The \u returns the username of the current user
The \h returns hostname, \W returns working directory
The \$ is the user prompt $, which is #, for the root user.
