# Create a New Github Repository - Step by Step

## 1. Prepare your local project

If your folder isn't a Git repository yet:

- Open the terminal and go to the folder using cd
- Initiate git with the **git init** command
- Always make sure to check your **git status**

---

## 2. Stage and commit your local files

- Add the files you want to commit (or the entire folder) by using **git add -file name- or **git add .\*\* (for the entire folder)
- Then do a first commit: \*\*git commit -m "initial commit"

---

## 3. Create a new (empty) repository on Github

- Then go to **GitHub -> Repositories -> New**
- Enter a repository name (e.g. personal-website -> it should match your local project name)
- Optionally add a description
- Choose **Public** or **Private** (for bootcamp challenges always public)
- **Do not** initialize with a README (if you already have one locally)
- Click **Create repository**

---

## 4. Connet your local folder with the remote repo

- Go to your empty Github repository
- Copy the **SSH repository address**, e.g. git@github.com:your-github-name/your-repo-name.git
- Add the remote repository "origin" to your local repository with the following command **git remote add origin -ssh link-**
- Check if it was successfully linked: **git remote -v**
- If the terminal shows you a **fetch** and a **push** address, it means everything worked out fine

## 5. Push your local repo to the Github

- In order to push your local repo to Github, all you need to do is enter the following command: **git branch -M main** and **git push -u origin main**

### Congrats! Your local files are now on Github!
