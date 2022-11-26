# Git的使用与合作（活动）

## 材料

- 电脑

- 能上github的网络
- github账号
- Git安装包（建议准备）
- Vscode

## 介绍

> GitHub以及git的使用是开发者必备的技能

背景：在没有git的情况下，我们的项目开发会使用文件夹的方式管理，比如

```
project/项目1/
porject/项目备份/
porject/废案/
……
```

缺点：

- 不简洁
- 管理困难
- 合作困难
  - 每次传输都要压缩
  - 并行开发的话，合并的时候很麻烦
  - ……

### Git

git的一个项目管理工具，能进行分支化的管理，和GitHub一起用效果非常好

（git的结构）

![图片](https://mmbiz.qpic.cn/mmbiz_png/uJDAUKrGC7Ksu8UlITwMlbX3kMGtZ9p0AII6YVooUzibpibzJnoOHHXUsL3f9DqA4horUibfcpEZ88Oyf2gQQNR6w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

git是一个分布式版本控制工具，其最大的2个特点是**分布式**和**版本管理**

分布式: 每个点（远程和本地）都存放了完整的项目代码

版本管理: 使用分支进行版本管理

### GitHub

GitHub是一个面向开源及私有软件项目的托管平台，因为只支持Git作为唯一的版本库格式进行托管，故名GitHub

GitHub上面有：

- 许多非常优秀的开源项目
- 各种教程，工具
- 由社区维护的各种项目（基于GitHub特别的贡献机制request）

你可以用GitHub来：

- 存放/管理你自己的项目（现在可能还体会不到）
- 存放笔记
- 找优秀的项目学习
- ……

奇怪的项目举例：

- 整活：https://github.com/itorr/sojo

- 程序员做饭指南：https://github.com/Anduin2017/HowToCook

- 全国各省市烂尾楼停贷断供通知汇总：https://github.com/WeNeedHome/SummaryOfLoanSuspension
- QQBot：https://github.com/takayama-lily/oicq

## 今日的任务

- 在GitHub上：
  - 建一个自己的笔记仓库
  - 建一个C++公共仓库
    - 每个人提交本周的C++作业
  - 向公共库提交申请
    - 仓库地址：https://github.com/Truraly/common-problem-in-C
    - 添加一条C++错误的处理

（如果使用自己已有的文件，记得先做好备份）

## 任务点

> 怎么有程序员没有梯子的（？）

### 环境

- 安装git

  - 感觉不错的安装教程：https://blog.csdn.net/mukes/article/details/115693833

    > 其实一路默认就行

  - 安装完菜单栏有三个软件：

    - Git Bash：Unix与Linux风格的命令行，使用最多，推荐最多
    - Git CMD：Windows风格的命令
    - Git GUI：图形界面的Git，不建议初学者使用，尽量先熟悉常用命令

  - 当然今天我们不用这三个操作界面，而是和vscode的git插件搭配使用vscode的界面

  - git用户初始化（打开终端）

    ```
    git config --global user.email "邮箱"
    git config --global user.name "用户名（随便取）"  
    ```

- 使用vscode
  
  - 插件
    - Git Graph
    - git插件（如果使用git的时候vscode弹出窗口，直接装就行）
  - 操作快捷键
    - 文件快捷键：`Ctrl`+`K`+`O`
    - 终端快捷键：`Ctrl`+`J`
    - 保存快捷键：`Ctrl`+`S`

### 获取第一个仓库

> git有非常多的操作，整体结构其实很复杂，这里只取部分重要操作，

- `git init`

  - （增加一些文件，比如一份git笔记）
  - 填写第一次提交消息（initial push）
  - commit&push（登录github并选择新建一个私有库）
  - 增加一些笔记，新建一个文件，然后commit&push

  - `.gitignore`文件

    ```
    #为注释
    *.txt        #忽略所有 .txt结尾的文件,这样的话上传就不会被选中！
    !lib.txt     #但lib.txt除外
    /temp        #仅忽略项目根目录下的TODO文件,不包括其它目录
    tempbuild/       #忽略build/目录下的所有文件
    doc/*.txt    #会忽略 doc/notes.txt 但不包括 doc/server/arch.txt
    ```
  
  - 删除本地的文件
  - 重新克隆一份


- 分支

  - 新建一个分支

    ```
    # 新建一个分支，但依然停留在当前分支
    git branch [branch-name]
    
    # 新建一个分支，并切换到该分支
    git checkout -b [branch]
    ```

  - 切换分支

    ```
    # 列出所有本地分支
    git branch
    
    # 列出所有远程分支
    git branch -r
    
    # 切换到指定分支并更新工作目录(working directory)
    $ git switch -c [branch-name]
    ```

  - 修改东西

  - 合并分支

    ```
    # 合并指定分支到当前分支
    $ git merge [branch]
    ```
    
  
- 合作

  > 程序员的好习惯：先pull再写代码
  
  - 创建初始项目
  - 添加权限
  - clone
  - 添加文件
  - 提交
  
- 向公共库提交申请
  
  - 添加一条C++错误的处理

### 选做

- git移动版
- 使用GitHub的codespace

## 课外材料

github上git教程https://github.com/geeeeeeeeek/git-recipes

Git备忘清单https://training.github.com/downloads/zh_CN/github-git-cheat-sheet/

狂神的Git课https://www.bilibili.com/video/BV1FE411P7B3?p=14&spm_id_from=333.999.header_right.history_list.click

狂神的Git笔记https://mp.weixin.qq.com/s/Bf7uVhGiu47uOELjmC5uXQ

