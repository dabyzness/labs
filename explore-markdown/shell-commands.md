# Bash Commands Cheatsheet

## Installing Oh My Zsh
1. Start a Linux terminal on Powershell and type:  
```sudo apt-get install zsh```

2. Now that Zsh is installed, we need to initialize and configure (optional) it. Enter:  
```zsh```

3. This will begin the configuration process. Type in option number 2 and hit enter. Option 2 will configure it based on the recommended settings for your machine:  
```2```

4. Now we need to install git if it's not installed already. If you have it installed skip to step 5.  
```sudo apt-get install git```

5. Now download from Git with the following command:  
```sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```

#### Congratulations, you've successfully installed Oh My Zsh!  
If you'd like to add some color-coded configurations, follow the next few steps. 

1. First, clone this repo into the plugins directory:  
```git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting```

2. Open your ```.zshrc``` file in VS Code:  
```code ~/.zshrc```

3. Finally scroll down to ```plugins=(...)``` on line 70. The plugin field accepts a space-separated list of plugins. Insert ```zsh-syntax-highlighting``` within that list:  
```plugins=([other-plugins-here] zsh-syntax-highlighting)```

4. Save and close the file. You've no added syntax highlighting to your Zsh CLI!


## Command Line Interface Cheat Sheet

 Command | Action 
:-------|:------
 ```cd``` | Change directory 
 ```cd ~``` | Change to home directory
 ```ls``` | Display contents of current directory
 ```pwd```| Display working directory
 ```mkdir``` | Create directory
 ```mkdir {1,2,3}``` | Create multiple directories named 1, 2, 3
```touch``` | Create file
```&&``` | Operator used to combine multi-line commands
```rm``` | Remove a file
```rm -rf``` | Remove everything inside of a directory
```rmdir``` | Remove empty directories
```mv``` | Move or rename a directory
```less``` | View the contents of a text file
```chmod``` | Change permissions of a file [read more](https://www.ibm.com/docs/en/zos/2.3.0?topic=descriptions-chmod-change-mode-file-directory)
```grep``` | Search text file with regex [read more](https://www.ibm.com/docs/en/zos/2.3.0?topic=descriptions-grep-search-file-specified-pattern)
```echo``` | Prints text to the terminal window [read more](https://www.ibm.com/docs/en/zos/2.3.0?topic=descriptions-echo-write-arguments-standard-output)


## Git Commands

 Command | Action 
:-------|:------
```git init``` | Initialize Git in directory
```git add .``` | Adds all changes files to staging area. Replace ```.``` with file name if you don't want to stage all files.
```git commit -m "message"``` | Commit all files in staged area with a descriptive message
```git push <remote-name> <remote-branch name>``` | Pushes commits from one place to another. Common push is ```git push origin main```
```git status``` | Shows whether files in directory have any changes since last commit/push
```git clone <url>``` | Clones a repository
```git remote -v``` | Display names of remotes that have been configured in the repository
```git remote add <name> <url of repo>``` | Links a local repo to a remote repo by adding a remote repo
```git remote remove <name>``` | Unlinks or deltes a local repo from a remote repo
 ```git pull <remote-name> <remote-branch main>``` | Fetches any existing updates from a remote repo and merges them into an existing local repo
