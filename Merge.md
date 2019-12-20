# Merge

Types of Merge:
  * Fast-forward: The simplest form of merge. In this merge, the target branch is ahead of destination branch and when we merge them, it just adds the differents commits on the target branch to the destination branch and the pointer will be updated and the target branch will be deleted. 
  * Recursive: In this merge, the target and destination branch have their own unique commits, so, when we merge, we must combine these unique commits. 



In order to test an idea, we typically create a new branch and test our ideas on that branch and when we finalized our changes, we merge them to our main branch. This process is called **merge**. In order to merge two branches, first you must checkout to the destination branch and use the below code:\
$ git merge < target_branch > < destination_branch> 

for example $ git merge feature_1 dev

In Github, merge is called **pull request**. 

# conflict

When we try to merge two branches. If the changes (additions) are on different files or on different lines of codes in a file, then the merge is very straightforward. However, when there is two different versions for some lines of codes, then git will raise a conflict warning and it is upon to the developer to settle the conflict. 

Note: If you run into the conflict and you are not sure what to do on that moment, you can **abort** the merge and then settle the conflict later.\
$ git merge --abort
