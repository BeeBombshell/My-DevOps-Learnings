# Git and GitHub - Quick Reference 👾

## What is Git?

- Git helps **maintain who did what and when**. 
- It is a **version control system**. 
- It is a tool that helps you manage your source code history. 
- It allows you to track changes to your code and collaborate with others.

## What is GitHub?

- GitHub is a **code hosting platform** for version control and collaboration.

- Allows us to host our Git Repositories.


## Pre-requisites

- [Install Git](https://git-scm.com) on your system. (GUI Clients - not recommended)

## Terminal Commands

Terminal helps us to manipulate the file structure on our system.

- `ls` - List all files and folders in the current directory.

- `mkdir folder_name` - Make a new directory with the specified *folder_name*.

- `cd folder_name` - Change directory to the specified *folder_name*.


## Git Commands

- `git init` - Initialize an empty Git repository.

- `git status` - To know if the changes added have been reflected in the staging area.

- `git add .` - Put all the untracked files in the staging area.

- `git commit -m "commit message"` - Commit the changes in the staging area with a commit message.

- `git log` - To see the commit history.

- `git restore --staged file_name` - To unstage a file, back as untracked.

## Working with existing projects on GitHub

- Fork the repository to your GitHub account.

- Clone the repository to your local system.
![Clone URL](./Assets/Screenshot%202023-01-02%20at%2011.19.22%20PM.png)

- Add remotes to the repository.
    - **Origin**
        ```git
        git remote add origin "Your forked repository URL"
        ```

    - **Upstream**
        ```git
        git remote add upstream "Original repository URL"
        ```

- Make different branch for changes/feature you want to add.
    ```git
    git checkout -b "branch_name"
    ```

- Stage files using `git add .` 

- Commit changes with a commit message.
    ```git
    git commit -m "commit message"
    ```

- Push changes to your forked repository.
    ```git
    git push origin "branch_name"
    ```