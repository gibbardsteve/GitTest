# Git Workflow

## Clone Repository

You can find the URL associated with the repository in GitHub

### Clone to current directory

```bash
git clone https://github.com/gibbardsteve/git-notes.wiki.git
```

### Clone to specified directory

```bash
https://github.com/gibbardsteve/git-notes.wiki.git <directory>
```

## Branches

### Create Branch

```bash
git checkout -b my-new-branch
```

### List Branches

```bash
git branch
```

### Switch Branches

```bash
git switch main
```

### Delete Branch

To only delete branch if it is merged:

```bash
git branch -d my-new-branch
```

To delete branch regardless of if it is merged:

```bash
git branch -D my-new-branch
```

## Workflow

### Check Status of Repo

To determine which files have been changed, deleted, staged for commit or are untracked:

```bash
git status

On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
    modified:   Home.md

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    deleted:    Basic-Workflow.md
    deleted:    Git-Notes.md
    deleted:    Git-Setup.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
    git/

```

### Stage Files for Commit

To stage all files locally ready for commit:

```bash
git add .
```

To stage a single file ready for commit:

```bash
git add <filename>
```