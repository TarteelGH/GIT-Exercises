
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
     
          - Here we'll examine the git clone command in depth. git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository. In this page we'll discuss extended configuration options and common use cases of git clone
          - **Cloning to a specific folder**` git clone <repo> <directory> `Clone the repository located at ＜repo＞ into the folder called ~＜directory＞! on the local machine.

           - **Cloning a specific tag**` git clone --branch <tag> <repo> `
Clone the repository located at ＜repo＞ and only clone the ref for ＜tag＞.
``` git clone -branchThe -branch argument lets you specify a specific branch to clone instead of the branch the remote HEAD is pointing to, usually the main branch. In addition you can pass a tag instead of branch for the same effect.` git clone --branch `This above example would clone only the new_feature branch from the remote Git repository. This is purely a convenience utility to save you time from downloading the HEAD ref of the repository and then having to additionally fetch the ref you need. ```

           - **Shallow clone**` git clone -depth=1 <repo> `Clone the repository located at ＜repo＞ and only clone the history of commits specified by the option depth=1. In this example a clone of ＜repo＞ is made and only the most recent commit is included in the new cloned Repo. Shallow cloning is most useful when working with repos that have an extensive commit history. An extensive commit history may cause scaling problems such as disk space usage limits and long wait times when cloning. A Shallow clone can help alleviate these scaling issues. 
  
            - In this document we took a deep look at git clone. The most important takeaways are:

              1. git clone is used to create a copy of a target repo

              2. The target repo can be local or remote

              3. Git supports a few network protocols to connect to remote repos

              4. There are many different configuration options available that change the content of the clone
          
        - [git config](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)

             - The most basic use case for git config is to invoke it with a configuration name, which will display the set value at that name. Configuration names are dot delimited strings composed of a 'section' and a 'key' based on their hierarchy. For example: user.email` git config user.email `
In this example, email is a child property of the user configuration block. This will return the configured email address, if any, that Git will associate with locally created commits.
           - **git config levels and files** ` --local ` , ` --global ` . ` --system ` .
           - **Writing a value**
Expanding on what we already know about git config, let's look at an example in which we write a value:` git config --global user.email "your_email@example.com" `
This example writes the value your_email@example.com to the configuration name user.email. It uses the --global flag so this value is set for the current operating system user.
             
      - [git alias](https://www.atlassian.com/git/tutorials/git-alias)
     
         - This section will focus on Git aliases. To better understand the value of Git aliases we must first discuss what an alias is. The term alias is synonymous with a shortcut. Alias creation is a common pattern found in other popular utilities like `bash` shell. Aliases are used to create shorter commands that map to longer commands. Aliases enable more efficient workflows by requiring fewer keystrokes to execute a command. For a brief example, consider the git checkout command. The checkout command is a frequently used git command, which adds up in cumulative keystrokes over time.
         ```
            $ git config --global alias.co checkout
            $ git config --global alias.br branch
            $ git config --global alias.ci commit
            $ git config --global alias.st status
         
    - Saving changes
        - [git add](https://www.atlassian.com/git/tutorials/saving-changes)

          - The ` git add ` command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit.In conjunction with these commands, you'll also need git status to view the state of the working directory and the staging area.
          - The ` git add ` and ` git commit ` commands compose the fundamental Git workflow. These are the two commands that every Git user needs to understand, regardless of their team’s collaboration model. They are the means to record versions of a project into the repository’s history.
          -  The` git reset `command is used to undo a commit or staged snapshot.
          -  ` git push ` is utilized to send the committed changes to remote repositories for collaboration. This enables other team members to access a set of saved changes.
          -  The` git add ` command should not be confused with svn add, which adds a file to the repository. Instead, git add works on the more abstract level of changes. This means that git add needs to be called every time you alter a file, whereas svn add only needs to be called once for each file. It may sound redundant, but this workflow makes it much easier to keep a project organized.
            
           ![image](https://github.com/TarteelGH/GIT-Exercises/assets/114241640/d0ce5f68-b9ef-4e99-a326-861d720c3f6b)

           - **Common options**` git add <file> `Stage all changes in <file> for the next commit.` git add <directory> `Stage all changes in <directory> for the next commit.`git add -p `Begin an interactive staging session that lets you choose portions of a file to add to the next commit. This will present you with a chunk of changes and prompt you for a command. Use `y` to stage the chunk, `n` to ignore the chunk, `s` to split it into smaller chunks, `e` to manually edit the chunk, and `q` to exitذ استخد` y لتقسيم القطعة ، و n لتجاهل القطعة ، و s لتقسيمها إلى أجزاء أصغر ، و e لتحرير القطعة يدويًا ، و q للخروج.`.
          
        - [git commit](https://www.atlassian.com/git/tutorials/saving-changes/git-commit)
 
           - The git commit command captures a snapshot of the project's currently staged changes. Committed snapshots can be thought of as “safe” versions of a project—Git will never change them unless you explicitly ask it to. Prior to the execution of git commit, The git add command is used to promote or 'stage' changes to the project that will be stored in a commit. These two commands git commit and git add are two of the most frequently used.
           - **Common options**`git commit`Commit the staged snapshot. This will launch a text editor prompting you for a commit message. After you’ve entered a message, save the file and close the editor to create the actual commit.`git commit -a`Commit a snapshot of all changes in the working directory. This only includes modifications to tracked files (those that have been added with git add at some point in their history).`git commit -m "commit message"`A shortcut command that immediately creates a commit with a passed commit message. By default, git commit will open up the locally configured text editor, and prompt for a commit message to be entered. Passing the -m option will forgo the text editor prompt in-favor of an inline message.`git commit -am "commit message"`A power user shortcut command that combines the -a and -m options. This combination immediately creates a commit of all the staged changes and takes an inline commit message.`git commit --amend`This option adds another level of functionality to the commit command. Passing this option will modify the last commit. Instead of creating a new commit, staged changes will be added to the previous commit. This command will open up the system's configured text editor and prompt to change the previously specified commit message.
           > The git add command adds files to the staging area whereas the git commit command will write changes to the repository permanently.
      
        - [git diff](https://www.atlassian.com/git/tutorials/saving-changes/git-diff)
     
           - Comparing changes with git diff Diffing is a function that takes two input data sets and outputs the changes between them. git diff is a multi-use Git command that when executed runs a diff function on Git data sources.
             
        - [git stash](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)
     
            - git stash temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on.

        - .[gitignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)
     
            - A gitignore file specifies intentionally untracked files that Git should ignore. Files already tracked by Git are not affected; see the NOTES below for details. Each line in a gitignore file specifies a pattern.


- **Exercises**
    - [Git Kata: Configuring Git](https://github.com/eficode-academy/git-katas/tree/master/configure-git)

 ⌛️ Duration: 2h

- [x]  Check if done
