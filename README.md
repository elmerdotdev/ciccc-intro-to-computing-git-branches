# Exercise - Git Branching

![image](https://github.com/elmerdotdev/a-0524-git-branch-exercise/assets/13399450/1ab4c232-6aeb-45b7-9346-7136509a83f0)

## **Objective:**

Learn to create, switch between, merge, and manage conflicts in Git branches.

## **Setup:**

1. **Clone the assignment:**
   - Copy the git assignment url. Example `https://github.com/username/assignmenturl.git`
   - On your computer, run `git clone https://github.com/username/assignmenturl.git` and open the directory in VS Code.

## **Tasks:**

1. **Create and Switch to a New Branch:**
   - Create a new branch in your local computer named `feature-add-about`:

     ```bash
     git branch feature-add-about
     ```

   - Switch to this branch:

     ```bash
     git switch feature-add-about
     ```

2. **Add a New File:**
   - In the `feature-add-about` branch, create a file called `ABOUT.txt`.
   - Add some content to `ABOUT.txt`, such as "This file contains information about the project."
   - Add and commit the changes:

     ```bash
     git add ABOUT.txt
     git commit -m "Add ABOUT.txt with project information"
     ```

3. **Merge Branch:**
   - Switch back to the main branch using:

     ```bash
     git switch main
     ```

   - Merge the `feature-add-about` branch into main:

     ```bash
     git merge feature-add-about
     ```

   - If there are no conflicts, finalize the merge. If there are conflicts, resolve them as instructed by Git.

4. **Handle Conflicts:**
   - For more practice, create another branch called `feature-update-about` and switch to it.
   - Make changes to `ABOUT.txt` in this new branch and git add and commit the changes.
   - Switch back to main and make different changes to `ABOUT.txt` and git add and commit the changes.
   - Try to merge `feature-update-about` into main and handle the merge conflict that arises.

5. **Push your changes:**
   - The changes you have made on the main branch are still on your local computer so we need to push it to GitHub.
   - Push your changes by running:

     ```bash
     git add .
     git commit -m "Finished exercise"
     git push
     ```

6. **Pushing your local branches to remote**
   - Although `feature-add-about` and `feature-update-about` branches exist, they only exist on your local computer and not on GitHub.
   - If you wish to have them on your remote repository as well, switch to the `feature-add-about` branch and run this command which will link the local and remote branches:

     ```bash
     git push -u origin local-branch-name
     Example: git push -u origin feature-add-about
     ```

   - Git will automatically create a branch called `feature-add-about` in GitHub.
   - Do the same for `feature-update-about`.
