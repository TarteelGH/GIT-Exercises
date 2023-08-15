# 💻 **Git Fundamentals and Basic Commands**

- **About Git** ****- Git Tutorial for Beginners****
    - [Command-Line Fundamentals](https://www.youtube.com/watch?v=HVsySz-h9r4)
 
        - `git log` : Git log is a utility tool to review and read a history of everything that happens to a repository. Multiple options can be used with a git log to make history more specific. Generally, the git log is a record of commits.
        - `git clone <url> < where to clone >`
        - `git remote -v` , `git branch -a`
        - In git we are working with three different areas:

            - The working directory where you are making your changes
            - The staging area where all changes you have added through git add will stay
            - The repository where every commit ends up, making your history. To put your staged changes in here you issue the git commit command.
          
    - [Git Basics - Recording Changes to the Repository](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

        - ![image](https://github.com/TarteelGH/GIT-Exercises/assets/114241640/0a45215a-e551-4d06-a0d7-8003b5b74473)
        - **Tracked** files are files that were in the last snapshot, as well as any newly staged files; they can be unmodified, modified, or staged. In short, tracked files are files that Git knows about.
        - **Untracked** files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area.
 > GitHub changed the default branch name from master to main in mid-2020, and other Git hosts followed suit.
      - The git add command takes a path name for either a file or a directory; if it’s a directory, the command adds all the files in that directory recursively.
      - While the git status output is pretty comprehensive, it’s also quite wordy. Git also has a short status flag so you can see your changes in a more compact way. If you run `git status -s` or `git status --short` you get a far more simplified output from the command.
      - Often, you’ll have a class of files that you don’t want Git to automatically add or even show you as being untracked. These are generally automatically generated files such as log files or files produced by your build system. In such cases, you can create a file listing patterns to match them named .gitignore. Here is an example .gitignore file:
```
$ cat .gitignore
*.[oa]
*~
```
The first line tells Git to ignore any files ending in “.o” or “.a” — object and archive files that may be the product of building your code. The second line tells Git to ignore all files whose names end with a tilde (~).
       - If the git status command is too vague for you — you want to know exactly what you changed, not just which files were changed — you can use the `git diff` command. We’ll cover git diff in more detail later.
       - It’s important to note that git diff by itself doesn’t show all changes made since your last commit — only changes that are still unstaged. If you’ve staged all of your changes, git diff will give you no output.
       - To remove a file from Git, you have to remove it from your tracked files (more accurately, remove it from your staging area) and then commit. The `git rm` command does that, and also removes the file from your working directory so you don’t see it as an untracked file the next time around.
       - Thus it’s a bit confusing that Git has a mv command. If you want to **rename** a file in Git, you can run something like:` git mv file_from file_to`
```
$ mv README.md README
$ git rm README.md
$ git add README
```
Git figures out that it’s a rename implicitly, so it doesn’t matter if you rename a file that way or with the `mv ` command. The only real difference is that `git mv` is one command instead of three — it’s a convenience function. More importantly, you can use any tool you like to rename a file, and address the `add/rm` later, before you commit.


- **Exercises**
    - [Git Kata: Basic Staging](https://github.com/eficode-academy/git-katas/tree/master/basic-staging)

 ⌛️ Duration: 1.5h

- [ ]  Check if done
