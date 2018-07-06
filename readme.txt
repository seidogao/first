Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
add remote
Creating a new branch is quick.
Creating a new branch is quick and simple.
 new branch 'dev'
modify for dev
modify for pc2

git clone -o remotegit git@github.com:seidogao/first.git
git push remotegit master
other: git pull remotegit master

git checkout -b dev remotegit/dev
git push remotegit dev

因此，多人协作的工作模式通常是这样：
首先，可以试图用git push origin <branch-name>推送自己的修改；
如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
如果合并有冲突，则解决冲突，并在本地提交；
没有冲突或者解决掉冲突后，再用git push origin <branch-name>推送就能成功！
如果git pull提示no tracking information，则说明本地分支和远程分支的链接关系没有创建，
用命令git branch --set-upstream-to <branch-name> origin/<branch-name>。
add for rebase1
add for rebase2
