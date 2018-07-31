# git基本操作
```shell
$ git config -l	//查看配置信息  
$ git config --global user.name "sophotomato"	//设置全局user name  
$ git config --global user.email johndoe@example.com  
```
## git仓库初始化
```shell
$ git init
```

## 添加跟踪文件，并提交
```shell
$ git add *.c
$ git add README
$ git commit -m 'initial project version'
```
注:commit提交add内容，包括文件修改和新添加的跟踪文件

## 仓库clone
```shell
$ git clone git://github.com/sophotomato/SNotes.git
```

## 检查当前文件状态
```shell
$ git status
```

## .gitignore格式规范
所有空行或者以注释符号 ＃ 开头的行都会被 Git 忽略。  
可以使用标准的 glob 模式匹配。  
匹配模式最后跟反斜杠（/）说明要忽略的是目录。  
要忽略指定模式以外的文件或目录，可以在模式前加上惊叹号（!）取反。  

## 比较已暂存(git add)和未暂存的内容
```shell
$ git diff
```

## 比较暂存和提交的内容
```shell
$ git diff --cached
$ git diff --staged	//git 1.6.1 or 更改版本
```

## 跳过暂存区提交
```shell
$ git commit -a
```

## 移除文件
## 移除删除的文件（以后再也不跟踪这个文件了）
```shell
$ git rm <filename>
```
## 移除add的文件
```shell
$ git rm --cached <filename>
```

## 移动文件
```shell
$ git mv README.txt README
```

## 查看提交历史
```shell
$ git log
```
### 常用 -p 选项展开显示每次提交的内容差异，用 -2 则仅显示最近的两次更新
```shell
$ git log -p -2
```

# 远程仓库
## 要查看当前配置有哪些远程仓库
```shell
$ git remote
```

## 添加远程仓库
```shell
$ git remote add test git://github.com/SNotes.git
```
## 获取仓库数据
```shell
$ git fetch test
```
## 推送数据到远程仓库
```shell
$ git push test master<branch-name>
```
## 远程仓库的删除和重命名
```shell
$ git remote rename test newtest
```

# branch 相关内容
## 新建branch
```shell
$ git branch testing
```

##### HEAD 指向当前所在的分支
## 切换分支
```shell
$ git checkout testing
```
## 删除分支
```shell
$ git branch -d testing
```

## REFERENCE
For more details see [Git](https://git-scm.com/book/zh/v1/%E8%B5%B7%E6%AD%A5).