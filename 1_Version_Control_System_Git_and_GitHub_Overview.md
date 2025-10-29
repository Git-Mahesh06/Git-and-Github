## 🧩 Version Control System (Git & GitHub)

🧠 Overview

Git is a Distributed Version Control System (DVCS) used to track and manage changes in source code.
It allows multiple developers to collaborate efficiently and maintain version history.

🔹 Types of Version Control Systems
1️⃣ Centralized Version Control System (CVCS)

A single central server stores the codebase.

Developers directly commit code to this central server.

Example: SVN, Perforce

2️⃣ Distributed Version Control System (DVCS)

Every developer has a local copy of the repository.

Work can be done offline, commits are local.

Example: Git, Mercurial

✅ Advantages of DVCS

Works offline

Faster commits

Each clone is a backup

Easy branching and merging

## 🧱 Git Architecture

Git operates through four main areas of a project:

[ Working Directory ]
│
▼
git add
│
▼
[ Staging Area ]
│
▼
git commit
│
▼
[ Local Repository ]
│
▼
git push
│
▼
[ Remote Repository (GitHub) ]

🔹 Working Directory

Your project folder containing actual files.

Files are not tracked until staged.

🧰 Commands
git bash

```
git status
```

git diff

🔹 Staging Area (Index)

Holds files ready to be committed.

You decide which files to include in the next commit.

🧰 Commands
git add filename.txt

git add .

git status

🔹 Local Repository

Stores committed snapshots of your project.

Allows viewing or reverting to previous commits.

🧰 Commands
git commit -m "Commit message"

git log

git show

🔹 Remote Repository (GitHub)

Online storage of your repository for collaboration.

Hosted on GitHub or similar platforms.

🧰 Commands
git remote add origin https://github.com/username/repo-name.git

git push origin main

git pull origin main

git clone https://github.com/username/repo-name.git

⚙️ Git Configuration

Before first use, configure your Git identity.

🧰 Commands
git config --global user.name "Your Name"

git config --global user.email "your@email.com"

git config --list

🏗️ Initializing a Git Repository
🧰 Commands
mkdir project-folder
cd project-folder
git init

☁️ Linking Local Repository to GitHub
🧰 Commands
git remote add origin https://github.com/username/repository-name.git
git remote -v

📤 Uploading Files to GitHub
🧰 Commands
git add .
git commit -m "Initial commit"
git push origin main
