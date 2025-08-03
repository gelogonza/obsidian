---
Course: Git
Date: 2025-04-12
---
**git status**

- shows the state of the working tree
- lets you see which changes Git is tracking
    - allows you to decide whether you should ask Git to take another snap shot

  

### git add

- command that tells git to start keeping track of changes in the files you specify
    - otherwise known as staging
    - arent committed but are stored in the staging area

  

### git commit

- after staging you save your work by commiting
    - commiting can include a message
    - uploads everything you added to the commit while staging
        - includes authors name
        - email
        - date
        - unique identifier
        - and comments explaining the commit

### git log

- allows you to see information about previous
- git log prints information about the most recent commit
    - time stamp
    - author
    - commit message
- helps keep track of what you’ve been doing and what changes you made

### git help

- command that shows you a list of all the other commands
    - once you’re in another command like commit you can use git commit —help and it’ll bring up a page about that
        - works with other commands not just git commit of git help

  

### Questions

**Which of the following scenarios is a common use case for a version control system?**

- Making experimental changes to your project in an isolated branch. 

  
**What is another name for a version control system?**  

- Software configuration management (SCM) system 

  
**What’s the difference between Git and GitHub?**  

- Git lets you work with one or more local branches and push changes to a remote repository. GitHub acts as the remote repository, which is accessed through a website or command-line tools.   
      
    

**What Git command gives information about how to use Git?**

- `git help`