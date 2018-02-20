# Git 常用基本操作命令
* 从远程服务器克隆仓库到本地电脑：用 ```git clone``` 命令
```
Administrator@PC-20170212VZUQ MINGW32 /f/Github
$ git clone git@github.com:Twanjun/Python-Spider.git
Cloning into 'Python-Spider'...
remote: Counting objects: 50, done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 50 (delta 7), reused 0 (delta 0), pack-reused 25
Receiving objects: 100% (50/50), 10.27 KiB | 0 bytes/s, done.
Resolving deltas: 100% (12/12), done.

Administrator@PC-20170212VZUQ MINGW32 /f/Github
$ cd Python-Spider

Administrator@PC-20170212VZUQ MINGW32 /f/Github/Python-Spider (master)
$
```
* 修改本地仓库文件，查看当前仓库状态：用 ```git status``` 命令
```
Administrator@PC-20170212VZUQ MINGW32 /f/Github/Python-Spider/spider-01 (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
上面的命令说 README.md 被修改过了，但还没有提交，所以接下来提交文件修改
* 要提交文件修改到当前分支，需要先用 ```git add <filename>``` 或 ```git add *``` 命令提交文件修改到暂存区，可以临时保存改动，然后用 ```git commit - "代码提交信息"``` 命令将暂存区里的修改提交到当前分支
```
Administrator@PC-20170212VZUQ MINGW32 /f/Github/Python-Spider/spider-01 (master)
$ git add README.md

Administrator@PC-20170212VZUQ MINGW32 /f/Github/Python-Spider/spider-01 (master)
$ git commit -m "write the instruction of spider-01.py in README.md"
[master 6623a84] write the instruction of spider-01.py in README.md
 1 file changed, 11 insertions(+)
```
* 将本地仓库改动的 master 分支推送至远程仓库，用 ```git push origin master``` 命令，可以将 master 换成你想要推送的任何分支。origin 是 Git 克隆远程仓库时，创建的指向远程仓库的默认名称
```
Administrator@PC-20170212VZUQ MINGW32 /f/Github/Python-Spider/spider-01 (master)
$ git push origin master
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 662 bytes | 0 bytes/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:Twanjun/Python-Spider.git
   6e0d83b..6623a84  master -> master
```
