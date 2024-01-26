# Essential steps to set-up your System:
## Setting up an IDE (Integrated Development Environment):
### 1) Pycharm:
- PyCharm is an integrated development environment (IDE) specifically designed for Python development.
- You can download PyCharm [here](https://www.jetbrains.com/pycharm/download/?section=windows). There are two versions available i.e. Professional version and Community version (free).
- After successfully installing PyCharm, you need to add new environment variables. Setting environment variables for PyCharm can be done at system level or by using PyCharm run configuration.
- To set environment variables at the system level on Windows:
  - Go to, edit the system environment variables
  - Environment variables
  - Under user variables select Path
  - Click Edit
  - Click New
  - Add (C:\Users\omkar\AppData\Local\Programs\Python\Python312\ & C:\Users\omkar\AppData\Local\Programs\Python\Python312\Scripts)
  - Click Ok
  - Click Ok
  - Click Ok
- You can find path and version of Python using below commands

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/f2b570b0-fd4b-4590-9341-b337d97c223c)

### 2) VS code:
- VS Code is a free and open source integrated development environment (IDE) developed by Microsoft.
- It supports multiple languages and comes with features such as debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git, which is very convenient for version control.
- It offers numerous settings and a vast marketplace with extensions for adding new languages, themes, debuggers, and connecting additional services.
- Working with VS Code can enhance your efficiency as a Data scientist. It can manage your entire data science project lifecycle.
- You can download VS Code [here](https://code.visualstudio.com/download).
- To open VS Code in specific folder:
  - Right click
  - Open in terminal
  - Run `code` command

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2f255810-d9f8-4485-b5fa-b4bf38c70e4c)

### 3) Anaconda:
- To use Jupyter notebook, you need to download Anaconda. You can download Anaconda [here](https://www.anaconda.com/download).
- Jupyter notebook is not a traditional integrated development environment (IDE). It is an open-source web application that enables you to create and share documents containing live code, equations, visualizations, and narrative text.
- After successfully installing Anaconda, you need to add new environment variables. Setting environment variables for Jupyter can be done at the system level.
- To set environment variables at the system level on Windows:
  - Go to, edit the system environment variables
  - Environment variables
  - Under sser variables select Path
  - Click Edit
  - Click New
  - Add (C:\Users\omkar\anaconda3\ & C:\Users\omkar\anaconda3\Scripts)
  - Click Ok
  - Click Ok
  - Click Ok
- To open Jupyter in specific folder:
  - Right click
  - Open in terminal
  - Run `jupyter notebook` command
- You can find path and version of Jupyter notebook using below commands

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/3fb73c31-00e7-432a-9ecd-a7745ba61e4e)

