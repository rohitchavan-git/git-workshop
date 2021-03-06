# Intro
This is a little guide to help you get introduced to git.
`Anything that looks like this should be executed in the terminal.`
# Part 0: Setup
1. Install git: https://git-scm.com/download
2. Set user info (needed before you can commit)
    * `git config --global user.email "you@example.com"`
    * `git config --global user.name "Your Name"`
3. Create github account with your Brock email: https://github.com/
4. Get your github education pack: https://education.github.com/pack

# Part 1: Working Locally
1. Create a folder called "git-stuff".
2. Create a text file in that folder.
2. Open either git bash or cmd, and navigate to your folder
3. `git init`
4. `git add file.txt`
5. `git commit -m "Created file"` (Creates a commit with the given commit message)
6. Open file.txt and type "Hello World". Save, close.
7. `git diff` (Shows the difference between your working directory and the git repo)
9. `git add .` (Adds files in the current directory recursively)
10. `git status` (Shows the changes that will happen when you commit)
11. `git commit -m "Added text"`

# Part 2: Working with Github
1. Go to github and create a new project: https://github.com/new
2. Name it something descriptive, and make it private (So you can control who sees it), then click "Create repository"
3. The page you go to gives you instructions on how to push an existing repository (the one you created earlier)
4. `git remote add origin https://github.com/Jesse-longname/something-descriptive.git`
5. `git push -u origin master` (When you push, it will ask you to sign in)
6. Refresh the github page with the instructions. Your repo should be there!
7. Locally, add a new file and put some text in it.
8. Add it to your repo, and commit it.
9. `git push` (Pushes the repo to github)
10. Refresh your github repo page, and you'll see the new file on it
11. On your repo in github, click "Create new file". Name it something, give it some contents, and create it.
12. Now we will get it onto your computer
13. `git pull`
14. Go to your folder, and you will see that the new file is there

# Part 3: Working with another repo and Branches
1. Go to https://github.com/BrockCSC/git-workshop
2. Click the "Fork" icon in the top right to fork this repo to your github
   account.
3. Navigate to your github page
   (`https://github.com/<your_user_name>/git-workshop`) Click "Clone or download" and copy the url
4. Go to your terminal and navigate to a folder that you want the git-workshop folder in. (Cloning creates the folder for you wherever you working directory currently is). Type `git clone [url]` in your terminal.
5. Now you have the repo locally.
6. Set the upstream repository as per
   [this](https://help.github.com/articles/configuring-a-remote-for-a-fork/) with `git remote add upstream https://github.com/BrockCSC/git-workshop.git`
7. Create a branch with your name
    * `git branch Jesse`
8. Navigate to the branch
    * `git checkout Jesse`
9. Edit the "Fixme.java" file. There are lots of erros in it. Find one or two to fix
   (spelling mistakes count!), add your changes and commit them.
10. Add and commit them.
10. Check the differences between your branch and the master branch
    * `git diff master` (master is the base branch)
11. Checkout the master branch again
12. Now the file you made is gone from your folder! Don't worry, it is still on your branch.
    * `git diff Jesse`
14. Once done, switch to your branch and `git push`.
15. Git will tell you there is no branch called that, so do the command it tells you to do
    * `git push origin Jesse`
16. Now go to `https://github.com/<your_user_name>/git-workshop` and you'll see your branch and changes under "branches"

17. Click on the "Pull request" button in the menu bar just above the repo.
18. Create a pull request to BrockCSC's master branch. You can see the changes
    between your commit and master. You should only see the changes that you
    made to the "Fixme.java" file. Create a message for your pull request and
    submit the PR.
19. Someone from the CSC will review your code and merge your request.
20. Congratulations, you have made your first open-source contribution! Now you
    can check out any of the literally thousands of open-source repos and do
    the same! (I recommend

    [Kubernetes](https://github.com/kubernetes/kubernetes/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22))
