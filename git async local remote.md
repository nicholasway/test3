# git 本地项目与云端项目同步
---
> add new text

### 初始化本地仓库
``` git init ```
### 新建文件，将文件加入到暂存区
``` git add helloworld.txt ``` 或者   ``` git add -A  ``` **or** ``` git add . ```  //添加全部文件  
### 将文件添加到历史版本中
``` git commit -m 'add helloworld file to git remote' ``` -m 是版本的描述信息
### 将本地仓库与远程仓库连接
``` git remote add origin https://github.com/nicholasway/test3.git ```
### 将代码提交到远程仓库
``` git push -u origin master ``` **-u** 第一次提交让git记住本地仓库与远程仓库的链接，以后可以不用，直接使用git push 

### 出现的问题
**如何解决failed to push some refs to git**
出现错误的原因：**github中的README.md文件不在本地代码目录中**
*解决办法：* ``` git pull --rebase origin master ``` 执行完命令之后，远程的readme.md文件会同步到本地仓库中，这时再执行``` git push -u origin master ```即可