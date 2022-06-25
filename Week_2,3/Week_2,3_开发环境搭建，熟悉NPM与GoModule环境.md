# Week 2, 3 开发环境搭建，熟悉NPM与Go Module环境
## Introduction
对于Windows平台的开发，最好的开发环境便是Windows本身——安装Visual Studio便可以解决绝大多数的问题。然而对于Web开发则似乎存在着一些争论——这说明Windows可能对Web开发环境的搭建存在着一定的提升空间。原因在于Windows的既有命令行环境——`cmd.exe`对开发者并不友好；更主要的，是因为市面上68%[^1]的服务器都在采用Linux操作系统，无论是从系统运维层面上，还是从软件底层调用上，对于熟悉Windows操作环境的开发者无疑是一个挑战。解决Windows开发环境的瓶颈主要有两个解决方案——一是使用更加现代的PowerShell命令行，二是使用WSL，在既有Windows用户体验上用更简便的方式利用Linux。本周任务我们将同时介绍两种方法，来让大家熟悉PowerShell与WSL开发环境。

NPM是Node Package Manager，即Node.js的包管理器。不过实际上不止Node.js，在JavaScript的其他领域上NPM都大展身手。即便NPM饱受诟病，但它仍为Node.js安装后的默认包管理器。本周任务我们将搭建JavaScript开发环境，熟悉NPM模式的JavaScript开发架构，以及介绍除NPM以外的其他替代方案。NPM的软件包描述文件`package.json`由JSON编写，请提前熟悉JSON的语法。

本周开始我们将学习Golang。Golang作为主流编程语言，其语法简练、便捷的多线程调度深受人们的喜爱。目前Golang在云原生与Web开发领域大展身手。Golang在1.11版本前的包管理机制主要通过GOPATH进行，这对于经常进行破坏性更新的软件包十分脆弱。所幸在1.11版本后Golang推出了Go Module，用于不同的软件包隔离不同的代码库环境，并在1.13版本后默认开启。本周我们也同时简单了解Golang开发环境的搭建，熟悉Go Moudle的开发模式。

## Tasks
### 安装Visual Studio Code
Visual Studio Code为微软开发的一款文本编辑器，其强大的性能与插件系统为VSCode强力赋能。请通过[Visual Studio Code官方网站](code.visualstudio.com)下载。

