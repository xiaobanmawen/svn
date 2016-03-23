# svn
本地测试服务器搭建（实现每次提交更新web内容）
1.安装svn服务器
2.创建svn项目库
3.设置svn库hook文件，创建post-commit.bat文件，内容如下：
  @echo off
SET REPOS=%1
SET USER=%2
SET SVN="E:/Program Files/VisualSVN Server/bin/svn.exe"  //svn服务器路径
SET DIR="E:/wamp2/www"                                  //  web服务器代码路径
(call %SVN% update %DIR% --username izaodao --password izaodao --non-interactive)//username==svn用户名 password==svn用户名密码
4.注意事项：web目录下一定要用TortoiseSVN checkout出Repositories的代码
