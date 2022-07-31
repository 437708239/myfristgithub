# GitHub搭建仓库并上传本地代码

## 一、介绍
本文介绍如何搭建GitHub仓库并上传本地代码

### 具体步骤：
	1、安装 git 客户端 官网下载链接：https://git-scm.com]参数按默认安装即可
	2、注册一个github账号，登记后按界面右上角“+” New repository新建一个仓库，填写仓库的名称、其他默认，最后点create
	3、创建SSH协议登录服务器的密码，窗口执行指令如下: ssh-keygen -t rsa -C "注册邮箱"。并根据信息找到id_rsa.pub，在网页githubSSH and GPG keys中把该密钥添加进入
	4、Git是分布式版本控制系统，需要填写注册邮箱以及GitHub用户名作为标识
		* git config --global user.name "GitHub用户名"
		* git config --global user.email "邮箱"
	5、创建一个文件夹，依次输入一下指令完成上传
		* 把当前目录变成Git可以管理的仓库，指令如下： git init
		* 添加对应文件到本地仓库 添加全部文件指令：git add .  添加部分文件指令：git add ./xx文件
		* 添加上传文件的注释信息，指令如下：git commit -m "first commit"
		* 关联远端 github 仓库，即我们第2步创建的那个仓库。指令如下：git remote add origin git@github.com:仓库信息
		* 上传本地代码至GitHub，指令如下：git push -u origin main 或 git push ，(注意：第一次上传要验证账号的密码，终端输入失败可以直接关联网页)
	6、参考网站	：https://blog.csdn.net/Eayonz/article/details/122307521
	7、常用git指令参考网站：https://www.runoob.com/git/git-basic-operations.html