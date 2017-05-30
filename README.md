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
也可以使用`git status -s`命令或`git status --short`命令，你将得到一种更为紧凑的格式输出。
```
git status -s
``` 

# 实现对指定文件的跟踪，然后执行git commit暂存已修改文件
```
git add xxx
git commit -m 'initial project version'
```

# 暂存已修改文件
Git可以暂存一个已跟踪文件的修改记录，其实只不过暂存了运行`git add`命令时的版本，如果现在提交，提交文件的版本是你最后一次运行`git add`命令时的那个版本，而不是运行`git commit`时，在工作目录中的当前版本。所以，运行了`git add`之后又作了修订的文件，需要重新运行`git add`把最新版本重新暂存起来
```
git add xxx
git commit
```

# 移除文件
要从Git中移除某个文件，就必须要从已跟踪文件清单中移除（确切地说，是从暂存区域移除），然后提交。可以用`git rm`命令完成此项工作，并连带从工作目录中删除指定的文件，这样以后就不会出现在未跟踪文件清单中了。

# 移动文件
运行`git mv`就相当于运行了下面三条命令：
```
mv README.md README
git rm README.md
git add README
```
同时可以使用mv命令实现修改文件名称。不管是直接使用`git mv`还是使用上述三个操作，Git都会意识到这是一次改名，所以不管何种方式结果都一样。两者唯一的区别是，`mv`是一条命令而另一种方式需要三条命令，直接用`git mv`轻便得多。

# 查看已暂存和未暂存的修改
`git diff`命令让你知道当前做的哪些更新还没有暂存，同时也可以知道有哪些更新已经暂存起来准备好了下次提交。
```
git diff
```
不管该命令在windows可能存在问题，显示的代码都是乱码

# 提交修改， -m表示注释
git clone https://github.com/libgit2/libgit2 mylibgit
克隆资源。 如果后面无名称，会以url末尾路径做资源目录名
git status 			要查看哪些文件处于什么状态