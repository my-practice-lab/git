# README
“Talk is cheap. Show me the code.”--Linus
# Git是什么？
“Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.”

# Git教程
Git非常强大，命令也不少，但Git提供了清晰明了的[参考手册](https://git-scm.com/docs),Git归根结底只是一个工具，所以学习使用Git建议按照“二八定律”。

*二八定律是19世纪末20世纪初意大利经济学家帕累托发现的。他认为，在任何一组东西中，最重要的只占其中一小部分，约20%，其余80%尽管是多数，却是次要的，因此又称二八定律.*

# Let's Do it
## 新建一个仓库
* 登录[Gitlab](192.168.8.236),新建仓库` git-pr `,新建仓库后会自动出现命令行操作提示：

```
todo:

```


* 克隆仓库到本地
打开终端，使用` clone `命令加仓库地址克隆该仓库：

``` shell
git clone http://192.168.8.236/suen/git-pr 
todo:
```
*新建的仓库内没有任何文件，克隆完成会提示该仓库为空*
## 编写代码
* 进入仓库目录，新建一个目录：` pic `和文件：` README.md `：

``` shell
cd git-pr
mkdir pic
touch README.md
todo:

```
*`pic`目录存放截图文件，` README.md `文件的内容会自动显示在仓库的首页当中。因此，一般会在这个文件中标明本仓库所包含的软件的概要、使用流程、许可协议等信息，建议使用Markdown语法进行描述，还可以添加标记，提高可读性。*
* 编辑` README.md `文件：
向` README.md `文件添加仓库说明，关于为什么要添加` README.md `以及怎么编写这个文件，请参阅[如何为开发项目编写规范的README文件](https://www.cnblogs.com/wj-1314/p/8547763.html)。

可以使用` git status `命令查看当前工作树的状态，由于文件夹` pic `和文件` README.md `还没有添加到Git仓库，所以这里显示为**Untracked files**。

## 提交
将文件夹` pic `和文件` README.md `提交到仓库，这样文件就进入到版本管理系统的管理之下，以后的更改管理都交由Git进行。
```
git add .
git commit -m "add README"
todo:

```
通过` git add `命令将文件加入暂存区，再通过` git commit `命令提交。添加成功后可以使用` git log `命令查看提交日志。
* *` git commit `命令是将当前暂存区中的文件实际保存到仓库的历史记录中，通过这些记录，可以在工作树中复原文件*
* *` git diff `命令，可以查看当前工作树与暂存区的差别*

```
git log
todo:

```



## push代码

执行` push `命令后，Gitlab上的仓库就会被更新。
```
git push -u origin master
todo:

```

# 分支的操作
分支操作时Git的重要特性，大部分时间我们都是在利用分支进行开发，基本流程可以参考：**[利用分支进行开发的工作流程](https://git-scm.com/book/zh/v1/Git-%E5%88%86%E6%94%AF-%E5%88%A9%E7%94%A8%E5%88%86%E6%94%AF%E8%BF%9B%E8%A1%8C%E5%BC%80%E5%8F%91%E7%9A%84%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B)**
## 显示分支：` git branch `
` git branch `命令可以将分支名列表显示，同时可以确认当前所在分支。
```
git branch
todo:

```
` master `分支左侧标有` * `(星号)，表示当前所在的分支。

## 创建、切换分支：` git checkout -b `
以当前` master `分支为基础创建新的分支` suen `:
```
git checkout -b suen
todo:
```
使用` git branch `命令查看当前分支，可以看出有两个分支，当前分支为` suen  `:
```
git branch
todo:
```
如果要切换到` master `分支，可以使用` git checkout `命令：
```
git checkout master
todo:

```



# Homework
克隆该仓库，然后修改` README.md `,添加你的名字/昵称到` 已完成作业 `名单列表中,然后提交到你的远程仓库，并提交` Pull Requests ` ,等待管理员合并分支后，在该仓库就可以看到你的名字/昵称了。

# 已完成作业
恭喜以下小伙伴，顺利完成"家庭作业"
* [suen](192.168.8.236/suen)

