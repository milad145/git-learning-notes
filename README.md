# git-learning-notes
some notes for git learners


# Git Commands

1. **Initialize a Git Project:**

   To start tracking a project with Git, use the following command:
   ```
   git init
   ```

2. **Check the Status:**

   To see the status of your project and its files, use:
   ```
   git status
   ```

3. **Add Files to the Staging Area:**

   Add files to the staging area before committing. You can do this in several ways:

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

   To unstage a file, use the following command:
   ```
   git reset 'filename'
   ```

7. **Restore a File to Its Previous State:**

   If you want to replace the file with the version from the last commit, use:
   ```
   git checkout -- 'filename'
   ```

Remember to use these commands as needed in your Git projects. It's important to maintain a clean and organized version control process for effective collaboration and project management.
