---

This file documents every step, command, and explanation for this Git learning project.

---

## Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/git-basics-devops-project.git
cd git-basics-devops-project
```
## Step 2: Initialize Git
Initializes a new Git repository in your local folder.
```bash
git init
```

## Step 3: Create Project Files
```bash
touch hello-world.txt changelog.md .gitignore README.md
```
## Step 4: First Commit
Adds your file to staging and creates the first snapshot.
```bash
echo "Hello, DevOps!" > hello-world.txt
git add hello-world.txt
git commit -m "Initial commit: add hello-world.txt"
```
## Step 5: Create a Feature Branch
Creates and switches to a new branch.
```bash
git checkout -b feature/update-message
```

## Step 6: Make Changes & Commit in Feature Branch
```bash
echo "This is a feature branch." >> hello-world.txt
git add hello-world.txt
git commit -m "Updated hello-world.txt with feature message"
```

## Step 7: Merge Feature Branch into Main
Merges changes from feature branch into main.
```bash
git checkout main
git merge feature/update-message
```
## Step 8: Simulate and Resolve Merge Conflict
1. In main:
```bash
 echo "MAIN branch edit" > hello-world.txt
git commit -am "Edited hello-world.txt in main"
```
2. In feature/update-message:
```bash
   git checkout feature/update-message
echo "FEATURE conflicting edit" > hello-world.txt
git commit -am "Conflicting edit"
```
3. Merge back into main:
```bash
git checkout main
git merge feature/update-message
```
4. Manually resolve conflict in hello-world.txt then:
```bash
git add hello-world.txt
git commit -m "Resolved merge conflict in hello-world.txt"
```

## Step 9: Revert a Commit
```bash
git log --oneline
git revert <commit_hash>
```
## Step 10: Connect to Remote Repo and Push
```bash
git remote add origin https://github.com/YOUR_USERNAME/git-basics-devops-project.git
git push -u origin main
git push origin feature/update-message
```
## Step 11: Create a Pull Request

Go to GitHub → Click “Compare & pull request” → Add description → Merge.

Project Complete!
