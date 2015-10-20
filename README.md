# GitHub Tutorial

###_by **Ahmed Abdalla**_

---
## Git vs. GitHub
- **_Git:_** Git is an online version control serivce used for coding and software development; Git keeps "snapshots" of code; you don't need Github to use Git.  

- **_GitHub:_** GitHub is a Git repository hosting service that stores code in an online cloud which allows easy collaboration on files/code ; in order to use Github, you need to have Git. 




---
## Initial Setup
1. Create a GitHub account.
2. On your local IDE, type in `git config --global user.name "FirstName LastName"` 
3. Then, type in `git config --global user.email "email@appleseed.org"`
4. Look for and acquire the SSH key provided by your IDE service.
5. Now, go to Github > profile icon > settings > SSH Keys > Add SSH key
6. Type in the SSH key you acquired, and save it. It is recommended that you use  the name of the IDE service you're using to save the SSH key as it will help you identify which SSH belongs to what later on, when you connect your GitHub to more than one IDE service.
7. Finally, on your IDE, type in `ssh -T git@github.com` , then type in _yes_ to confirm.



---
## Repository Setup
1. In your IDE, type `mkdir first-repo` (first-repo would be the name of your repo)
2. Now, you have to navigate into the repo you just created, you do that by typing `cd first-repo`
3. Then, you intialize git in this directory/repo by typing in `git init`
4. Add a file; in this case we'll use a README.md file to get started. So, type in `touch README.md` to create a README.md file.
5. Save your file. (Check for an auto-save feauture provided by your IDE service)
6. "Add" your file to the Git stage by typing in `git add README.md`
7. Now, we have to "commit" the file which is the last step the file goes through before being sent through to the public!    
To make a commit you type in `git commit -m "add a message"`
  
_Typing in `git status` every once in a while while during the process of adding/commiting/pushing files wouldn't hurt._


---
## Workflow & Commands