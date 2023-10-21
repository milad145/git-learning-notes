# git-learning-notes

some notes for git learners

# Git Commands

1. **Initialize a Git Project:**

   To start a new Git repository for your project, use the following command:
   ```
   git init
   ```

2. **Check the Status:**

   To view the current status of your project and its files, use:
   ```
   git status
   ```

3. **Add Files to the Staging Area:**

   Add files to the staging area to prepare them for commit. You have several options:

    - Add all files:
      ```
      git add -A
      ```
    - Add specific file types, e.g., all HTML files:
      ```
      git add "*.html"
      ```

    - Add specific file :
      ```
      git add "file-name"
      ```

4. **Commit Changes:**

   To save the staged changes as a new snapshot, use the `git commit` command:
   ```
   git commit -m "Your message about the changes"
   ```
    - `git commit`: Archive staged changes and add a descriptive message.
    - Always include a message with your commit.

5. **View Differences:**

   Git provides several ways to view differences:

    - See the difference between the current stage and the last commit:
      ```
      git diff HEAD
      ```

    - See the difference between the current stage and the previous stage:
      ```
      git diff --staged
      ```

6. **Reset and Exit the Staging Area:**

   To manipulate the state of your working directory, staging area, and commit history, you can use the `git reset`
   command:

    - To unstage a file, use:
      ```
      git reset 'filename'
      ```

    - To move the HEAD pointer to a specific commit and optionally modify the staging area and working directory, use:
      ```
      git reset --soft <commit>
      git reset --mixed <commit>
      git reset --hard <commit>
      ```

7. **Restore Files:**

   To manipulate the state of your working directory and staging area without affecting the commit history, you can use
   the `git restore` command:

    - To unstage a file, use:
      ```
      git restore --staged <file>
      ```

    - To restore a specific file from a previous commit to your working directory, use:
      ```
      git restore --source=<commit> <file>
      ```

    - To restore your entire working directory to match a specific commit, use:
      ```
      git restore --source=<commit> .
      ```

8. **Branches:**

   Managing branches is essential for collaboration and project organization. Here are some branch-related commands:

    - Show all branches in the project:
      ```
      git branch
      ```

    - Create a new branch for your project:
      ```
      git branch 'branch-name'
      ```

    - Delete a branch from the project:
      ```
      git branch -d 'branch-name'
      ```

9. **Checkout Branch and Files:**

    - To switch to a different branch and replace all the files in your current branch with those from 'branch-name',
      use:
      ```
      git checkout 'branch-name'
      ```
    - To replace a file with the version from the HEAD (latest commit), use:
      ```
      git checkout -- 'filename'
      ```
        - `'--'`: Refers to the HEAD (latest commit).


10. **Merge Branches:**

    To merge a branch into your current branch, use:
    ```
    git merge 'branch-name'
    ```

11. **View Commit History:**

    To see all the commit logs, use:
    ```
    git log
    ```

12. **Remove a File:**

    To remove a file from Git and your project, use:
    ```
    git rm 'file-name'
    ```

13. **Push to a Remote Repository:**

    To push all the changes from your local `master` branch to a remote repository (usually in the cloud, like GitHub or
    GitLab), use:
    ```
    git push origin master
    ```
    - `origin`: Represents the remote repository.
    - `git push -u origin master`: After using this parameter, you can use `git push` instead
      of `git push origin master`.

14. **Pull from a Remote Repository:**

    To update, retrieve, and replace the changes from the remote repository into your local `master` branch, use:
    ```
    git pull origin master
    ```

Remember to use these commands as needed in your Git projects. It's important to maintain a clean and organized version
control process for effective collaboration and project management.
