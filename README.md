# ArtI Git Workshop (S23)

#### Git Workshop Overview:

- [ ] Decide when to have weekly ArtI meetings
- [ ] Installing Git ("git --version") and VS Code
- [ ] Creating a GitHub account and adding members as collaborators
- [ ] Access to the demo-repo respository
- [ ] Creating your branch in demo-repo
- [ ] Pushing your changes to demo-repo/your_branch
- [ ] Pulling changes from partner_branch to your_branch
- [ ] Pushing your changes to master_branch
- [ ] Pulling from master_branch to your_branch
- [ ] Access to the ArtI repository
- [ ] Creating your branch in ArtI repo
- [ ] Pushing your changes to ArtI/README

### Miscellaneous

- PLEASE WORK ON SEPARATE FILES to avoid GitHub merge conflicts
- When pushing your changes to GitHub, ALWAYS push to YOUR branch; you will push to master branch during our ArtI group meetings
- Set up frontend routing BEFORE coding any UI
- It might be easier to use a single .css file for the entire UI
- Check out [this video](https://youtu.be/RGOj5yH7evk) if you're completely lost in terms of Git commands
- `rafce`-> to create the skeletons of components in React

### Basic Git Commands

**(#.) steps needed to push code to GitHub after finishing up edits on the IDE**

- `status` -> **_(1.)_** check to see which files are being tracked or need to be commited
- `init` -> use this command inside of your project to turn it into a Git repository and start using Git with that codebase
- `clone` -> bring a repo down from the internet (remote repository like Github) to your local machine
- `log` -> outputs a log of all of your commits
- `add .` -> **_(2.)_** track all your files and changes with Git
- `commit -m "[descriptive message]"` -> **_(3.)_** save your changes into Git
- `push` -> **_(4.)_** push your changes to your remote repo on Github (or another website)
  - `push origin master` -> pushes your changes to master branch
  - `push -u origin master` -> sets up stream so that pushing to master branch is the default
- `pull` -> pull changes down from the remote repo to your local machine
- `reset [file-name]` -> undo an `add [file-name]`
- `reset HEAD` -> undo the last `commit`
  - `reset HEAD~1` -> undo the `commit` that was 1 commits ago

### Important Terminal Commands

- `code .` -> opens the code in VS Code depending on the filepath
- `cd ../[file-name]` -> gets you out of a folder
- `q` -> gets you out of a terminal response
- `clear` -> clears terminal
- `ls` -> see which files make up the repo

### Git Branching

- `branch` -> see the branches that make up the repo
- `checkout -b [new-branch]` -> creates new branch
- `checkout [existing-branch]` -> switches you to work on another branch
- `diff [another-branch]` -> see how another-branch differs from the branch you are currently on
- `branch -d [merged-branch]` -> deletes branch; only use if the branch has already been merged
- **_Using a pull request to push local branch's code master-branch:_**
- **_(1.)_** `status`
- **_(2.)_** `add`
- **_(4.)_** `commit -m "[message]"`
- **_(4.)_** `push origin [new-branch]`
- **_(5.)_** On the GitHub repo, you should see the option to create a pull request
  - **_Merging local branch's code with master-branch:_**
  - **_(6.)_** On the GitHub repo's Pull Request, you should be able to merge new-branch with master-branch (clicking the button will only merge the code on GitHub)
  - **_(7.)_** `pull [origin master]` -> pulls code from GitHub's master-branch to local machine's environment
  - **Merge Conflicts:**
    - after `pull [origin master]`, you might experience merge conflicts
    - VS Code allows you to manage merge conflicts within the IDE's terminal, BUT easiest way is to resolve it within GitHub's interface

### How to initialize a repository locally

- Create the folder and files in VS Code
- `git init` -> initializes empty Git repository
- `git status` -> check to see if on master branch
- `git add .` -> adds files to staging area
- `git commit -m "[message]" `
- Create repo (same name as the VS Code folder's name) in GitHub
- ` git remote add origin [HTTPS]`
- `git remote -v` -> to check to see if it worked
- `git push origin master`
- Done :)

### How to start a React Web App

- Create a new, empty folder on laptop
- Open VS code
- Open new folder through VS Code (or just drop folder into VS Code, if folder is located on Desktop)
- `npx create-react-app ./` within VS Code's terminal (VS code -> view -> terminal) in order to start the app
- `npm start` to view on a local host
- Good job :)

### Server side of a MERN stack application

- Create a new folder (titled "server") in the same folder that the front end of the web app is located in
- `npm init`
  - Keep hitting enter (this will be your package.json file)
- `npm i express` -> installs express package (the most common tool for making servers; provides you with the basic tools and methods to initialize a server)
- `npm i mongoose` -> a dependency that provides us with the method to make the model, so that you can see the schemas of mongoDB on the server side
- `npm i body-parser` -> a middleware that checks out http requests that comes from the client side; that the data and http requests are valid to run on the server
- `npm i nodemon` -> when we make any file changes and save them, this will automatically restart and update our server (we no longer have to do it manually)
- `"start": "nodemon index.js"` -> add to your scripts in package.json; whenever we start our program in the terminal, it also starts index.js with the nodemon package
- `"type": "module"` -> add before scripts in package.json; necessary for importing modules

Hello there!
