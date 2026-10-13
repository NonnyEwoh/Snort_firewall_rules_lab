# Publish This Project Using Git Bash

## 1. Create the GitHub repository

1. Sign in to GitHub and create a repository named `snort-firewall-rules-lab`.
2. Choose public or private as appropriate.
3. For a simple first push, create it empty (do not initialize it with a README, `.gitignore`, or license).

## 2. Open Git Bash

Extract the downloaded ZIP. Open the extracted project folder in File Explorer, right-click inside the folder, and select **Git Bash Here**.

## 3. Initialize and push

Replace `YOUR-USERNAME` with your GitHub username. Run these commands one at a time:

```bash
git init
git branch -M main
git add .
git status
git commit -m "Add Snort firewall lab documentation"
git remote add origin https://github.com/YOUR-USERNAME/snort-firewall-rules-lab.git
git push -u origin main
```

Review the output of `git status` before committing. Confirm that no executables, raw packet captures, credentials, or private data are staged.

## 4. If Git says there is no configured identity

Configure the name and email you want associated with your commits:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Then retry the commit.

## 5. If `origin` already exists

Check the current remote:

```bash
git remote -v
```

If it points to the wrong repository, update it:

```bash
git remote set-url origin https://github.com/YOUR-USERNAME/snort-firewall-rules-lab.git
```

## 6. Publish later changes

```bash
git add .
git status
git commit -m "Add lab evidence and findings"
git push
```

If there are no changes, Git may tell you there is nothing to commit.

## Authentication

Follow GitHub's current browser sign-in or credential-manager prompts. Do not put passwords or personal access tokens directly into repository files or commit messages.
