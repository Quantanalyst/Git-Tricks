# How to make a folder a git folder

Open a terminal. Go to that folder. Use the below command:\
$ git init

After creating a local git repo. If we plan to push our changes to Github, we must create an online repo and assign the online address to the "remote". 
$ git remote add _origin_ "https:// ... " 

After assigning the online address to remote, we can push our changes on the master branch to the Github. 
$ git push origin master

Note 1: the "origin" is a common name assigned to the remote. However, you can use other names like "github" or ...
$ git remote add github "..."
$ git push github master

Note 2: If we plan to push our changes on other branch, we must modify the commands as below
$ git push origin _branchname_
