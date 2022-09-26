# Week 1 Git与Github的基本使用

## Introduction

Git是主流的代码协作工具，本周将学习Git与Git主流平台Github的使用

关于Github的访问问题可以参考[GitHub访问问题](GitHub访问问题.md)

## Tasks

### 1. Git的安装与基本配置

根据您使用的操作系统不同，Git的安装方式会有所不同。

**在安装Git后，通过输入`git config --global user.name <username>`设置您的用户名（替换`<username>`），再通过输入`git config --global user.email <email>`设置您的邮箱（替换`<email>`）。**

请注意：邮箱将作为您在开源社区中识别自己的重要凭证，请谨慎设置，建议不要使用qq邮箱或网易系
邮箱，推荐使用Gmail、Outlook等邮箱。

**Windows**

请在Git官网[git-scm.com](https://git-scm.com)下载并安装，安装后当您想要使用Git时建议您先通过打开开始菜单中Git
Bash以进行下一步操作。

**macOS**

请打开终端，输入命令`xcode-select --install`按下回车，系统会弹出窗口提醒您安装Xcode命令行
工具，完成系统要求后Git会自动安装。

**Linux**

根据发行版不同，安装方式也有所不同，在这里不再赘述。

### 2. Git的基本使用

学习Git基本知识后，完成下列任务。

1. 在一个空文件夹中新建Git repository；
2. 新建一个文本文档，文件名与内容随意，但不得为空文件；
3. 将变更Commit至默认仓库，Comment随意，下同；
4. 新建两个branch，名字分别为sub1与sub2，切换到各自branch后分别新建不同内容，不同文件名的文本文档后提交；
5. 切换至默认branch，将文本文档内容进行修改，再次进行Commit；
6. 利用git merge将三个分支的变更内容完美合并至默认branch。

### 3. Github的基本使用

1. 创建一个GitHub账号（*注意： GitHub在大陆访问较不稳定，请谨慎设定您的 GitHub ID*），创建
   后请及时填写成员GitHub信息表，待信息表中显示已发送邀请后，请按照指示操作接受邀请；
2. 创建一个Private Repository，并将该repository clone至本地计算机；（提示： 新手请使用HTTPS
   方式进行clone，若被提示输入用户名与密码，请输入你的GitHub用户名与密码)
3. 在本地计算机存储的该Repository中创建一个文本文档并Commit；
4. 将本地repository push至remote origin。

### 4. Github的进阶使用

本子任务均在3中创建好的private repository中进行

1. 在本地计算机的repository中对文本文档进行适当的更改；
2. 在GitHub网站上的repository中对文本文档进行适当的更改；
3. 在本地计算机中对相应的repository输入 git fetch 查看效果，并以你的方式解决冲突；
4. 解决好冲突后push至remote origin。

### 5. Github与团队协作

1. 将科中GitHub测试Repository Fork至您的账户，随后将您fork好的repository clone至您的本地计
   算机；
2. 按照该Repository中README.md的内容补充您的个人信息；
3. 对您的commit打上tag，名为您的GitHub ID；
4. 将本地计算机中的repository push至remote origin；
5. 在GitHub网站上您fork好的repository中提交Pull Request；
6. 接下来交给考核管理专员处理。

### Assessments

[任务提交处](https://docs.qq.com/sheet/DVE91VkhaS0FLY0Fx)
+ **Task 1**：不做考核
+ **Task 2**：请在您创建好的Repository中输入命令`git log --pretty=format:"%h - %an<%ae> - %ad : %s" -p > task2_assessment.txt`，完成后请将文件task2_assessment.txt提交至对应的收集表附件栏中
+ **Task 3, 4**：请将您的Private Repository改为Public,随后将您的repository以 `<username>/<repository>`的格式提交至收集表文本栏中
+ **Task 5**：成员侧无需额外操作

> 截至日期：2022年6月26日
>
> *作者：金一*
