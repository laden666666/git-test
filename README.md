# 列出git的全部配置信息
```
git config --list
```
		
# 列出git的帮助命令
```
git help
```

# 状态简览
可以查看修改状态
```
git status
```
也可以使用“git status -s”命令或“git status --short”命令，你将得到一种更为紧凑的格式输出。
```
git status -s
``` 

# 实现对指定文件的跟踪，然后执行git commit暂存已修改文件
```
git add xxx
git commit -m 'initial project version'
```

# 暂存已修改文件
Git可以暂存一个已跟踪文件的修改记录，其实只不过暂存了运行“git add”命令时的版本，如果现在提交，提交文件的版本是你最后一次运行“git add”命令时的那个版本，而不是运行“git commit”时，在工作目录中的当前版本。所以，运行了“git add”之后又作了修订的文件，需要重新运行“git add”把最新版本重新暂存起来
```
git add xxx
git commit
```

提交修改， -m表示注释
git clone https://github.com/libgit2/libgit2 mylibgit
克隆资源。 如果后面无名称，会以url末尾路径做资源目录名
git status 			要查看哪些文件处于什么状态