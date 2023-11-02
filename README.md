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

15. **Clone a Repository:**

   To copy an existing repository from a remote location (like GitHub) to your local machine, use:
   ```
git clone <repository_URL>
   ```

16. **Push Changes to Remote:**

   To send committed changes from your local repository to the remote server, use:
   ```
git push
   ```

17. **Add Remote Repository:**

   To add a remote address to your current project on your local machine, use:
   ```
git remote add origin <remote_URL>
   ```

18. **Change Remote URL:**

   To replace the current remote URL with a new one, use:
   ```
git remote set-url origin <new_remote_URL>
   ```

19. **Pull Changes from Remote:**

   To fetch and merge changes from the remote server into your local branch, use:
   ```
git pull origin main
   ```

20. **Set Upstream Branch:**

   To track a remote branch, use:
   ```
git branch --set-upstream-to=origin/main main
   ```

21. **Push with Upstream:**

   To push the current branch and set the remote as the upstream branch, use:
   ```
git push --set-upstream origin <local-branch>
   ```

22. **Tagging:**

    Tags are used to mark specific points in the commit history. 
    **also you can make versions for your application**

    - Show all tags:
      ```
      git tag
      ```

    - Create a tag for the last commit:
      ```
      git tag -a <tag-name or version-number> -m "Your message"
      ```

    - Create a tag for a specific commit:
      ```
      git tag -a <version-number> <commit-id> -m "Your message"
      ```

    - Search between tags (e.g., tags starting with 'v0'):
      ```
      git tag -l 'v0*'
      ```

    - Push a specific tag to the remote:
      ```
      git push origin <tag-name>
      ```

    - Push all tags to the remote:
      ```
      git push origin --tags
      ```

23. **Switch to a Tag:**

    To switch to a specific tag, use:
    ```
    git switch <tag-name>
    ```

Remember to use these commands as needed in your Git projects. It's important to maintain a clean and organized version
control process for effective collaboration and project management.
