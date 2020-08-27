First commit from thai.buiminh@nccsoft.vn
This project will demo git and git flow.

# …or create a new repository on the command line
`echo "# git-flow" >> README.md`

`git init`

`git add README.md`

`git commit -m "first commit"`

`git remote add origin git@github.com:thaibmnccsoft/git-flow.git`

`git push -u origin master`

# …or push an existing repository from the command line
`git remote add origin git@github.com:thaibmnccsoft/git-flow.git`

`git push -u origin master`

# …or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

# Git config 
## 1. Identify

`git config --global user.name “Thaibm"`

`git config --global user.email thai.buiminh@ncc.asia`

`git config user.email thaibm.uet@gmail.com`

## 2. Alias

`git config --global alias.co checkout`

`git config --global alias.br branch` 

`git config --global alias.ci commit` 

`git config --global alias.st status`

# Git flow
## 1. Work on new brand
Check out from master or dev branch: `git checkout -b your-new-branch` 

## 2. After finished your work. Add your change to staged and commit it
`git add .` or `git add your-file-name`

`git commit -m "Commit's message"`

## 3. After commit, merge the latest code from remote branch
### 3.1. The first way - Use MERGE
- Pull the latest code: `git pull origin dev` or `git pull origin master`
- Fix the conflict if you have and commit it

### 3.2. The second way - Use REBASE
- Checkout to master (or dev): `git checkout master`
- Pull the latest code: `git pull origin master`
- Checkout back to your new branch: `git checkout your-new-branch`
- Rebase master: `git rebase master`
- Fix the conflict if you have and then add it to staged. After that, use `git rebase --continue`

## 4. Push your branch
`git push origin your-new-branch`
