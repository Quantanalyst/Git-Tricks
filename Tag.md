# Tag

Tags are useful for tagging the milestones. For example, the first version that we release to the public. You can create a tag by below code:\
$ git tag -a < tag_name > -m < message >

Moreover, if you want to go back to your old commits and tag one of them, you can use their SHA code by below code:\
$ git tag -a < tag_name> < SHA code > -m < message >

Since git doesn't recognize tag changes as a real change, you need to push them separately to the remote by:\
$ git push origin --tags


