

http://blog.chinaunix.net/uid-11639156-id-3077471.html


下面是一个git-svn的一般使用流程：
1 git-svn clone svn_repository   检出一个已存在svn repository(类似于svn checkout)
  git-svn clone -r255:HEAD svn_repository_url   从指定版本开始克隆到本地
  svn info svn_repository_url, 记录最后的版本号
2 修改本地代码，使用git add/commit将修改提交到本地git库
  git-svn log  查看提交历史日志
  git-svn log -v  可以提供每次commit操作涉及的相关文件的详细信息
3 git-svn rebase  获取中心svn repository的更新, 如果提交有冲突也要调用这个获取最新文件
  冲突解决
  git add conflict.c
  git rebase –continue完成rebase操作
4 git-svn dcommit   命令将本地git库的修改同步到中心svn库
  git-svn dcommit -n 不会真正提交，而是显示差异
