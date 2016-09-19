

http://blog.chinaunix.net/uid-11639156-id-3077471.html

注意装了git直接用 giv svn 不是 git－svn

下面是一个git-svn的一般使用流程：
1 git svn clone svn_repository   检出一个已存在svn repository(类似于svn checkout)
  git svn clone -r255:HEAD svn_repository_url   从指定版本开始克隆到本地
  svn info svn_repository_url, 记录最后的版本号

2 修改本地代码，使用git add / git commit将修改提交到本地git库
  git svn log  查看提交历史日志
  git svn log -v  可以提供每次commit操作涉及的相关文件的详细信息

3 git svn rebase  获取中心svn repository的更新, 如果提交有冲突也要调用这个获取最新文件
  冲突解决
  git add conflict.c
  git rebase –continue完成rebase操作

4 git svn dcommit   命令将本地git库的修改同步到中心svn库
  git svn dcommit -n 不会真正提交，而是显示差异

5 git rm filename  删除文件


参考:  http://www.cppblog.com/niewenlong/archive/2013/06/04/200791.html
git及git-svn使用：

下载svn源码：git svn clone http://xxxx myproject       （相当于svn checkout）

建立临时分支：git branch aaa
切换到临时分支：git checkout aaa
提交：git add .
提交确认：git commit
提交及确认：git commit -a     (git add . + git commit，但新增文件必须要git add .)

切换回master分支：git checkout master
合并临时分支：git merge aaa
删除临时分支：git branch -d aaa

从svn更新：  git svn rebase                             (相当于svn update)
提交至svn：  git svn dcommit                            (相当于svn commit)

查看状态：git status
查看diff：git diff，git diff head




问题*******
<filename>: needs update
 update-index --refresh: command returned error: 1
删除未上传的文件时出现过这个问题, 后来删掉文件,dcommit后,就能提交了
