# Git

## 什么是Git?
  - Git是一款源代码管理工具(版本控制工具)
    - 我们写的代码需要使用Git进行管理。
  - 源代码有必要管理起吗？
  - 1.0
  - 2.0 // 
  - svn,vss,vcs.... git
  - 有必要，因为人工的去处理不同的版本，做相应备份会很麻烦。
  - Git是linux之父当年为了维护linux---linus之前也是手动维护合并把文件发给Linus
  - linus自己写了一个版本管理的工具(Git)

## Git安装

## 初始化Git仓储/(仓库)
- 这个仓库会存放，git对我们项目代码进行备份的文件
- 在项目目录右键打开 git bash
- 命令: `git init`


## 自报家门
- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者的信息存储起来
- 命令: 
    + 配置用户名:`git config --global user.name "xiaoming"`
    + 配置邮箱:  `git config --global user.email "xm@sina.com"`


## 把代码存储到.git仓储中
- 1.把代码放到仓储的门口
    + `git add ./readme.md` 所指定的文件放到大门口
    + `git add ./` 把所有的修改的文件添加到大门口
- 2.把仓储门口的代码放到里面的房间中去
    + `git commit -m "这是对这次添加的东西的说明" `

## 可以一次性把我们修改的代码放到房间里(版本库)
- `git commit --all -m "一些说明"`
    + --all 表示是把所有修改的文件提交到版本库

## 查看当前的状态
- 可以用来查看当前代码有没有被放到仓储中去
- 命令: `git status`

## git中的忽略文件
- .gitignore,在这个文件中可以设置要被忽略的文件或者目录。
- 被忽略的文件不会被提交仓储里去.
- 在.gitignore中可以书写要被忽略的文件的路径，以/开头，
    一行写一个路径，这些路径所对应的文件都会被忽略，
    不会被提交到仓储中
    + 写法
        * ` /.idea  ` 会忽略.idea文件
        * ` /js`      会忽略js目录里的所有文件
        * ` /js/*.js` 会忽略js目录下所有js文件

## 查看日志
- `git log` 查看历史提交的日志
- `git log --oneline` 可以看到简洁版的日志

## 回退到指定的版本
- `git reset --hard Head~0`
    + 表示回退到上一次代码提交时的状态
- `git reset --hard Head~1`
    + 表示回退到上上次代码提交时的状态

- `git reset --hard [版本号]`
    + 可以通过版本号精确的回退到某一次提交时的状态

- `git reflog`
  + 可以看到每一次切换版本的记录:可以看到所有提交的版本号

## 分支
- 默认是有一个主分支master

### 创建分支
- `git branch dev`
    + 创建了一个dev分支
    + 在刚创建时dev分支里的东西和master分支里的东西是一样的
    + 切换到新分支：`git checkout dev`
    + 然后，上面两个命令也可以合成为一个命令，创建一个并切换到新分支：
      `git checkout -b dev`  
    + `git branch` 可以查看当前有哪些分支


### 合并分支
- `git merge dev`
    + 合并分支内容,把当前分支与指定的分支(dev),进行合并
    + 当前分支指的是`git branch`命令输出的前面有*号的分支
- 合并时如果有冲突，需要手动去处理，处理后还需要再提交一次.
- `git merge –-no-ff` 可以保存你之前的分支历史。能够更好的查看 merge历史，以及branch 状态。
- `git merge` 则不会显示 feature，只保留单条分支记录。

### 提交代码到github(当作git服务器来用)
- `git push [地址] master`
 + 示例: `git push https://github.com/huoqishi/test112.git master  master`
 + 会把当前分支的内容上传到远程的master分支上

 - `git pull [地址] master`
 + 示例: `git pull https://github.com/huoqishi/test112.git master`
 - `git clone [地址]` 
 + 远程桌面地址 
 - `git remote add origin [远程仓库地址]`
 + push到远程桌面 
 - `git push -u origin master `
 + 查看本地添加了哪些远程地址
 - `git remote -v`
 + 删除本地指定的远程地址
 - `git remote remove origin`
 ## git pull 与 git clone
 + 从远程服务器克隆一个一模一样的版本库到本地,复制的是整个版本库，叫做clone.
 + 从远程服务器获取到一个branch分支的更新到本地，并更新本地库，叫做pull.
 
 ```
 git remote add origin [地址]
 git checkout -b dev
 git checkout -b setData
 git status 
 git add ./
 git commit -m "xx"
 git checkout dev
 git merge setData --no-ff
 :q
 git push origin dev
删除本地分支： git branch -d setData
 git checkout master
 git pull origin master
 git merge dev
 git status
 git push origin master

 
 ```
