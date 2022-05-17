# ➖➖➖➖➖➖🔴 Git & Github 🔴➖➖➖➖➖➖

## How To Install Git ?

#### Using HomeBrew..
> Note >> Mac OS Already has git installed by Default, but HomeBrew git is better than Stock

1. Install HomeBrew First From This Link >> https://brew.sh/
1. Check if There is any updates by typing >> brew update or brew upgrade
1. Install git by typing >> brew install git
1. Check version by typing >> ```git --version```

#### Using Website
1. go to https://git-scm.com/
1. Choose Your Operating System.
1. Download & Install
1. Done



## Git Initialization.
> Change Directory to the Path of the Project
```
git init
```

## Git Configurations.
### Setting Configuration.
```
Git config --global user.name “Omar Ashraf"

Git config --global user.mail “omar_ashraf_93@hotmail.com”

Git config --global user.author “Omar Ashraf”
```
### Getting Configuration.
```
Git config --global user.name

Git config --global user.mail

Git config --global user.author
```

## Check Repo Status.
```
git status
```

## Adding Files to Staging Area.
```
git add .

git add *

git add File_Name
```

## Removing Files from Staging Area.
```
git reset .

git reset *

git reset File_Name
```

## Committing to Local Repo.
```
git commit -m “Your Commit Message”
```

## Git Log.
> Git log is a utility tool to review and read a history of everything that happens to a repository. Multiple options can be used with a git log to make history more specific. Generally, the git log is a record of commits.

```
git log

git log --oneline
```

## Un-Commiting.

### ➔ Checkout Commit
   * It Will Only Show You What The Code Was Like at This Commit ( Read Only )
   * Use ```git chechout master``` or ```git checkout main``` When Finishing To Go Back.
```
git checkout Commit_ID
```
### ➔ Revert Commit
   * It Will Revert The Commit ID You Passed to it by Adding One More Commit With the Revert.
   * Same Like Undoing One Particular Commit.
   * Use ```git push origin main``` After That (Because It is Actually a Commit)

```
git revert Commit_ID
```
### ➔ Reset Commit
   * It Will Reset the HEAD to The Commit ID You Passed to it & Remove all the Commits after it as it never happened.
   * Use ```git push origin main --force``` After That.
```
git reset Commit_ID --hard
```
## Branches.

### Checkout to Specific Branch.
```
git checkout Branch_Name
```

### Checkout To Master or Main Branch.
```
git checkout master

git checkout main
```

### Create Branch & Checkout To It In One Command.
```
git checkout -b Branch_Name
```

### Show All Branches.
```
git branch
```

### Delete Branch.
```
git branch -d Branch_Name      // Only Works if Branch is Megred
```

```
git branch -D Branch_Name      // Works Even if Branch is Not Merged
```

### Merging branches With Master
> Note: You Have To Be On The Master Or Main Branch To Be Able To Merge.

```
git checkout master

git merge Branch_Name
```

## Git Clone.
> git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository.

```
git clone URL.git
```

## Generate & Test SSH Key ID.
1. Type >> ```ssh-keygen -t rsa -b 4096 “omar_ashraf_93@hotmail.com”```
Or Type >> ```ssh-keygen -o -t rsa -c “omar_ashraf_93@hotmail.com”```
1. Enter File Path: Enter
1. Enter Password
1. Re-Enter Password
1. ```cat ~/Path/Path/id_rsa.pub```
1. Copy The ID Value Starts with ssh-rsa
1. Open Github Settings > SSH & GPG Keys
1. New SSH Key
1. Enter The Copied ID Value & Give it a Proper Name
1. Type >> ```ssh -T git@github.com```
1. Enter Password
1. DONE (AUTHENTICATED) √

## Change SSH Key ID Password.
1. Type >> ```ssh-keygen -p```
1. Enter File Path: Enter
1. Type Old Password
1. Type New Password
1. Retype New Password
1. DONE √

## Aliases.
```
git config —global alias.(Shortcut) (Command)


//Examples
$ git config --global alias.ch checkout
$ git config --global alias.br branch
$ git config --global alias.co commit
$ git config --global alias.st status
```

## Push To Remote Repo.
```
git push origin master
git push origin main
```
Or Push a Branch
```
git push origin Branch_Name
```

## .gitignore File.
> .gitignore file tells Git which files to ignore when committing your project to the GitHub repository. gitignore is located in the root directory of your repo. [Read More](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

