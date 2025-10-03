Hasiecj: I have forked the repository, how to make sure I can push my own changes tothe code and pull the latest updates from the original repository to keep it up to date?

GitHub Copilot: To ensure you can push your own changes to your forked repository and pull the latest updates from the original repository, follow these steps:

### 1. **Set Up Your Forked Repository**
   - Clone your forked repository to your local machine:
     ```zsh
     git clone https://github.com/<your-username>/udemy_agentic_ai.git
     cd udemy_agentic_ai
     ```
   - Replace `<your-username>` with your GitHub username.

### 2. **Add the Original Repository as an Upstream Remote**
   - Add the original repository as a remote named `upstream`:
     ```zsh
     git remote add upstream https://github.com/Hasiecj/udemy_agentic_ai.git
     ```
   - Verify the remotes:
     ```zsh
     git remote -v
     ```
     You should see both `origin` (your fork) and `upstream` (the original repository).

### 3. **Pull Updates from the Original Repository**
   - Fetch the latest changes from the `upstream` repository:
     ```zsh
     git fetch upstream
     ```
   - Merge the changes into your local branch:
     ```zsh
     git merge upstream/main
     ```
     Replace `main` with the default branch name of the original repository if it's different.

### 4. **Push Changes to Your Fork**
   - After making changes to your local repository, commit them:
     ```zsh
     git add .
     git commit -m "Your commit message"
     ```
   - Push the changes to your fork:
     ```zsh
     git push origin main
     ```

### 5. **Keep Your Fork Updated**
   - Regularly fetch and merge changes from the `upstream` repository to keep your fork up to date:
     ```zsh
     git fetch upstream
     git merge upstream/main
     git push origin main
     ```

### 6. **Resolve Conflicts (if any)**
   - If there are merge conflicts, Git will notify you. Open the conflicting files, resolve the conflicts, and then:
     ```zsh
     git add <file>
     git commit
     ```

By following these steps, you can maintain your fork, contribute your changes, and stay updated with the original repository. 