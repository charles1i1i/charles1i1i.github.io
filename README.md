## 今天学习了MarkDown
###### MarkDown 是一种超文本语言，今天我第一次学习了它。
``Hello MarkDown！``
###### 接下来我还会学习:
1. Git的基础命令
1. Hexo架构
1. Hexo更换主题
###### 用命令行敲命令是一种Geek行为，我觉得还挺有趣的。
###### 有点意思，下面这张gif图可以形容我的心情:
## 如何查看本地的ssh
###### 我们可以用这个命令来查看我们是否生成了ssh：
``cat ~/.ssh/id_rsa.pub``
###### 如果有则会生成，如果没有则显示空白。
## 如何生成本地的ssh
###### 我们可以用这个命令来生成本地的ssh：
``ssh-keygen -t rsa -b 4096 -C "your_email@example.com"``
###### 有些东西需要自行更改。
## 获取ssh
``cat ~/.ssh/id_rsa.pub``
## 第一次使用git的时候需要进行全局变量设置
###### 全局变量设置
``git config --global user.name "name"``
###### 告诉git你的名字
###### 告诉git你的邮箱（这个邮箱最好是你注册GitHub的邮箱）
``git config --global user.email "916905688@qq.com"``
## git clone 命令
###### 可以使用git clone 命令把GitHub仓库里面的代码下载到自己的电脑上
``git clone 仓库地址``
## 常见的一些Linux命令
###### 查看当前目录下的文件：
``ls``
###### 查看当前目录下的文件，包括隐藏文件
``ls -a``
###### 在当前目录下创建文件：
``touch 文件``
###### 在当前目录下创建文件夹：
``mkdir 文件夹``
###### 进入某个文件夹：
``cd 文件目录``
###### 删除当前目录下的指定文件（慎用）:
``rm -rf 文件``
## git 提交三部曲：
1. git add
1. git commit
1. git push
## git add 命令
###### 第一步一般使用的命令：
``git add -A``
###### 如字面意思是all 就是提交全部的文件 （git add .）同意
## git commit 命令
###### 我们一般使用如下的命令行代码：
``git commit -m "本次提交的修改的备注"``
``新创建的文件必须要按照顺序进行提交，如果只是修改文件，并没有创建文件，也可以使用 git commit -am "本次提交的修改的备注" 来合并前面两个步骤``
## git push 命令
###### 分为以下几种情况：
* 第1次提交到本分支
* 第2-n次提交到本分支
* 提交到其他分支
### 第1次提交到本分支
``(2020.10.1前create github)git push origin master||(2020.10.1后create github)git push origin main``
### 第2-n次提交到本分支
``git push``
### 提交到其他分支
``git push origin b``
## 初始化git仓库
``我们使用`git init`命令将一个文件夹初始化为一个git仓库，出现下面的提示，表示初始化成功：``
## 我们使用下面的代码来绑定远程仓库：
``git remote add origin 仓库地址 ``
## 使用下面的代码来检查是否绑定成功：
``git remote -v``
## 安装Hexo
###### 执行以下命令创建我们的博客文件夹：
``hexo init blog``
###### 不知道如何命名就用blog这个名字
## 安装发布工具
###### 首先进入博客目录（cd blog）,打开 terminal 输入下面的命令：
``npm install hexo-deployer-git --save``
###### 注意：这个命令需要在文件夹中安装，如果更换文件夹需要重新安装。
## 修改配置文件找到"_config.yml" 打开，然后输入配置
``theme: landscape``

``deploy:``

  ``type: git``

  ``repository: 你的GitHub仓库地址``

  ``branch: master``
## Hexo 提交
###### Hexo 的提交也分为三个步骤
1. hexo clean
1. hexo generate
1. hexo deploy
### hexo clean
#### 清除缓存
### hexo generate
#### 生成静态文件 同 hexo g
### hexo deploy
#### 部署文件到博客
