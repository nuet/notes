
以下可能复制第一行就行了
复制 C:\Users\chenx\Downloads\luarocks-2.4.1-win32\win32\lua5.1 到c:\lua
复制 C:\Users\chenx\Downloads\luarocks-2.4.1-win32\win32\lua5.1 到c:\lua\lua5.1


双击  C:\Users\chenx\Downloads\luarocks-2.4.1-win32\install.bat


执行下这个命令，否则cl.exe不存在(如果没有VS要安装某个插件)  errno.h找不到
 可能是在当前命令行下执行下， 设置当前命令行的变量属性？？
D:\Program Files (x86)\Microsoft Visual Studio 14.0\VC\bin\vcvars32.bat


设置代理否则翻墙下不了(蓝灯翻墙)
set http_proxy=http://127.0.0.1:60165

cd C:\Program Files (x86)\LuaRocks
luarocks install Ldoc

执行此条命令生成api doc
c:\lua\bin\ldoc D:\patest\luascript


要生成的lua源码放在此目录  D:\patest\luascript\lua
生成api doc在此目录  D:/patest/luascript/docs/api
lua api配置文件内容如下(注释内) D:\patest\luascript\config.ld
/************
project='平安云测'
title='平安云测 API'
description='平安云测lua扩展函数帮助文档。'
format='discount'
backtick_references=false
file='D:/patest/luascript/lua'
dir='D:/patest/luascript/docs/api'
**************/


以下样式更改  文件: ldoc_css.lua
参考: http://blog.csdn.net/jncpp/article/details/42779355
~~~css
#content {
    margin-left: 14em;
    padding: 1em;
 /* width: 700px;*/
    border-left: 2px solid #cccccc;
    border-right: 2px solid #cccccc;
    background-color: #ffffff;
}
table.function_list td.name {
	background-color: #f0f0f0;
	min-width: 200px;
	width: 600px;
	max-width: 800px;
}
~~~
