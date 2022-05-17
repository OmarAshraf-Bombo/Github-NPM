# Tutorials-and-CheatSheets
---
---
---
# ➖➖➖➖➖➖🔴 Markdown 🔴➖➖➖➖➖➖
## Headings

```
# heading 1
## heading 2
### heading 3
#### heading 4
##### heading 5
###### heading 6
```

## Italic Text
```
*Italic Text* or _Italic Text_
```

## Bold Text
```
**Bold Text** or __Bold Text__
```

## Strikethrough Text
```
~~Strikethrough Text~~
```

## Horizontal Rule
```
---
Or
___ 
```

## Blockquote
```
 > Blockquote Text
```

## Links
```
Normal Link
------------
    [Link Text](Link URL)

Link With a Title
------------------
    [Link Text](Link URL "Title")
```

## Unordered Lists
```
* Item 1
* Item 2
* Item 3
  * Nested Item 1
  * Nested Item 2
```

## Ordered Lists
```
1. Item 1
1. Item 2
1. Item 3
    1. Nested Item 1
    1. Nested Item 2
```

## Images
```
Same as links but with exclamation mark in the beginning.

    ![Alt Text](Image URL)
```

## Github Special Markdown
```
## Code Blocks

As all these black boxes in this tutorial.
For Some Reason I Can't Show it Here, But Make Sure to Remove The Curly Brackets.....

(```)Language Name
  Your Code Here
(```)

example
(```)javascript
  function Sum(num1, num2) {
    return num1 + num2;
  }
