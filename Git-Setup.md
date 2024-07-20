## Check config
```bash
git config --list
```
## Set user name and email globally
Global scope applies to the user logged in to the machine
```bash
git config --global user.name "Your Global Name"
git config --global user.email "your@email.com"
```
## Set user name and email locally to a repository
This is useful when you want a specific setup for a repo (e.g working on a personal project v work project)

You will usually find local config in the repository under _.git/config_
```bash
git config --local user.name "Your Local Name"
git config --local user.email "your-local@email.com"
```