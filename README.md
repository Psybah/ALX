# ALX – All My ALX Projects in One Place 🚀

During my time at ALX, I worked on multiple projects, each in its own repository. Managing them separately became inefficient, so I decided to merge everything into a single repository: **ALX**.  

This repository now contains all my ALX-related projects, making it easier to access and manage.  

---

## What Changed?  

Previously, each project had its own repository, with independent version histories and tracking. Git suggested using **submodules**, which allow you to embed repositories inside another repo while keeping them separate.  

However, submodules require additional steps to clone, update, and manage properly. While they are useful in certain cases, they can also complicate things.  

> **Let’s just say submodules are not always the simplest solution.**  

Instead, I chose to **remove the individual repositories' histories** and merge everything into this one repository.  

---

## How I Did It  

### **Step 1: Remove Git from All Sub-Repos**  
Since each ALX project was its own Git repository, I had to remove their `.git` directories to make them part of this repo:  

```bash
find . -name ".git" -type d -exec rm -rf {} +
This deleted all Git tracking data from the individual projects, leaving only the raw project files.

Step 2: Reinitialize a New Git Repository
After removing the old Git histories, I set up a fresh repository for ALX:

bash
Copy
Edit
git init
git branch -m main
git remote add origin https://github.com/Psybah/ALX.git
git add --force .
git commit -m "Merged all ALX projects into a single repository"
git push -u origin main
Now, all my ALX projects exist within one repository, without the complexity of submodules.

Should You Do This?
This approach works well if you:

Want to consolidate multiple repositories into one for easier management.
Don't need to preserve the individual commit histories of each project.
Prefer a simpler structure without handling submodules.
However, if you need to keep separate commit histories, using submodules or monorepo strategies may be a better approach.

What's Inside?
This repository includes various ALX projects, such as:

AirBnB_clone_v3
Simple Shell
Monty
Binary Trees
And many more...
All projects are now accessible in one place. 🚀
