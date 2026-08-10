### configuring git
```bash
git config --global user.name "My Name"
git config --global user.email "someone@email.com"
git config --list
```
- tells which account we are making changes in github using git
- configurations are of two types, `gloabal` and `local` (for specific account/repo)
- last command above shows what all set up using `git config`

### some git tools
- `clone` : clone repo on local machine
- `status` : displays state of code
- `add` : to add change before commiting (optional)
- `commit` : to finally add a change in original code

### types of status
- `untracked` : new files that git doesnt know and doesnt track yet
- `modified` : file that is changed into
- `staged` : file is ready to be commited (after adding before commiting)
- `unmodified` : unchanged

### add and commit
- `add` : adds new or changed files in working directory to git's staging area
```bash
git add <file name>
```

- `commit` : it is the record of change
```bash
git commit -m "some message"
```
- `-m` : adds message to be displayed
- the above commits for all added changes

### push command
`push` : to upload local repo content to remote repo

```bash
git push origin main
```

- `origin` : the default repo used to clone the repo is called the `origin`
- `main` : name of the branch to be used

### init
- used to create a new git repo
- we know a folder is not tracked by git if `ls -a` does not have a folder named `.git`
```bash
# to add a new directory to git
git init

# to add new remote (github repo) and name it "origin"
git remote add origin <link>

# to verify remote
git remote -v

# tells which branch we are on
git branch

# to rename current branch (Master) to Main
# main is the default branch
# but git branch will by default give Master as output, so change it
git branch -M main

# finally push changes to the main branch
git push origin main

# or else we can use
git push -u origin main
```

- `-u` : means upstream, which sets origin main as default
- next time if we use just `git push` it will auto understand the `origin main`
