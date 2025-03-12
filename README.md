# Git Merge Conflict Practice
This project was created as an exercise to learn how to handle merge conflicts on GitHub. It has a simple HTML file where different changes were made in separate branches to simulate conflicts.

---

## Project Overview
- Learn how to create, merge, and resolve conflicts in Git.
- HTML (for simplicity in practicing merges).
- Skills Practiced: 
  - Branching and merging in Git
  - Handling merge conflicts
  - Understanding Git workflows

---

## What I Learned
- How to create and switch between Git branches  
- How to merge branches and resolve conflicts  
- How Git handles conflicting changes  
- How to use GitHub’s interface and CLI for merging  

---

## Project Structure
```
/Git-Merge-Conflict-Practice
│── hello2.html # Simple HTML file used for testing merges
│── README.md # This README file
```

## How to Simulate a Merge Conflict

Follow these steps to recreate a merge conflict:

### 1. Clone the Repository

```bash
git clone https://github.com/StackOverflowedDev/Git-Merge-Conflict-Practice.git
cd Git-Merge-Conflict-Practice
```
### 2. Create and Switch to a New Branch
```bash
git checkout -b feature-branch
```

### 3. Modify the HTML File
Open hello2.html
Add some text inside the <body> section
Save the file

### 4. Commit the Changes
```bash
git add .
git commit -m "Add Descriptive Info on Change Here"
```

### 5. Switch Back to main and Make Another Change
```bash
git checkout main
```
Edit hello2.html again, but differently than in feature-branch.
Save the file, then commit the changes:

```bash
git add .
git commit -m "Add Descriptive Info on Change Here"
```
### 6. Merge the Feature Branch (Causing a Conflict)

```bash
git merge feature-branch
```
### 7. Resolve the Merge Conflict
When Git detects a merge conflict, it will mark the conflicting code in hello2.html like this:

```bash
<<<<<<< HEAD
(Changes from main branch)
=======
(Changes from feature-branch)
>>>>>>> feature-branch
```

To resolve the conflict:

Open hello2.html and manually edit the file
Keep the correct version and remove the Git conflict markers (<<<<<<<, =======, >>>>>>>)
Save the file
Mark the conflict as resolved by running:

```bash
git add .
git commit -m "Resolved merge conflict"
``` 
Done! Your conflict is resolved!
