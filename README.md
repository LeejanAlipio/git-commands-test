# Everything about Git
A comprehensive updated crash course of Git for common everyday work.

## Setting Up and Initiating Git
Commands to set up your environment before working on a project.

- `git config` - Sets up your information for your commits.
  ```Bash
  git config --global user.name "Lee"
  git config --global user.email "gg@gmail.com"
  ```

- `git init` - Initialize a new git repository in your current folder/directory. Creates a hidden .git that tracks your project's progress/history.


- `git clone <SSH or HTTPS>` - Downloads repo from a remove server to your local machine.
  ```Bash
  git clone git@github.com:LeejanAlipio/git-commands-test.git
  ```

## Saving Changes
Commands to saving your files and its history

- `git status` - Checks the status if any changes have been made. 

- `git add <file>` - Allows you to add the file you want to the staging area. "Think of the staging area as a “waiting room” for your changes until you commit them."
  ```Bash
  git add README.md
  git add . # Stages everything
  ```

- `git commit -m <"A description">` - Commits the files in the staging area and saves it into your local repository history. Always add a description to the commit you make.

- `git log` - Allows you to see the changes and who changed it in chronological order.
  ```Bash
  git log --oneline # Shows a single line history of every commit
  ```

## Branching and Merging
Let's you test and improve your codebase without touching your original code.

- `git branch` - Lists all of your repository's branches.
  ```Bash
  git branch new-feature # Creates another branch
  ```

- `git checkout/switch` - Switches to another branch.
  ```Bash
  git switch new-feature
  git checkout -b new-feature # Creates a branch and switches to it immediately
  ```

- `git merge` - Implements the new feature to the main.
  ```Bash
  git checkout main # Always go back to the main branch
  git merge new-feature
  ```

## Sharing and Updating
Commands that lets you share your progress with others and update it whenever you make changes.

- `git remote add origin <github link of your repo>` - Allows you to add your local repository to a remote server

- `git fetch` - Downloads new data from the remote/online repository without changing/updating any file in your current workspace. Acts as a read-only so you can review what has changed.

- `git pull` - Download new data and updates your workspace. Combination of `git fetch` and `git merge`.
  ```Bash
  git pull origin <branch>
  ```

- `git push` - Pushes your changes in your local repository to the remote server(GitHub).
  ```Bash
  git push origin <branch>
  ```

## Reverting Changes
Going back to a previous version of your project when you made a mistake.

- `git restore <file>` - Discards uncommitted changes to a file and restores the last committed version.

- `git reset` - Restores project history to a previous commit. Must be used extremely carefully.
  ```Bash
  git reset --soft <commit-hash> # Undo the last commit and move changes back to staging
  git reset --mixed <commit-hash> # Undo the last commit and keep changes unstaged
  git reset --hard <commit-hash> # Completely remove changes and reset the repository to that commit
  ```