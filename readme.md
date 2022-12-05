## linux commands

`pwd` - present working directory
`cd <directory-name>` 
`ls -la` - everything including hidden folders

# git configuration

```shell
## global configs

git config --global user.name "prashant"
git config --global user.email "prashant@gmail.com"
```

```shell

# First navigate to your project directory / folder
# And then run following commands

# STEP 1 : Open terminal (`cd` to project root)
git init

# STEP 2: check of status of git repository
git status

# STEP 3: to add files in staging area (to track)
git add <file-name>

# STEP 4: create a file `.gitignore`

# STEP 5: run following command *only if* un-necessary files are not reflecting
# in `git status` command
git add --all

# STEP 6: whenever you run git commit all files under staging area are commited and
# certain unique "commit-id" is generated (SHA-256).
git commit -m "<commit-message>"

# STEP 7: run git log to see commit id and commit message history
git log

# STEP 7: copy https URL from github and paste 
git remote add origin https://github.com/python10sep/mini_xkcd.git

# STEP 8:
git push -u origin master
```

