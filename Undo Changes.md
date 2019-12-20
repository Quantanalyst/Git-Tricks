# How to undo changes and revert back to your old files?

1. If you have made some unwanted changes and _you haven't staged the file yet_. You can go back and undo your changes by **checkout** command\
$ git checkout -- < filename >

2. What if you have made those unwanted changes staged? Then you should first **unstage** them by using **reset** command:\
$ git reset HEAD < filename >\
and then checkout those unwanted changes.\
$ git checkout -- <filename>

3. And now, the worst case scenario. What if you have committed those unwanted changes? In this scenario, you should first find the SHA code of the commit before your unwanted commit (you can find that SHA code by $git log) and **checkout** that SHA code like below:\
$ git checkout < earlier SHA > < filename >

Another solution is to **rebase** to the commit you want
$ git rebase < earlier SHA >
(note: It works very well when you haven't pushed your changes to the remote)