## Conda environment:
- Conda environment provides a way to isolate different projects, preventing conflicts between dependencies and package versions required by different projects.
- Creating a Conda environment is crucial for maintaining a clean, organized, and reproducible development environment. It helps manage dependencies, reduces conflicts, and enhances overall efficiency and reliability in Python projects.
- Environments allow you to manage specific versions of Python and other packages for a particular project. By specifying exact dependency versions, Conda environments make it easier to share code, enabling others to recreate the same environment without issues.
- Conda simplifies package management with a single tool for installing, updating, and removing packages, making it more user-friendly than manual dependency management.
- With Conda, you can easily switch between different Python versions for different projects, particularly beneficial for projects with specific Python version requirements.
- Use Conda prompt or Command promt or VS Code powershell (ctrl + `) for Conda operations.

__Conda commands:__
| Command                                                                      | Use                                                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| conda info                                                                   | Used to verify whether Conda is installed or not                                                                   |
| conda --version                                                              | Used to check Conda version                                                                                        |
| conda update conda                                                           | Used to update Conda to the latest version                                                                         |
| conda env list                                                               | Used to get a list of all environments (active environment is shown with *)                                        |
| conda list                                                                   | List all packages and versions installed in an active environment                                                  |
| conda create --name your_env_name                                            | Create a new environment                                                                                           |
| conda create --name your_env_name python=3.x                                 | Create a new environment with a specific python version                                                            |
| conda create --name your_env_name python=3.x package1 package2 ...           | Create a new environment with a specific python version and specific packages                                      |
| conda env create --file environment.yml                                      | Create a new environment from a .YAML file (in .YML file env_name is already present)                              |
| conda create --name your_env_name --file requirements.txt                    | Create a new environment from a .TXT file (in .TXT file env_name is not present so that you need to give env_name) |
| conda create --name your_env_name python=3.x && conda activate your_env_name | Create a new environment with a specific python version and activate it                                            |
| conda activate your_env_name                                                 | Activate specific environment                                                                                      |
| conda deactivate your_env_name                                               | Deactivate specific environment and switch back to base environment                                                |
| conda env remove --name your_env_name                                        | Delete specific environment                                                                                        |
| conda create --clone source_env_name --name new_env_name                     | To make exact copy of a specific environment                                                                       |
| conda install package_name                                                   | Install a specific package to a currently active environment                                                       |
| conda install --name your_env_name package_name                              | Install packages in a specific environment                                                                         |
| conda update package_name                                                    | Update a package in a currently active environment                                                                 |
| conda install package_name=1.2.3                                             | Install a specific version of a package to a currently active environment                                          |
| conda install package1 package2 package3                                     | Install multiple packages at once to a currently active environment                                                |
| conda install -c channel_name package_name                                   | Install packages from a specific channel to a currently active environment                                         |
| conda install -c channel_name package_name=1.2.3                             | Install packages from a specific channel with a specific python version to a currently active environment          |
| conda install --file requirements.txt                                        | Install packages using a .TXT file to a currently active environment                                               |
| pip install -r requirements.txt                                              | Install packages using a .TXT file to a currently active environment (preferred way)                               |
| conda install --name your_existing_env_name --file requirements.txt          | Install packages using a .TXT file to a specific environment                                                       |
| conda env update --name your_existing_env_name --file environment.yml        | Install packages using a .YML file to a currently active environment                                               |
| conda list --export > environment.yml                                        | To generate .YML file from a currently active environment (error due to formatting)                                |
| conda env export --name your_env_name > environment.yml                      | To generate .YML file from a specific environment (error due to formatting)                                        |
| conda list --export > requirements.txt                                       | To generate .TXT file from a currently active environment (error due to formatting)                                |
| conda env export --name your_env_name > requirements.txt                     | To generate .TXT file from a specific environment (error due to formatting)                                        |
| conda list -e > requirements.txt                                             | To generate .TXT file from a currently active environment (error due to formatting)                                |
| pip freeze > requirements.txt                                                | To generate .TXT file from a currently active environment (error due to formatting)                                |
| pip list --format = freeze > requirements.txt                                | To generate .TXT file from a currently active environment (works fine this is the preferred way)                   |

__Ways to specify version numbers:__
| Specification         | Result                              |
|-----------------------|-------------------------------------|
| numpy=1.11            | 1.11.0, 1.11.1, 1.11.2, 1.11.18 etc |
| numpy==1.11           | 1.11.0                              |
| "numpy>=1.11"         | 1.11.0 or higher                    |
| "numpy=1.11.1|1.11.3" | 1.11.1, 1.11.3                      |
| "numpy>=1.8,          | 1.8, 1.9, not 2.0                   |

__Difference between .YML and .TXT file:__

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/7ac97e53-ee7f-403d-bcfc-8902d0b8d799)

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2b7eb970-556d-4f3c-ae8f-15294df568c8)

## Version control systems & Repository hosting services:
__Terminology:__
- Remote repository is a repository on GitHub account, whereas Local repository is repository in your local machine/computer.

### Version control systems:
__1) Git:__
- Git is a distributed version control system or tool that enables collaboration among multiple contributors by allowing them to work on the same project concurrently.
- It helps you manage and track changes in your code or project over time.
- Git can be used through the command line interface, but various GUI tools, such as GitKraken or GitHub Desktop, provide a visual interface for those who prefer not to use the command line interface, but as a programmer it's always a good practice to use terminal.

__2) GitKraken | Tower:__
- GitKraken is a graphical user interface (GUI) for Git, providing a visual representation of your repositories. Visualizes branches, commits, and merges.
- Tower is a popular Git client that provides a graphical user interface (GUI) for managing Git repositories. It is not an intrinsic part of Git itself but is a third-party tool that facilitates Git-related tasks.

__3) GitHub Dekstop:__
- GitHub Dekstop is another graphical user interface (GUI) for Git, providing visual representations and simplifying common Git operations.

__4) SVN (Subversion):__
- SVN is a centralised version control system that helps software developers manage and track changes in their code over time.
- It allows multiple people to work on the same project simultaneously, keeping a history of modifications, and facilitating collaboration.

### Repository hosting services: 
- GitHub, GitLab, and Bitbucket are online platforms where you can store, collaborate, and manage your code that uses Git as the version control system. While they share the fundamental purpose of hosting repositories, they may differ in additional features, integrations, and the overall development ecosystem they offer.

__1) GitHub:__
- GitHub is a web-based platform, owned by Microsoft, for hosting and collaborating on Git repositories. It's like a cloud-based space to store and work on your code.
- It provides Git repository hosting, code collaboration, issue tracking, and integration with various development tools.
  
__2) GitLab:__
- GitLab is also a web-based platform for hosting Git repositories, similar to GitHub.
- It offers a complete DevOps platform, encompassing not only version control but also continuous integration and deployment (CICD).
- It provides Git repository hosting, continuous integration, deployment tools, code review, issue tracking, and more—all within a single platform.

__3) Bitbucket:__
- Bitbucket is also a web-based platform for hosting Git repositories, owned by Atlassian, similar to GitHub and GitLab.
- It provides Git repository hosting, code collaboration, integration with other Atlassian products (such as Jira), and support for both Git and Mercurial repositories.

### Authentication methods in Git:
- When connecting your local machine to a GitHub account or remote repository using Git, you need an authentication method. Here are several commonly used methods:

__1) HTTPS:__
- HTTPS authentication in Git uses username and password for authentication but GitHub deprecated password authentication for Git operations in August 2021.
- So it is recommended to use a Personal Access Token (PAT) instead of your account password.
- Easy to set up, but may require entering credentials again and again.

> Steps to generate PAT:
  - Go to GitHub settings
  - Developers settings
  - Personal access token
  - Token (classic)
  - Generate new token
  - Generate new token (classic)
  - Enter your GitHub password
  - Confirm
  - Set expiry date for token
  - Select scope of token
  - Generate token.
  - Use generated personal access token as a password during Git operations

__2) GCM (Git Credential Managers):__
- Enhances authentication by caching credentials.
- GCM is a one-time process, often requires logging in with a browser.
- By default, GCM is installed at the time of Git installation.
- If GCM is not installed in system you can download GCM from [here](https://github.com/git-ecosystem/git-credential-manager/releases) 

> Step to check whether GCM is installed or not using below command in Git Bash:
```ruby
git credential-manager-core --version
```
    
__3) SSH (Secure Shell) Keys:__
- SSH keys provides a more secure method for authentication.
- It requires generating an SSH key pair and adding the public key to your GitHub account.
- It enables secure communication via the SSH protocol.

> Steps to generate and set SSH key:
  - Open Git Bash and write below command:
```ruby
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
  - Specify location and name of the file to be saved
  - You can optionally set a passphrase for added security. Press Enter to skip or enter a passphrase when prompted.
  - SSH key will be generated and saved to the specified location
  - View SSH public key using below command:
```ruby
cat file_path.pub
```
  - Copy SSH public key
  - Add SSH private key to SSH Agent using below command:
```ruby
eval "$(ssh-agent -s)"
ssh-add E:/file_path
```
  - Add copied SSH public key to GitHub or Git hosting services, go to GitHub account
  - Settings
  - SSH and GPG keys
  - New SSH key
  - Give a title (just for your reference)
  - Paste SSH public key
  - Add SSH key
  - Enter Github password
  - Confirm

## Git branching simplified:
- Branching is extremely useful because when building new features for an application that might break your code or are not yet finished, you don't want to save them directly to the main master branch. Instead, you want to work on them in a kind of sandbox, a separate branch. This way, you can write and refine the code until it's correct and in the state you want, before merging it back into the main code base. This approach is especially helpful when multiple people are working on the same repository or when there are numerous branches in progress simultaneously.
- Git branching is like creating separate paths to work on different tasks without messing up the main project.
- It's like having different notebooks for different tasks, such as writing a story or drawing. This way, you can make changes and try out new ideas without affecting the main story until you're sure you want to include them. Once you're happy with your work in a branch, you can bring those changes back into the main project.
- Developers use branches to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It allows developers to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It helps in managing complexity by allowing developers to work on different tasks independently.
- It reduces conflicts by isolating changes in separate branches until they are ready to be integrated.
- It facilitates a more controlled and efficient development process, especially in collaborative environments.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/38bf13f5-9148-4202-808a-1b6b9fe4d433)

