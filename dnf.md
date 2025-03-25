# Update
- command to check for updates:\
  `dnf check-update`
- command to update all packages and their dependencies:\
  `dnf upgrade`
- command to update a single package:\
  `dnf upgrade <package_name>`

# List
- command to list the latest versions of all available packages, including architectures, version numbers, and the repository they were installed from (The @ sign in front of a repository indicates that the package in this line is currently installed):\
  `dnf list --all`
- command to list only installed packages:\
  `dnf list --installed`
- command to list all available packages:\
  `dnf list --available`
- command to list packages for which newer versions are available:\
  `dnf list --upgrade`

# Install
- command to install packages from the repositories:\
  `dnf install <package_name_1> <package_name_2> ...`

# Remove
- command to remove installed packages:\
  `dnf remove <package_name_1> <package_name_2> ...`

# List transactions - package management history
- command to display a list of all the latest DNF transactions:\
  `dnf history`
- command to display a list of all the latest operations for a selected package:\
  `dnf history list <package_name>`
- command to display details of a particular transaction:\
  `dnf history info <transaction_id>`

# Revert DNF transactions
- command to revert the transaction:\
  `dnf history undo <transaction_id>`
- command to revert all DNF transactions performed between a specified transaction and the last transaction:\
  `dnf history rollback <transaction_id>`


