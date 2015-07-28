Hello Github
============

##Introduction

###Github

- Github is a web-based method of storing files.

- Public repositories are free, anyone can see them.

- Private repositories can be paid for.

- We don't store any passwords, secret keys, or other sensitive info.  Just code.

- Anyone can create a Github account.  No harder than creating a Facebook account.


###Gitlab

- Very similar to Github.  Web pages have a different look and feel.

- Can configure where files are stored.  LR Gitlab is configured to store locally.

- Used to store more sensitive code.  Such as code using legacy databases.

- Need to sign on with LR username and password.


###Git

- Git is the actual version control system. Github and Gitlab are 'remotes', or locations where everyone can find the files.

- At LR we generally use Git on the command line.  Tools with a graphical user interface are available.

- New files structures are created on a local machine, then 'pushed' to a remote like Github or Gitlab.

- Existing file structures are 'cloned' to a local machine, updated, and 'pushed' back to a remote.


##Using Github

- When creating a Github account, we generally use a name that our colleagues will recognise.

- Then we identify our development machines with Github using an SSH key. 

- Once that's done you can create a new repository, by clicking the button.

- Then you can follow the instructions to add code to the repository.

- Once the code is pushed you can create a branch from master to make changes.

- Once you pushed your changes you can create a 'Pull Request'

- Once the Pull request is accepted, you should delete the branch.  The change is now in Master.


##Using Gitlab

- Very similar to Github.  An active directory username and password is required.

- Click on 'New Project' (as opposed to 'New Repository' in Github)

- Select the appropriate visibility level.

- Follow the instructions to add code to the repository.

- Once the code is pushed you can create a branch from master to make changes.

- Once you pushed your changes you can create a more sensibly named 'Merge Request' (as opposed to Pull Request)

- Once the Merge request is accepted, you should delete the branch.  The change is now in Master.


##Additional reading.

- Generating SSH keys for Github.  https://help.github.com/articles/generating-ssh-keys/
 
- Git cheat sheet: Git: http://www.git-tower.com/blog/git-cheat-sheet-detail/

- Git basics: https://git-scm.com/book/en/v2/Getting-Started-Git-Basics

- Git simple guide: http://rogerdudler.github.io/git-guide/
 

##Some extra things we could cover.

- More command line Git commands

    - git clone

    - git pull
    
    - git diff
    
    - git merge
    
    - tagging
    
    - git checkout to undo
    
    






