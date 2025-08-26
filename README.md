# Essential git commands for everyone

Here is a list of important Git commands, broken down by a common workflow. This is a great set of commands for any new engineer to master.
This covers the most essential commands for a new engineer. The commands listed here follow the core Git workflow: `clone` \> `add` \> `commit` \> `pull` \> `push`.

-----
### 1\. Getting Started

These commands are used to create a new Git repository or to get a copy of an existing one.

  * `git init`
      * **What it does:** Initializes a new, empty Git repository in the current directory. This is the first step for a brand new project.
      * **Example:** You have a new project folder called `my-app`. Navigate into it and run:
        ```
        git init
        ```
  * `git clone <repository_url>`
      * **What it does:** Creates a copy of an existing Git repository from a remote location (like GitHub, GitLab, or Bitbucket) and puts it in a new folder on your computer.
      * **Example:** To get a copy of a team project from GitHub:
        ```
        git clone https://github.com/your-team/project-name.git
        ```

-----
### 2\. Making and Saving Changes

Once you're in a Git repository, these are the commands you'll use most often to save your work.

  * `git status`
      * **What it does:** Shows you the current state of your repository. It tells you which files have been modified, which are staged for a commit, and if your branch is ahead or behind the remote branch.
      * **Example:** To see what's changed since your last commit:
        ```
        git status
        ```
  * `git add <file_name>`
      * **What it does:** Moves changes from your working directory to the "staging area." Staging is a way of preparing a set of changes for the next commit.
      * **Example:** To stage a single file:
        ```
        git add new-feature.js
        ```
      * **Pro Tip:** Use `git add .` to stage all new and modified files in the current directory.
  * `git commit -m "Your commit message"`
      * **What it does:** Takes the changes from the staging area and permanently saves them as a "commit" (a snapshot of your project). The `-m` flag lets you add a short, descriptive message.
      * **Example:** To commit your staged changes:
        ```
        git commit -m "Add user authentication feature"
        ```

-----
### 3\. Working with Branches

Branches are essential for collaboration. They allow you to work on new features or bug fixes without affecting the main project code.

  * `git branch`
      * **What it does:** Lists all branches in your repository. It also shows you which branch you are currently on.
      * **Example:** To see your branches:
        ```
        git branch
        ```
  * `git branch <new_branch_name>`
      * **What it does:** Creates a new branch.
      * **Example:** To create a branch for a new feature:
        ```
        git branch user-profile-page
        ```
  * `git checkout <branch_name>`
      * **What it does:** Switches you to a different branch. You have to be on a branch to work on it.
      * **Example:** To start working on your new branch:
        ```
        git checkout user-profile-page
        ```
      * **Note:** In newer versions of Git, the command `git switch` is the preferred way to switch branches.
  * `git switch <branch_name>`
      * **What it does:** Switches to a different branch. This is a more modern and safer alternative to `git checkout` for switching branches.
      * **Example:**
        ```
        git switch user-profile-page
        ```
  * `git merge <branch_name>`
      * **What it does:** Combines the changes from a specified branch into your current branch.
      * **Example:** After finishing your feature on `user-profile-page`, you switch back to your `main` branch and merge your changes:
        ```
        git switch main
        git merge user-profile-page
        ```

-----
### 4\. Sharing and Syncing

These are the commands you'll use to communicate with the shared, remote repository.

  * `git pull`
      * **What it does:** Fetches all the changes from the remote repository and merges them into your current branch. This is how you update your local code with what your teammates have pushed.
      * **Example:** To get the latest code from the remote `main` branch:
        ```
        git pull origin main
        ```
  * `git push`
      * **What it does:** Pushes your local commits to the remote repository. This makes your changes available to your teammates.
      * **Example:** To push your changes to the `user-profile-page` branch on the remote:
        ```
        git push origin user-profile-page
        ```
      * **Pro Tip:** The first time you push a new branch, you might need to use `git push --set-upstream origin <branch_name>` or its shorter version, `git push -u origin <branch_name>`.

-----

### 5\. Viewing History
Sometimes you need to see what happened in the past.

  * `git log`
      * **What it does:** Shows a history of all the commits in the current branch. Each entry includes the commit ID, author, date, and commit message.
      * **Example:** To see the full commit history:
        ```
        git log
        ```
  * `git diff`
      * **What it does:** Shows the difference between two states in your repository, such as between your working directory and the staging area, or between two commits.
      * **Example:** To see what's changed in your files before you stage them:
        ```
        git diff
        ```

-----