> Types of Branch in Git:

__1) Master/Main Branch:__
- The master (or main) branch is typically the default branch in a Git repository. It represents the stable, production-ready version of the code. Your main workspace where all the finished code lives.

__2) Feature Branch:__
- Developers create special areas to work on new things called "feature branches." Feature branches are like special areas for working on new features without disturbing the main project.
- Changes made in a feature branch can be brought back into the main project when ready. It's a way to keep everything neat and tidy while trying out and adding exciting features.
- When we create a new feature branch, initially, the code on the master branch and this new feature branch will be exactly the same. As you make updates and commit those changes to the feature branch, those updates are only visible in the feature branch. Similarly, when you make updates and commit changes to the master branch, those changes are only seen in the master branch.
- Each branch keeps track of the changes made on that specific branch. The changes made in one branch are isolated to that branch until they are explicitly merged into another branch.

__3) Bugfix Branch:__
- These are used to fix specific bugs without affecting the main code. Similar to feature branches, bugfix branches are created off the master branch.

__4) Release Branch:__
- These branches are created before releasing a new version for final testing. They are merged into both master and development branches once ready.

__5) Development/Branch-per-feature workflow:__
- In some workflows, each feature or task is developed in its own branch. Once the feature is complete, it is merged back into the main branch.

### Branching strategies in Git:
Every Git repository contains at least one long running branch commonly named main or master branch, representing the primary development path. Additional long-running branches, such as developement branch or production branch, may exist, persisting throughout the project lifecycle. These branches often reflect different stages in the release or deployment process.

