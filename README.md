| **Action**                              | **Command**                                                                                         | **Description**                                                                                   | **Example with Explanation**                                                                                                                                                           |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Set user identity**                   | `git config --global user.email "you@example.com"`<br>`git config --global user.name "Your Name"`    | Sets your global identity for all Git repositories. Use without `--global` for per-repo identity. |  `git config --global user.email "user@gmail.com"` <br> This sets the email "user@gmail.com" as your identity for all repositories globally.            |
| **Initialize a new repository**         | `git init <repository>`                                                                             | Creates a new local repository in the specified directory.                                     |  `git init my-project`<br> Initializes a Git repository inside the folder `my-project`, enabling version control for the folder.                           |
| **Clone a repository**                  | `git clone <URL>`<br>`git clone username@host:/path/to/repository`                                  | Copies an existing repository locally.                                                        |  `git clone https://github.com/User/repo.git`<br> Clones the remote GitHub repository to your local machine for editing and tracking changes.               |
| **Add & commit changes**                | `git add <file>`<br>`git add *`<br>`git commit -m "message"`                                        | Adds files to staging and commits them to the local repository.                                |  `git add index.html`<br>`git commit -m "Add homepage layout"`<br> Stages `index.html` and saves the changes to the local repository with a description.    |
| **Push changes to remote**              | `git push origin master`                                                                            | Pushes local commits to the remote branch.                                                    |  `git push origin main`<br> Sends all new commits on the `main` branch to the remote GitHub repository.                                                    |
| **Set remote server**                   | `git remote add origin <server>`                                                                    | Links a local repository to a remote server.                                                  |  `git remote add origin https://github.com/User/repo.git`<br> Connects the local repository to the remote URL for pushing and pulling changes.              |
| **Create a new branch**                 | `git checkout -b <branch>`                                                                          | Creates and switches to a new branch.                                                         |  `git checkout -b feature/new-layout`<br> Creates a new branch called `feature/new-layout` and switches to it for working on specific changes.             |
| **Switch branches**                     | `git checkout master`                                                                               | Switches back to the master (or main) branch.                                                 |  `git checkout main`<br> Moves your working directory to the `main` branch, so changes apply to the main line of development.                              |
| **Delete a branch**                     | `git branch -d <branch>`                                                                            | Deletes a local branch.                                                                       |  `git branch -d feature/new-layout`<br> Deletes the branch `feature/new-layout` locally after ensuring all changes are merged or no longer needed.         |
| **Push branch to remote**               | `git push origin <branch>`                                                                          | Makes the branch available to others on the remote repository.                                |  `git push origin feature/new-layout`<br> Pushes the branch `feature/new-layout` to the remote repository for collaboration.                               |
| **Update repository**                   | `git pull`                                                                                          | Fetches and merges the latest changes from the remote repository.                             |  `git pull origin main`<br> Updates your local `main` branch with the latest changes from the remote repository.                                           |
| **Merge branches**                      | `git merge <branch>`                                                                                | Combines another branch into the current branch.                                              |  `git merge feature/new-layout`<br> Merges the changes from `feature/new-layout` into your current branch (e.g., `main`).                                  |
| **Preview changes before merging**      | `git diff <source_branch> <target_branch>`                                                          | Shows the differences between two branches before merging.                                    |  `git diff feature/new-layout main`<br> Displays the changes in `feature/new-layout` that are not yet in `main`, so you can review them.                  |
| **Tagging a commit**                    | `git tag 1.0.0 <commit-hash>`                                                                       | Creates a new tag for the specified commit.                                                   |  `git tag 1.0.0 abc123def`<br> Tags the commit `abc123def` with the version `1.0.0` to mark a specific release point.                                       |
| **View commit history**                 | `git log`                                                                                          | Shows the commit history of the repository.                                                  |  `git log`<br> Lists all commits in the current branch, including details like author, date, and commit message.                                           |
| **Filtered commit log**                 | `git log --author=bob`<br>`git log --pretty=oneline`<br>`git log --graph --oneline --decorate --all` | Various log options: filter by author, one-line format, or a graphical tree.                  |  `git log --graph --oneline --decorate`<br> Displays a graphical history of commits with branches and tags annotated.                                      |
| **Show file changes in commits**        | `git log --name-status`                                                                             | Displays which files were changed in each commit.                                             |  `git log --name-status`<br> Lists commits with details on files added, modified, or deleted in each commit.                                               |
| **Discard local changes**               | `git checkout -- <filename>`                                                                        | Replaces local changes in a file with the last committed version.                             |  `git checkout -- style.css`<br> Discards unsaved changes in `style.css`, restoring it to the last committed version.                                      |
| **Reset local branch to remote**        | `git fetch origin`<br>`git reset --hard origin/master`                                              | Fetches the latest changes from the remote and resets the local branch to match.             |  `git reset --hard origin/main`<br> Resets the `main` branch to match the remote branch exactly, discarding local changes.                                 |
| **Built-in Git GUI**                    | `gitk`                                                                                              | Launches a graphical interface for Git history and changes.                                   |  `gitk`<br> Opens a GUI tool to explore commit history and branches visually.                                                                              |
| **Colorful Git output**                 | `git config color.ui true`                                                                          | Enables colorful output for Git commands in the terminal.                                     |  `git config color.ui true`<br> Makes Git's output, like `git status`, easier to read with colors.                                                        |
| **Interactive staging**                 | `git add -i`                                                                                        | Opens an interactive interface for staging files.                                             |  `git add -i`<br> Allows you to interactively select files or chunks of changes to stage for a commit.                                                     |
| **Stash changes**                       | `git stash`                                                                                         | Temporarily saves uncommitted changes and reverts the working directory to a clean state.    |  `git stash`<br> Temporarily saves all local changes to a "stash" so you can switch branches without losing progress.                                     |
| **Apply stashed changes**               | `git stash apply`                                                                                   | Restores changes from the most recent stash without deleting the stash.                     |  `git stash apply`<br> Restores the changes you saved with `git stash`, allowing you to continue where you left off.                                      |
| **Delete a specific stash**             | `git stash drop <stash@{index}>`                                                                    | Removes a specific stash from the stash list.                                               |  `git stash drop stash@{0}`<br> Deletes the most recent stash (`stash@{0}`) from the list of saved changes.                                                |
