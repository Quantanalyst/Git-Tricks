# How to create a branch?

* In order to **create** a branch, you simply should use **branch** command:\
$ git branch < branchname >

* In order to **switch** between branch, you should use **checkout** command:\
$ git checkout < branchname >

* The above two steps can be combined into one step by below command:\
$ git checkout -b < branchname >

* In orderto **delete** a branch, you should use **branch -d** command:\
$ git branch -d < branchname >

Note: To delete a remote branch you can use the following command:\
$ git push < remote_name > --delete < branch_name >

* In order to synch your local and remote repo, you must push the new branches to the remote repo.
$ git push < remote_name > < branch_name >
* If you have a new branch on your remote repo, you can't just pull that repo directly from the remote. You must create a branch locally that tracks that remote branch by:\
$ git checkout --track < remote_branch >