Every git repository  typically called main or master branch. but there can be other long running branches called developer production these branches have something in common they exist throghout the complete lifecycle of the project. Another long running branches called integration branches often named develope or stging. Typically these branches represent states in a project release or deployement process

> Pushing local repository to GitHub account:
- Open local project folder having project files in it and copy path
- Open Git Bash and set username and email address
- Check for present working directory in Git Bash
```ruby
pwd
```
- Change current working directory of Git Bash to the project folder path (copied path)
```ruby
cd /e/copied_path
```
- Go to GitHub account and create a new repository (local and remote repository name can be differnet, doesn't have to be same) without initializing README file
- Come back to Git Bash and run below command
```ruby
git remote add origin https://github.com/user_name/remote_repo_name.git
git status
```
- Stage, commit and push all the files to the remote repository
```ruby
git add .
git commit -m "Commit message"
git push origin -u master
```

> Pushing changes to remote repository
- After making changes run below commands:
```ruby
git add .
git commit -m "commit message"
git push
```

> Clonning remote repository from GitHub account to local machine:
- Goto GitHub account and create a new repository and copy the HTTPS web url
- Open Git Bash and run below command
```ruby
git clone copied_url
```

> Pulling changes to local repository:
- Navigate to the local repository on your machine
- Run below command in Git Bash:
```ruby
git fetch origin
git merge
```

or you can use 
```ruby
git pull --------> (fetch + merge)
```

git fetch will check are there any new changes in remote repository which are not available in our local repositor. It's more like just checking to seen if there are any changes avialable.
Whereas git pull will fetch and merge/update new changes from remote repository to local repository.
![image](https://github.com/omkarfadtare/Essential/assets/154773580/03ba2592-fa02-4d29-bc91-5849a9b3eeb9)

> 











### Command line interface Git commands for branching
git branch * indicates that current branch
hit Q to get out of that
git checkout used to switch branches
git checkout -b feature_read_me_instructon (Give branch name as descriptive a possible) -b is for creating a new branch
git checkout feature_read_me_instructon  is used to change switch branch (You can hit tab button to auto fill the rest of the name)
git diff shows what changes have been made it compares the code and it shows all of the lines that have been changed
after commit and git push you need to create a pull request once the Pull request is merged you generally deletes the branch and switch back to master branch

manually created PR: You can also add or write a messege and 
put a ss

to get changes on the local master branch git pullif you do not have set upstream then set or else leave it
git branch -d feature_read_me_instructon (is used to delete branch)

__Merge conflict in Git:__
when you are building your own code writing bunch of code on your own branch maybe other people are writing code oon their branches and master is getting updated from multiple different places. So its possible that multiple people changes the same files and so sometimes git does not know which code you want to keep or which code you want to get rid of off or which code is reduncted

gti commit -am "added world line the code" adds and commits at the same time but this only works for modified files not for newly created file
what is git stash????

git merge master To merge branch

Why merging locally wasnt the regular pattern?
because master gets updated as you are working on the project because may be other people are meging into master and you dont have tose changes into your branch but you dont want to get too far behind the master as you are working because then its gonna be very difficult to merge later may be first git pull an dthen git merge 


There are couple of ways to fix merge conflicts interfaces, terminal but the best way to fix merge conflicts is to use code editor like vscode 

Undoing in Git:
so what if we make a mistake what if we acccidentky add something or commit something and we didnt want to do it 
- We can actually undo our stages or commits
staged but undo staging stage means git add
simply write git reset or git reset filename


undo a commit: mean git -m
git reset HEAD~1
here HEAD is to get pointer to the last commit and ~1 mean only one commit
gti log it will show all the commits and at the top it will show hashes then if you want a certain commit to reste copy that sopied_hash

git reset --hard copied_hash ????




Fork: used to make a complete copy of the other peoples repository
to get the access of all 
After forking you will have all the acecss for that repository you can create your own branch and then make changes or anything 
if you want your changes to be made in the original people repo you created a new pull request

dev does not get deleted 
Include some basic git Operations:
https://www.youtube.com/watch?v=RGOj5yH7evk&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=2
https://www.youtube.com/watch?v=Uszj_k0DGsg&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=3
https://www.youtube.com/watch?v=qsTthZi23VE&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=5


Intermediate git:
- The perfect commit:
- git add -p file_name
- the perfect commit message: subject + body
- git commit is used to enter commit message

Branching strategies:
Every git repository contain at least one long running branch typically called main or master branch. but there can be other long running branches called developer production these branches have something in common they exist throghout the complete lifecycle of the project. Another long running branches called integration branches often named develope or stging. Typically these branches represent states in a project release or deployement process. If your code moves through different states for example fromdevelopement to stging to the production it makes a lot of sense to mirror the structure to. And finally many teams have a convention connected to long running branches typically commits are never directly added to these branches. COmmits should only make it to the long running branches through integration. In other words through a merge or rebase. Thats because you dont wanna add untested unrevied code into your production environment thats why different codes should go through different tests and reviews before finally arrives at production. Another reason might be release bundling and scheduling you might want to release new code in batches maybe even thoroughly scheduled and without susch a rule. And it is also diffeicult because typically keeping an eye on what is released is difficult. 

IN contrast to long running branches they are created for certain purposes and then deleted after they have been integrated. there are many reason to create short lived branches for example when you statrt working on a new feature or a bug fix.
Github branching strategies:
- GitHub flow:
- Gitflow:
In GitFlow main branch is reflection of the current production state. The other long running branch is called as develope in any feature branches statrt from this one and will be merged back into it. Develope is also the starting point for any releases you would open a new release branch do your testing commit any bug fixes to that release branch. and once you are confident that its ready for production you merge it back into mai. You would then add a tag for that release commit on main and close the release branch.



Pull requests:
They are way to communicate about code and review it. The perfect example is when you have finished working on a feature without a pull request you would simply merge your code into main master or some other branch and in some cases this might be totally fine But especially when you are changes are a bit more complex or bit more importatnt you might want to have a second opinion to look over your code. And this is exactly the pull requests are made of. With pull request you can invite other people to review your work and give you a feedback. and after some conversation about the code your reviewer might approve the pull request and merge it into another branch.

Merge conflicts:

When they occur? 
git merge --abort



What they actually are?
How tosolve them?



















Python programming
- Introduction
- OOPS (Object oriented programming)
- Numpy
- PAndas
- Regex
- Data types in Python
- Sci-Kit learn
- MatPlotLib
- Seaborn
- NLTK
- Tensorflow
- Keras
- Automl
- Optical character recognition (OCR)
- Hello world

Learning Path
- Python
- Machine learning
- Deep learning
- Natural language processing
- AWS
