# Git & GitHub Workshop 🚀

Welcome to the Git & GitHub Workshop! This repository is designed to help beginners learn essential Git commands and GitHub workflows through hands-on practice.

## Workshop Overview

This workshop will teach you:
- Basic Git setup and configuration
- Creating and managing branches
- Making commits and tracking changes
- Working with files in Git
- Merging branches and resolving conflicts
- Collaborating with remote repositories

## Prerequisites

Before starting, make sure you have:
- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- A GitHub account ([Sign up for GitHub](https://github.com/join))
- A text editor (VS Code, Sublime Text, or any editor you prefer)

## Getting Started

### Step 1: Fork and Clone This Repository

1. **Fork this repository**: Click the "Fork" button at the top right of this page
2. **Clone your fork**: Replace `YOUR_USERNAME` with your GitHub username
   ```bash
   git clone https://github.com/YOUR_USERNAME/Github-Workshop.git
   cd Github-Workshop
   ```

### Step 2: Configure Git (First Time Setup)

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Workshop Exercises

### Exercise 1: Basic Git Commands 🌱

**Goal**: Learn basic Git commands and create your first commit

1. **Check repository status**:
   ```bash
   git status
   ```

2. **Create a new file with your information**:
   ```bash
   echo -e "Name: Your Name  \nFavorite Programming Language: Your Language" > student-info.md
   ```

3. **Stage and commit your changes**:
   ```bash
   git add student-info.txt
   git commit -m "Add my student information"
   ```

4. **View commit history**:
   ```bash
   git log --oneline
   ```

### Exercise 2: Working with Branches 🌿

**Goal**: Create and work with different branches

1. **Create and switch to a new branch**:
   ```bash
   git checkout -b <name>/my-project
   ```

2. **Create a simple project file**:
   ```bash
   mkdir my-project
   echo -e "# My First Project\n\nThis is a project I'm working on during the Github workshop." > my-project/README.md
   ```

3. **Commit your project**:
   ```bash
   git add my-project/
   git commit -m "Add my first project"
   ```

4. **Switch back to main branch**:
   ```bash
   git checkout main
   ```

5. **List all branches**:
   ```bash
   git branch -a
   ```

### Exercise 3: File Operations 📝

**Goal**: Practice adding, modifying, and removing files

1. **Switch to your feature branch**:
   ```bash
   git checkout <name>/my-project
   ```

2. **Add a new file to your project**:
   ```bash
   echo "print('Hello, Git Workshop!')" > my-project/hello.py
   ```

3. **Modify an existing file**:
   ```bash
   echo -e "\n## Features\n- Learning Git\n- Having fun!" >> my-project/README.md
   ```

4. **Stage all changes**:
   ```bash
   git add .
   ```

5. **Commit your changes**:
   ```bash
   git commit -m "Add hello.py and update README with features"
   ```

### Exercise 4: Merging Branches 🔀

**Goal**: Learn how to merge branches

1. **Switch to AIM branch**:
   ```bash
   git checkout -b <name>/AIM
   ```

2. **Merge your feature branch**:
   ```bash
   git merge <name>/my-project 
   ```

3. **Delete the feature branch (optional)**:
   ```bash
   git branch -d <name>/my-project
   ```

4. **View updated log**:
   ```bash
   git log --oneline --graph
   ```

### Exercise 5: Working with Remote Repositories 🌐

**Goal**: Learn to push changes to GitHub

1. **Push your changes to GitHub (if you didnt fork then ignore)**:
   ```bash
   git push origin main
   ```

2. **Create a new branch for collaboration**:
   ```bash
   git checkout -b <name>/collaboration
   ```

3. **Add a collaboration file**:
   ```bash
   echo "This file was created to practice collaboration!" > collaboration.md
   git add collaboration.md
   git commit -m "Add collaboration file"
   ```

4. **Push the new branch**:
   ```bash
   git push origin <name>/collaboration
   ```

### Exercise 6: Simulating Merge Conflicts 💥

**Goal**: Learn to resolve merge conflicts

1. **Create two conflicting branches**:
   ```bash
   git checkout main
   git checkout -b branch-a
   echo "This is version A" > conflict-file.txt
   git add conflict-file.txt
   git commit -m "Add version A"
   
   git checkout main
   git checkout -b branch-b
   echo "This is version B" > conflict-file.txt
   git add conflict-file.txt
   git commit -m "Add version B"
   ```

2. **Merge and resolve conflict**:
   ```bash
   git checkout main
   git merge branch-a
   git merge branch-b
   # This will create a conflict!
   ```

3. **Resolve the conflict by editing the file**:
   - Open `conflict-file.txt` in your editor
   - Choose which version to keep or combine both
   - Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)

4. **Complete the merge**:
   ```bash
   git add conflict-file.txt
   git commit -m "Resolve merge conflict between branch-a and branch-b"
   ```

## Advanced Exercises (Optional) 🎯

### Exercise 7: Undoing Changes

Practice using:
- `git checkout -- filename` (undo unstaged changes)
- `git reset HEAD filename` (unstage files)
- `git revert commit-hash` (revert a commit)

### Exercise 8: Interactive Rebase

Learn to clean up commit history:
```bash
git rebase -i HEAD~3
```

## Useful Git Commands Reference 📖

| Command | Description |
|---------|-------------|
| `git status` | Check the status of your working directory |
| `git add <file>` | Stage a file for commit |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit staged changes |
| `git push origin <branch>` | Push branch to remote |
| `git pull origin <branch>` | Pull changes from remote |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <branch>` | Create and switch to a new branch |
| `git merge <branch>` | Merge a branch into current branch |
| `git branch` | List local branches |
| `git branch -a` | List all branches (local and remote) |
| `git log --oneline` | View commit history |
| `git diff` | View unstaged changes |

## Workshop Completion Checklist ✅

After completing all exercises, you should have:

- [ ] Configured Git with your name and email
- [ ] Created and committed a student info file
- [ ] Created and worked with feature branches
- [ ] Added, modified, and committed files
- [ ] Merged branches successfully
- [ ] Pushed changes to your GitHub repository
- [ ] Resolved at least one merge conflict
- [ ] Created a simple project structure

## Getting Help 🆘

If you get stuck:

1. Check the Git documentation: `git help <command>`
2. Ask your instructor or classmates
3. Search for solutions online (Stack Overflow is your friend!)
4. Use `git status` to understand your current situation

## Next Steps 🚀

After completing this workshop:

1. Explore more Git features like stashing, rebasing, and tagging
2. Learn about GitHub features like Issues, Pull Requests, and Actions
3. Practice collaborating on real projects
4. Contribute to open-source projects

## Resources 📚

- [Git Official Documentation](https://git-scm.com/doc)
- [Interactive Git Tutorial](https://learngitbranching.js.org/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

Happy learning! 🎉 Remember, the best way to learn Git is by practicing regularly. 
