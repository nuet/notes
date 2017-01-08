mac git


### 设置一次， 不如缓存大小不够提交不了
git config --global http.postBuffer 524288000
git config --global http.postBuffer 1048576000

### 错误:  error: RPC failed; curl 56 SSLRead() return error -9806s
brew remove git
brew remove curl
brew install openssl
brew install --with-openssl curl
brew install --with-brewed-curl --with-brewed-openssl git

## 大文件操作
brew install git-lfs
git lfs install
git lfs track "*****.zip"
git add file.zip  以后就恶意按正常提交大文件了
git commit -m "Add design file"
git push origin master


git clone https://github.com/ogoodo/ncms.git
git clone https://github.com/ogoodo/ncms.git  new name

git pull 同步服务器到本地并merge到本地

git checkout

git status

git add filename or dir

git diff
git diff —staged


git commit
git commit -a  跳过暂存直接提交
git commit -a -m ‘提交备注’
git commit -amend   修改最近一次提交，注释有误或者漏提文件可以用

git push 提交到远程服务器

git rm  filename  删除文件
git rm -f filename 删缓存到暂存区域的文件
git rm —cached filename 删除暂存，不删除文件
git rm log/\*.log 删除log目录下扩展名为.log的文件
git rm \*~ 删除当前目录及子目录中所有～结尾的文件

git mv file_from file_to  移动文件

git log 查看提交日志
git log --pretty=oneline  查看提交纪录，
git log --pretty=oneline  filename

git show 查看文件具体修改内容
git show f006660f4412c79a86c9a9a9e89dda9a51b4742e(提交hash值)

分支操作

撤销上次提交到github的记录
1. git reset --hard HEAD~1
2. git push -f origin


create a new repository on the command line
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/ogoodo/url.git
git push -u origin master
