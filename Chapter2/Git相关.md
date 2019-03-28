# 第一节:Git相关命令

----------
## 上传本地项目到git ##
1. （先进入项目文件夹）通过命令 git init 把这个目录变成git可以管理的仓库  
`git init`

2. 把文件添加到版本库中，使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点“.”，意为添加文件夹下的所有文件  
`git add .`

3. 用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明  
`git commit -m 'first commit'`

4. 关联到远程库  
`git remote add origin 你的远程库地址`
> 例如: `git remote add origin https://github.com/sixmillions/demo.git`

5. 获取远程库与本地同步合并（如果远程库不为空必须做这一步，否则后面的提交会失败)  
`git pull --rebase origin master`

6. 把本地库的内容推送到远程，使用 git push命令，实际上是把当前分支master推送到远程。执行此命令后会要求输入用户名、密码，验证通过后即开始上传。  
`git push -u origin master`
---

## 命令速查
![git速查图](images/2-1-1.png) 

---
## git忽略文件

1. 创建.gitignore
2. 在里面填上要忽略的文件或者文件夹
    例如:  
    .idea //忽略.idea文件夹及文件夹下文件  
    *.iml //忽略以.iml结尾的文件  
    dbg/ //只忽略dbg目录，不忽略dbg文件  

    dbg  
    !dbg/  只忽略dbg文件，不忽略dbg目录  
[忽略文件介绍](https://www.cnblogs.com/wangmo/p/7737109.html "git忽略文件")
---

 

