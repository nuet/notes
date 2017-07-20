

maven 安装位置
~/chen/java/apache-maven-3.5.0

web application using java ee
1264


[使用maven命令终端构建一个web项目及发布该项目]
(http://www.cnblogs.com/codingcloud/p/5012606.html)(试用可行)
[使用Apache Tomcat Maven插件部署运行 Web 项目]
(http://www.cnblogs.com/codingcloud/p/5012845.html)
[使用eclipse构建Maven项目及发布一个Maven项目]
(http://www.cnblogs.com/codingcloud/p/5010314.html)(可以编译成功)
[Maven在Windows上的安装与配置]
(http://www.cnblogs.com/codingcloud/p/5009760.html)(没实验)

// 启动tomcat教程
http://tomcat.apache.org/download-90.cgi 下载tar.gz格式的文件
解压到~/Downloads文件夹
cd apache-tomcat-9.0.0.M22
cd bin
sh startup.sh   启动tomcat
访问  http://localhost:8080/
将需要部署的war包文件，如:helloweb-1.0-SNAPSHOT.war
复制到这个目录下  apache-tomcat-9.0.0.M22/webapps
访问  http://localhost:8080/helloweb-1.0-SNAPSHOT/

## 这个可以跑起来
[Eclipse中Maven WEB工程tomcat调试]
(http://blog.csdn.net/clj198606061111/article/details/20221133)(这个配置成功)
[The superclass "javax.servlet.http.HttpServlet" was not found on the Java Build Path]
(http://blog.csdn.net/testcs_dn/article/details/36455669)(这个要设置下，不然会出错)
[SpringMVC最基础配置]
(http://blog.csdn.net/clj198606061111/article/details/20492887)(.do跑不起来,.html可以)
[SpringMVC AJAX支持]
(http://blog.csdn.net/clj198606061111/article/details/20569087)(实验可以)
[springMVC文件上传]
(http://blog.csdn.net/clj198606061111/article/details/20666565)(实验可以)
[springMVC 文件下载]
(http://blog.csdn.net/clj198606061111/article/details/20743769)(实验可以)


[第三章 DispatcherServlet详解 ——跟开涛学SpringMVC]
(http://jinnianshilongnian.iteye.com/blog/1602617/)(这个可以学习下)
[maven 自动部署到 tomcat7]
(http://www.cnblogs.com/qq78292959/p/3711497.html)
[Maven Tomcat8+ 实现自动化部署]
(http://www.cnblogs.com/amosli/p/6086515.html)
