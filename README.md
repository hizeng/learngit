#git的配置及操作小结

## 安装git：
     
     
最简单直接官网下载 本地解压安装git  
其他方法 后补...
## git常用的基本操作指令：
终端 进入新建的本地文件位置 $ cd ... $git init    
接着切换界面 正常去修改文件夹的内容 ...   
然后 返回 终端操作git  
###以下是重要操作思路 
#### git add : git add 你的文件.后缀  
#### git commit :git commit -m "引号内是你自己操作描叙"
git add 是将 “记录的修改——人” 放在一个空间 我把它叫 ***候车区***
git commit 是 将 上面 候车区 的 人 统一 ***装车***（推送到我们的master主分支）
####接下来如何推送到远程库？
### 推送到远程库 以GitHub为例子：
(首先要在 GitHub配置 SSH钥匙 _在终端操作_）

首次使用git 需要事先添加 用户名 和邮箱：
<<<<<<< HEAD
 `$ git config --global user.name "引号这里输入你的账号名字"`
=======

 `$ git config --global user.name "引号这里输入你的账号名字" 
 `
>>>>>>> 677239cf09ab82f081ae149c9dc54a17d21ee918
 
  ` $ git config --global user.email "引号这里输入你的邮箱"
`
 
 在终端获取SSH钥匙 命令：
 ` $ ssh-keygen -t rsa -C"你的git的用户邮箱" `，就凭感觉enter 下去  
 接着
 `$cd ~/.ssh` ——`$ls`——`$cat id_rsa.pub 
` 

下面出现你眼前的就是SSH 钥匙的公匙 复制 到GitHub设置SSH钥匙的页面 去 add 就好。
 
最后回到终端 输入推送的命令：

`$git remote add origin git@github.com:github账号/仓库名.git
`

`$git push -u origin master 
`  
测试二次推送

