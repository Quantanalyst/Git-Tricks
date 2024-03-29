# Git Basics

* **Initialize** a folder to make it a git repo. You need to do it once by ```git init```\
**$** git init

* **Staging** a file moves that file from project directory to **staged** _state_ . In this state, we still can make changes to the file and those changes are not recorded.\
**$** git add _filename_

* **Commiting** a file moves that file from staged state to **committed** state. In this state, we can't make any changes to the file. That file would get a version and we can always have access to that version and go back to that commit. \
**$** git commit -m "message"

Note: You need to include a mandatory brief note/message to your commits. 


### Git vs. Github

* Git
  * Version Control System (snapshots of versions)
  * Local
  * Distributed

* Github
  * Uses Git (copies or clones the repository)
  * Just one more computer that has a clone of the repo
  * Online
  * Adds user management (collaborators can discuss, ...)
  * Tool Integration (You can integrate with Slack, ...) 

### Fork

Forking is something that is only available in the context of Github. You can fork any public repo. If you fork a repo, all contents and commits of that repo will be copied on your account. Your copy only has original commits to the point of forking and from that point on, your copy and the original repo go separate ways. 
