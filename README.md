# WebPage

This repository contains a small multi-page landing site (Bootstrap) in Estonian.

Workflow requirements (follow these locally or on your remote):

- Keep `main` branch stable.
- Create a separate branch for each page or larger change (e.g. `feature/home`, `feature/info`, `feature/contact`).
- Make changes on the feature branch, commit, push, and open a Pull Request to merge into `main`.

Example commands:

```powershell
cd c:\Users\madilo\Desktop\webpage
# initialize repo (if needed)
git init -b main
git commit --allow-empty -m "Initial commit"

# create feature branch for homepage
git checkout -b feature/home
git add index.html
git commit -m "Add homepage"
git push -u origin feature/home
# open a Pull Request on GitHub to merge feature/home into main

# repeat for other pages:
git checkout main
git checkout -b feature/info
git add info.html
git commit -m "Add info/services page"
git push -u origin feature/info

git checkout main
git checkout -b feature/contact
git add contact.html
git commit -m "Add contact page with form"
git push -u origin feature/contact

``` 

Preview locally:

```powershell
python -m http.server 8000
# open http://localhost:8000 in your browser
```