### 使用PowerShell（仅限操作系统为Windows）
1. 使用不同的命令行处理器，您可以在下列选项中二选一，新手推荐Windows Terminal：
针对Windows Terminal：通过Microsoft Store下载
针对Hyper：通过[hyper.is](https://hyper.is)下载
2. 接下来您就可以享受PowerShell带来的便捷了。请通过[微软官方的PowerShell教程](https://docs.microsoft.com/zh-cn/learn/paths/powershell/)学习PowerShell。请您注意，当教程要求您打开PowerShell时，您可以直接选择打开您事先安装好的命令行处理器。

### 安装WSL（仅限操作系统为Windows 10或以上）
**本教程最低要求版本为Windows 10 2004，若您的操作系统为Windows 8.1及以下操作系统，请使用虚拟机。**
WSL全程Windows Subsystem for Linux，即适用于Linux的Windows子系统，旨在为既有Windows体验上更加便捷的提供Linux开发体验。
请通过[微软官方安装页面](https://docs.microsoft.com/zh-cn/windows/wsl/install "")安装WSL2，**需要注意该网页要求操作系统为Windows 11 或 Windows 10 2004以上**，若为Windows 10的更低版本，请更新。
安装WSL默认的Linux发行版为Ubuntu，请知悉。安装后，请尽快熟悉Linux命令行环境。

### 安装Node.js
虽然JavaScript并不只用于Node.js，但为了使用NPM必须要安装Node.js。
为了JavaScript开发的持续性与稳定性，我们一般会针对一个开发套件安装一个版本管理器，这里我们使用nvm。
#### 针对Windows操作系统
访问[GitHub的nvm-windows项目](https://github.com/coreybutler/nvm-windows/releases "")并安装nvm，然后您就可以在**管理员模式下**PowerShell中使用nvm了。
#### 针对Linux与macOS操作系统
参照[GitHub的nvm项目](https://github.com/nvm-sh/nvm "")中的`README.md`进行安装。
#### 安装最新版与LTS版Node.js
由于`nvm-windows`与`nvm`的命令有所不同，请访问各自的项目主页了解安装命令，要求至少安装最新版与LTS版。
随后您可以通过nvm自由切换Node.js版本
```bash
nvm use <version> # you can run `nvm list` to list installed versions
```
不要忘记更改NPM的镜像，请自行查阅教程修改。
### 熟悉NPM，认识NPM的替代品
#### 熟悉NPM
1. 在命令行中新建一个文件夹，进入该文件夹后输入`npm init`
2. 按照npm的指示输入信息
3. 您的第一个npm软件包构建完毕，现在请您在该文件夹中创建文件`index.js`，文件内容如下：
```javascript
	console.log('hello, world!')
```
4. **使用代码编辑器**打开`package.json`，在`scripts`中添加`"start": "node index.js"`。注意：根据JSON语法，您应该在`test`对应一行最后添加一个半角逗号。
5. 在命令行输入`npm start`，查看效果
6. 您也可以在该文件夹中新建Git仓库进行版本管理。

#### 认识NPM的替代品
1. 使用Git clone仓库`https://github.com/zeithrold/to-do`
2. 进入文件夹后输入以下命令
针对Linux(WSL)、macOS:`/usr/bin/time -a -o time_npm.txt npm install`
针对PowerShell: `Measure-Command { npm install | Out-Default } > time_npm.txt`
3. 现在删除`node_modules`文件夹与`package-lock.json`文件
4. 安装Yarn或pnpm，您可以在[Yarn官方网站](https://yarnpkg.com/getting-started/install)或[pnpm官方网站](https://pnpm.io/zh/installation "")查找安装步骤。
5. 使用您安装好的包管理器重复install操作，输入以下命令
	 - yarn: `/usr/bin/time -a -o time_alter.txt yarn`(Linux(WSL), macOS), `Measure-Command { yarn | Out-Default } > time_alter.txt`(Powershell)
	 - pnpm: `/usr/bin/time -a -o time_alter.txt pnpm install`(Linux(WSL), macOS), `Measure-Command { pnpm install | Out-Default } > time_alter.txt`(PowerShell)
6. 打开`time_npm.txt`与`time_alter.txt`，比较速度。

### 安装Golang并配置环境
1. 访问[Golang官方网站](https://go.dev "")下载Golang，根据操作系统不同安装方法也存在不同。
2. 修改您的环境变量：
Linux(WSL), macOS: 修改文件`.bash_profile`或其他等效文件，添加一行`export GOPROXY=https://proxy.golang.com.cn,direct`
Windows: 按下`Win+S`快捷键，键入高级系统设置，点击左下角环境变量按钮，在用户变量上新建变量，变量名为`GOPROXY`,值为`https://proxy.golang.com.cn,direct`

至此，Golang环境配置完毕，现在进行简单的Go Module测试，请访问[Golang网站](https://go.dev/doc/tutorial/getting-started "")完成任务至*Call code in an external package*教程。


## Assessments
 - 安装Visual Studio Code: 不做要求
 - 使用PowerShell: 在微软学习网站上登录自己的Microsoft帐户，学习*PowerShell 简介*后，点击右上角头像-配置文件，在配置文件页面左侧点击*培训*，截图上传您的学习记录，**要求截图必须包含您的Microsoft 账号信息与*Introduction to scripting in PowerShell*的学习记录**
 - 安装WSL：输入命令`grep Microsoft /proc/version`并截图上传
 - 安装Node.js：输入命令`nvm list`并截图上传，**要求必须安装LTS与Latest两个版本**
 - 熟悉NPM：截图上传`npm start`的运行效果
 - 认识NPM的替代品：上传`time_npm.txt`文件与`time_alter.txt`文件
 - 安装Golang并配置环境：将`go run .`运行效果截图后上传

[^1]: IDC 2018数据
