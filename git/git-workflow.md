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

### Stage Changes for Commit

To stage all changes locally ready for commit:

```bash
git add .
```

To stage a single file ready for commit:

```bash
git add <filename>
```

### Commit Changes

Prior to commiting check:

1. You are on the right branch:

    ```bash
    git branch

    main
    * my-new-branch
    ```

2. All of the changes you want to commit are staged:

    ```bash
    git status

    On branch my-new-branch
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
        deleted:    Basic-Workflow.md
        deleted:    Git-Notes.md
        modified:   Home.md
        new file:   git/git-notes.md
        renamed:    Git-Setup.md -> git/git-setup.md
        new file:   git/git-workflow.md
    ```

3. Commit the changes locally:

    ```bash
    git commit -m "your commit message" .
    ```

4. Push the changes to the remote repository:

    ```bash
    git push origin my-new-branch
    ```

5. Check commit history:

```bash
git log

commit d029706bcd1f01aa1a18beb89c0208f764c03294 (HEAD -> my-new-branch, origin/my-new-branch)
Author: Author Name <author.name@org.com>
Date:   Sat Jul 20 19:55:59 2024 +0100

    docs: restructure notes and add home content

```
