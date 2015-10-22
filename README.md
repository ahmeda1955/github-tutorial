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
_*Typing in `git status` every once in a while, during the process of adding/commiting/pushing files wouldn't hurt, it'll help you keep track of the changes made to your file_  

8. Now your file is waiting to be sent to the github, however, you'd need another repo in github, so that you can `push` your file to.
9. Create a repo in GitHub. _**Make sure the repo's name is the same as the one in your local ide**_ (first-repo).

10. You're one step away from sending your file to the public! Congrats! Before publishing your file , you need to type in 
`git remote add origin https://github.com/ahmeda1955/first-repo.git` that's just you, connecting your local repo, to the github cloud repo.
11. Finally, what we've all been waiting for! You are now, ready to `push` or publish your file to the public! It's simpler than you probably thought. All you need to type in, in your local ide is `git push`. Yup, that's all, just `git push`; git is smart enough to only "push" or publish the files you have commited, by using `git commit -m "commit mesage "`


  

## Workflow & Commands
1. `git status` is a command used to help you stay on top of, and up to date with your file/code. For example, if your file name is shown in red, then git is letting you know that the last commit was altered/changed, if it is red, then git is telling you, that you are good, you are ready to push your file up to the cloud. _To use `git status` all you need type is `git status`, nothing less, nothing more; git needs to be initialized in your repository.  
2. `git add` is a command used to put your file in the stage, so that it is ready to be commited. To use `git add` with a specific file, you'd need to type in `git add "your-file's-name` your file's name without the quotations. Also, you can use the command `git add --all` that would make git add _everything_ in your current repository to the stage.
3. `git commit` is a command used to allow you to add a message next to your snapshots code. Once you commit a file, and add a message, your file is ready to be pushed up to the cloud;  commiting a file is the last step your file goes through before it is pushed to the cloud. To successfully commit your file, you neded to  type in  
`git commit -m "message to remind you what the commit was for"`
5. `git push` is the actual last step your file goes through to be pushed to the cloud, it makes sense! You are "pushing" all the files you added and commited to the cloud. To push your file to the cloud, you just need to type in `git push`, this will send all the files you have added and commited to the cloud instantly.




## Error Handling
- If you happened to `init` git in the wrong directory, you can simply just delete the whole .git subdirectory by running the command:  
`rm -rf .git` 


##Collaboration
_One of GitHub's best features is the collaboration system it offers. There are a couple of steps and concepts you need to understand in order for you to be successfuly able to collaborate on files in GitHub. You need to understand the concepts of **forking**, **cloning**, **pull requests**, and **pulling**._ 

1. _**Forking:**_ Forking is just a fancy/cool term that describes the action of making a copy of someone else's repository, on your GitHub. On the person's repository page on GitHub, there should be a button named as "fork" on the top right. Clicking on that button allows you to "fork" that person's repository. 

2. _**Cloning:**_ Cloning allows you to literally, clone a person's repository or make a copy of it in your IDE. Though cloning is a very cool and useful feature from Github, cloning a file _does not_ push it and mix it with their code. Anyways, to clone a person's file, you need to use the command `git clone`. After forking a person's repository, on the right side of the page, you should see a text box named "SSH clone URL". Copy and Paste that URL after the `git clone` command. So, it should be something like this:  
`git clone https://github.com/ahmeda1955/first-repo.git`

3. _**Pull requests:**_ After forking a repo, submitting a pull request  will allow the orignal owner to see the changes you've made to their repository. Once a pull request is sent, the repo's original owner  can review the changes made to their repo and even add it to the original code if they like it. You can submit a pull request by clicking on the small green button on the person's Github repo page, and then pressing Create pull request.

4. _**Pulling:**_ If the owner of the original repo you forked thought the change(s) you've made was really worthy of adding, the owner can accept your pull request through Github and `pull` your file. All they would need to type in is `git pull` and the changes they have accepted in the pull request would show up on their local machine.