(```)

------------------------

## Tables

| Name     | Email          |
| -------- | -------------- |
| John Doe | john@gmail.com |
| Jane Doe | jane@gmail.com |

------------------------

## Task List

- [x] Task 1 Checked
- [x] Task 2 Checked
- [ ] Task 3 UnChecked
```
---
---
---
# ➖➖➖➖➖➖🔴 Npm 🔴➖➖➖➖➖➖

> Npm >> Node Package Manager.

> Nom was a stand alone company but Github Aquired Npm, and Microsoft owns Github so that means Microsoft Owns Npm.

> There is an Npm Alternative which is **YARN** which is Created by Facebook.

## How To Install Npm ?
> Note: Npm can not run without nodeJs.
  * Windows Users
    1. Go to https://nodejs.org
    2. Download LTS Version.
    3. Done.
  * Mac Users  
    1. Open Terminal
    2. Type brew install node
    3. Type brew link node
    4. Done
## Check Node Version ?
```
node -v
```
## Check Npm Version ?
```
npm -v
```
## What is Node Versioning ?
> Node Versioning is to have Multiple Versions of Node on your System.
## Why Node Versioning Exists ?
> * You Could be Working on a Legacy "Old" Project which runs old Node Version and at the same time you are working on a New Project with New Version of Node which have more Features.
> * Experimental Realeses of Node You want to try out but without breaking Your Projects.

## How Can We Manage Multiple Versions of Node (n) ?
```
sudo npm install -g n
```
## Install Latest Version of Node (n).
```
sudo n latest
```
## Install Specific Version of Node (n).
```
sudo n 6.0  // This Will Intsall Node Version 6.0
sudo n 17.4.0  // This Will Intsall Node Version 17.4.0
```
## How to Use the Version You Want ?
```
sudo n
```
* And you will see a list of all Node Versions Installed on your System.

* Use your up & down keys to choose the Version you want to use and press enter.

* press d to delete a Node Version you don't want.

## What is a Node Module ?
> Consider modules to be the same as JavaScript libraries. <br>
A set of functions you want to include in your application.

## How Does Npm install a Module ?
Under The Hood it will Run
```
 npm view Module_Name
```
which will get some data about that Module_Name, and most important is a tarball (.tgz) file URL.

It will then go to that URL file, Download it and Put it in a Folder called node_modules.

## What is Package.json and How to Create it ?

> A package.json is a **JSON** file that exists at the root of a Javascript/Node project. It holds metadata relevant to the project such as a project description, the version of the project in a particular distribution, license information, even configuration data, and it is used for managing the project's dependencies, scripts, version and a whole lot more.

```
npm init
```
This will ask you some questions which you can type your answer or press enter to leave the default Value.

You can Skip all of these questions by typing npm init --yes or npm init -y instead of npm init only.
```
npm init --yes
npm init -y
```
The Output will be a **JSON** File as said before, and this is an example of it.

```json
{
  "name": "npm",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Omar Ashraf",
  "license": "ISC",
  "keywords": [],
  "description": ""
}
```
and Normally you would see a Dependecies & devDependecies Key & Values, when you install them.
and here is an example as well.
```json
{
  "name": "npm",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Omar Ashraf",
  "license": "ISC",
  "keywords": [],
  "description": "",
  "dependencies": {
    "lodash": "^4.17.21"
  },
  "devDependencies": {
    "gulp": "^4.0.2"
  }
}
```

> Dependency is a library that a project needs to function effectively.

> DevDependencies are the packages a developer needs during development Only.

## How To Install a Package ?
```
npm install Package_Name

npm i Package_Name
```
> You can use **install** or **i** as a shortcut.

## How To Remove a Package ?
```
npm remove Package_Name

npm uninstall Package_Name
```
> You can use **remove** or **uninstall**.

## Local vs Global Packages.
> Local packages are installed in the directory where you run npm install Package-Name, and they are put in the node_modules folder under this directory.

> Global packages are all put in a single place in your system regardless of where you run **npm install -g** Package-Name. <br>
and Global packages is Used for any project not a specific project for example: create-react-app Package.

> You Install Gloabl Package as Follows.
```
npm install Package_Name --global

npm install Package_Name -g
```
> **-g** is a shortcut for **--global**.

## How To View All Your Global Packages ?
```
npm root -g
```
This Will Output a Path as follows
```
/usr/local/lib/node_modules
```
You can now change Directory to that Folder, and Open it.
```
cd /usr/local/lib/node_modules

open .
```

## Changing Global Packages Installation Location.
> 
> Note This is Not Recommended...

```
npm config set prefix Your/Path/Here
```

## Semantic Versioning xx.xx.xx (Major.Minor.Patch)
1. MAJOR version when you make incompatible API changes.
    * (Crashes The Project if Updated "Requires Developer to Update Code to work properly")
1. MINOR version when you add functionality or Feature.
1. PATCH version when you make some bug fixes.

> 📌 &nbsp; Note: 99% of Developers is **NOT** Following Sematic Versioning, and this is why Npm introduced the **package-lock.json** file in Version 5.

## What is Package-lock.json and Why it Exists ?

### ➔ The Problem
> * ```npm install``` is not deterministic. That is, if I run npm install today, and then I run it again two months from now, I may not end up with the same results.

> * What happens is that because of the ~ and the ^ contained in json, ```npm install``` will sometimes install updated packages without really raising a flag. Consider the following syntax: 1.0.1 = major.minor.patch.

> * ~1.0.1: this will install the most recent patch version for this minor. This can include 1.0.2, 1.0.3 and so on, but not 1.1.0. TL;DR: upgrade the patch as long as you stay at this minor.

> * ^1.0.1 : this is pretty much the same thing as the previous one, but for minor patches too . 1.0.1, 1.0.2, 1.1.0, 1.2.0 are all package versions that npm would install if you use that syntax. TL;DR : upgrade patch and minor, but not major.

### ➔ The Solution
> * package-lock.json: its goal is to provide an immutable version of package.json, so that you can, for example, pull an older version of your code (which contains the package-lock.json) and end up with the same node_modules folder.

> * package-lock.json : this file is generated by ```npm install```. If ```npm install``` ends up upgrading packages, it will output a new package-lock.json which contains details about the newer versions of the packages that were installed.

> * With package-lock.json comes this new npm command: ci. By running ```npm ci``` in a code base containing a package-lock.json, it is now possible to end up with a deterministic node_modules folder.

### ➔ Conclusion
> * ```npm install``` is not deterministic, but it generates a package-lock.json.
> * package-lock.json makes node_modules deterministic, by using the ```npm ci``` command.
> * Running ```npm ci``` on a package-lock.json will ALWAYS generate the SAME node_modules folder.


## Sementic Versioning in Package.json.
> In The Package.json File You Will Find a **^** Symbol Before Each Version Of Every Installed Dependency...

> This **^** Symbol Means If You Run ```npm install``` It Will Install The Version & Updated The Minor & Patch Version Automatically.

> You Can Change The **^** Symbol With **~** Symbol, Which Will Update Only The Patch Version & Leave The Major & Minor Version Untouched.

> If You Chose To Not The **^** Symbol or **~** Symbol, This Will Install The Exact Version In The Package.josn File Without ANy Updates.

## devDependencies.

> Packages that are only needed for local development and testing phase, as Jest, Babel, Webpack or Gulp...

> You can install a devDependency by passing a --save-dev flag in the end of you install commande.........Example below.
```
npm install Package_Name --save-dev
``` 

## PeerDependencies.
> You Will Never Use PeerDependencies in Your Project

> PeerDependencies are used when you are creating Npm Packages.

> Peer dependencies are a special type of dependency that would only ever come up if you were publishing your own package. Having a peer dependency means that your package needs a dependency that is the same exact dependency as the person installing your package.

## Npm Scripts

> An npm script is a convenient way to bundle common shell commands for your project. They are typically commands, or a string of commands, which would normally be entered at the command line in order to do something with your application. Scripts are stored in a project's package.json File.

> These Scripts are run (Prepublish, Install, Test, Preuninstall, prestart and more and more of Events.)

> Read More About Npm Scripts here >>  [Read More](https://docs.npmjs.com/cli/v8/using-npm/scripts)

## NPX

> NPX: The npx stands for Node Package Execute and it comes with the npm, when you installed npm above 5.2.0 version then automatically npx will installed. It is an npm package runner that can execute any package that you want from the npm registry without even installing that package.
```
npx install Package_Name         

npm install create-react-app
```

#### JUST FOR FUN
1. Open Terminal
1. Type ```npx cowsay Hellooooooo```
1. Hav Fun 😉


---
---
---
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

