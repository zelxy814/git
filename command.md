## npm install X:
- 会把X包安装到node_modules目录中, 安装模块到项目目录
- 不会修改package.json
- 之后运行npm install命令时，不会自动安装X
## npm install X –save:
- 会把X包安装到node_modules目录中
- 会在package.json的dependencies属性下添加X
- 之后运行npm install命令时，会自动安装X到node_modules目录中
- 之后运行npm install 
- –production或者注明NODE_ENV变量值为production时，会自动安装msbuild到node_modules目录中
## npm install X –save-dev:
- 会把X包安装到node_modules目录中
- 会在package.json的devDependencies属性下添加X
- 之后运行npm install命令时，会自动安装X到node_modules目录中
- 之后运行npm install 
- –production或者注明NODE_ENV变量值为production时，不会自动安装X到node_modules目录中
## window命令与mac命令
+ 在mac系统下的terminal和window系统下的cmd的命令是不通用的，可以使用PowerShell和下载Cmder  
+ `"pwd"(print working directory)`会得到当前的全路径信息
+ `"cd"(change directory)`改变当前路径，`.`当前路径，`..`上级路径。
+ `ls`查看当前文件夹下拥有哪些文件及文件夹。`ls -a`展示所有文件（包含隐藏文件），`ls -l`展示更多文件信息。
+ `mkdir` 在当前路径下创建新的文件夹
+ `touch`在当前路径下创建一个文件类型，`touch test.txt`
+ `mv` 做两件事，一个是移动文件，另一个重命名。重命名：`mv test.txt goat.txt`，移动后面跟的是路径`mv goat.txt ../`
+ `rm` 实现删除文件，删除后垃圾箱内不会存在，从系统中删除，也可以删除多个文件。`rm test.txt goet.txt`
+ `rmdir` 实现删除空的文件夹
+ `rm -r` 实现删除文件夹
+ `rm -f` 实现强制删除
+ `rm -rf` 强制删除，无法找回
