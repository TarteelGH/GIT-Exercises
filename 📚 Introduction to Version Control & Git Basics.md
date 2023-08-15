
# **📚 Introduction to Version Control & Git Basics**

- **Git Basics - [Git Documentation](https://git-scm.com/videos)**
    - [What is Version Control?](https://git-scm.com/video/what-is-version-control)
      
        > Version control, also known as source control, is the practice of tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. As development environments have accelerated, version control systems help software teams work faster and smarter. They are especially useful for DevOps teams since they help them to reduce development time and increase successful deployments.
Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.


        - **GIT** is fas and modern implementation of **version control** .
        - **GIT** provides **history** of content changes .
        - **GIT** facilitates **collaborative changeds** to files .
        - **GIT** is easy to use for any type of **knowledge worker** .
          
        > **Creat,Save,Edit and Save the thing gain**

    - [What is Git?](https://git-scm.com/video/what-is-git)
      
        - **Local GIT** : **Disributed** so that connenctivity does not block work .
        - **Git** is actually locally enabled , meaning that you can version-control items just on your dasktop , just withh a single piece of software available at the command line.
        - **Easy** so that learninig its commands can happen progressively .
        -  ` $ init myproject ` & ` $ cd myproject ` : To satrt off with the initialization of a project , That creates a directory , a folder that can contain the project files , as well as the control files store the historical elemtnts , source code  ...
        -  ` $ Git add ` : Thecommands that actually notices the files and puts them into kind of holding zone , ready to permenntaly be committed .
        -  ` $ gir commit -m"Importing all the code" ` : Is the key word that actually permanently records a historical version .
        -  **flexible** so that it fits your need instead of the other way around .
        -  **Powerfull** to satisfy the scripting needs of the advanced davelopers .
        
    - [Get Going with Git](https://git-scm.com/video/get-going)

        - To dowload it ` http://git-scm.com/downloads ` .
        - Configure username & email .
        - ` $ git config --global user.name "Tarteel Devops" ` .
        - ` $ git config --global user.email "tarteel.ghassan1@gmail.com" ` .
        - ` $ git init project1 ` : Creat my first Project - directory - .
        - ` $ cd project1 ` : Change directory .
        - ` $ git add file1.txt ` : creat file,txt .
        - ` $ git commit -m"My forst commit" ` : ` -m ` : allows us to provide a  commit message at the command line , describe what is happpening .

    - [Quick wins with Git](https://git-scm.com/video/quick-wins)

       - **GIT** is foucused on content , The importance precision deeeper than traditional version control system , so it can actually follow the move of source code from one file to another file
       - **GIT** idea o the staging area means that you elect which fles you want to participate in the next commit .
       - The idea of git is being open is one that is supported by the core tool as well as the surroundind servises
       - **GIT** is extremely effcient with its network transfers , to make it very simple to send large quantities of changes across ...
       - **Exchanges of code** actually become conversations , supported by some of rthe web services that surround GIT like GitHub .
       - **GIT** works entirely offline . commits,branches,merges,re-bases,resetting history , even searching through those historical events, all happened offline mode . The exchange of those changes , ` push ` ` pull ` being the commands that we use to execute those .
          
- **Git Tutorial - Getting Started**
    - Setting up a repository
        - [git init](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-init)
     
          - **SVN** : Subversion
          - The git init command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository. Most other Git commands are not available outside of an initialized repository, so this is usually the first command you'll run in a new project, A HEAD file is also created which points to the currently checked out commit,You can set the $GIT_DIR environment variable to a custom path and git init will initialize the Git configuration files there. Additionally you can pass the --separate-git-dir argument for the same result.
          - ` git init <directory> ` : Create an empty Git repository in the specified directory. Running this command will create a new subdirectory called ＜directory＞ containing nothing but the .git subdirectory.
          - **git init vs. git clone**
A quick note: git init and git clone can be easily confused. At a high level, they can both be used to "initialize a new git repository." However, git clone is dependent on git init. git clone is used to create a copy of an existing repository. Internally, git clone first calls git init to create a new repository. It then copies the data from the existing repository, and checks out a new set of working files. Learn more on the git clone page.
          - **Bare repositories --- git init --bare** ` git init --bare <directory> `
            Initialize an empty Git repository, but omit the working directory. Shared repositories should always be created with the --bare flag (see discussion below). Conventionally, repositories initialized with the --bare flag end in .git. For example, the bare version of a repository called my-project should be stored in a directory called my-project.git, The ` --bare ` flag creates a repository that doesn’t have a working directory, making it impossible to edit files and commit changes in that repository.
          - **git init templates** ` git init <directory> --template=<template_directory> ` Initializes a new Git repository and copies files from the   into the repository.Templates allow you to initialize a new repository with a predefined .git subdirectory. You can configure a template to have default directories and files that will get copied to a new repository's .git subdirectory. The default Git templates usually reside in a `/usr/share/git-core/templates` directory but may be a different path on your machine.The default templates are a good reference and example of how to utilize template features. A powerful feature of templates that's exhibited in the default templates is Git Hook configuration. You can create a template with predefined Git hooks and initialize your new git repositories with common hooks ready to go. Learn more about Git Hooks at the Git Hook page.
           - ` --SEPARATE-GIT-DIR= `
Creates a text file containing the path to . This file acts as a link to the .git directory. This is useful if you would like to store your .git directory on a separate location or drive from your project's working files. Some common use cases for --separate-git-dir are:
To keep your system configuration "dotfiles" (.bashrc, .vimrc, etc.) in the home directory while keeping the .git folder elsewhere
Your Git history has grown very large in disk size and you need to move it elsewhere to a separate high-capacity drive
You want to have a Git project in a publicly accessible directory like `www:root`

          - ` --SHARED[=(FALSE|TRUE|UMASK|GROUP|ALL|WORLD|EVERYBODY|0XXX)] ` Set access permissions for the new repository. This specifies which users and groups using Unix-level permissions are allowed to push/pull to the repository.

        
     
        - [git clone](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-clone)
        - [git config](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)
        - [git alias](https://www.atlassian.com/git/tutorials/git-alias)
        
    - Saving changes
        - [git add](https://www.atlassian.com/git/tutorials/saving-changes)
        - [git commit](https://www.atlassian.com/git/tutorials/saving-changes/git-commit)
        - [git diff](https://www.atlassian.com/git/tutorials/saving-changes/git-diff)
        - [git stash](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)
        - .[gitignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

<aside>


</aside>

- **Exercises**
    - [Git Kata: Configuring Git](https://github.com/eficode-academy/git-katas/tree/master/configure-git)

 ⌛️ Duration: 2h

- [ ]  Check if done
