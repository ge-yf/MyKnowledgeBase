# Git

## TLDR(Too Long; Didn't Read.) 
在使用Git的过程中，最好养成如下习惯：

1. 随时使用 `git status` ！
2. 只更改那些真正想更改的文件。
3. `git add .` 会是你真正的朋友。
4. 随时使用命令 `git commit -m "meaningful messages"`。
5. 在`push`前先`fetch`, `pull`。
6. 最后， `git push`推送提交的更改。

## command

### git checkout 
    git checkout -- fileName
恢复单个文件

### git reset
    git reset --hard
恢复当前目录中的所有文件（抛弃自上次提交以来的所有更改）

### git log
    git log -G"你要查找的文本内容" -p 
搜索提交内容，其中：-G 是查正则的，想要查文本用 -S


### git stash


#### 生成和使用patch ####

获取修改前和修改后文件的两种方法：

1. `git stash`备份当前工作区内容，将工作区恢复到上一次提交的状态，同时将当前工作区内容保存到Git栈中。  -> 取得变更前文件。

	`git stash pop`将暂存的内容恢复到工作区， 取得变更后的文件。  -> 取得变更后文件。

2. 有时候修改完代码后，不想马上提交，可以另外建立一个分支，在这个分支上提交，结束之后再切回原来的分支。
	`git checkout -b name`


**UNIX下的patch**

 	`git diff  > patch`
    `git diff  --cached > patch`
    `git diff  branchname --cached > patch`

以上3中方法都能生成一个unix风格的patch文件。

在应用时， 使用`git apply patch`来应用patch。

**Git patch**

打patch:

    'git format-patch -s [Hash code]'
    'git format-patch HEAD^ <==最近的1次commit的patch'
    'git format-patch HEAD^^ <==最近的2次commit的patch'
    'git format-patch HEAD^ <==最近的3次commit的patch'
    'git format-patch HEAD^ <==最近的4次commit的patch'

应用patch:

    git am [patch名]

#### 暂存不想提交的代码 ####

$git stash
$do some work
$git stash pop

进阶:
git stash          # save uncommitted changes
# pull, edit, etc.
git stash list     # list stashed changes in this git
git show stash@{0} # see the last stash 
git stash pop      # apply last stash and remove it from the list

git stash --help   # for more info

git stash clear	   # clear the stash stack

#### 配置difftool ####

// 将difftool修改为beyond compare
git  config  --global   diff.tool   bc

// 取消每次的提示
git  config  --global  difftool.prompt  false


#### 删除untracked files ####
#删除 untracked files
git clean -f
 
#连 untracked 的目录也一起删掉
git clean -fd
 
#连 gitignore 的untrack 文件/目录也一起删掉 （慎用，一般这个是用来删掉编译出来的 .o之类的文件用的）
git clean -xfd
 
#在用上述 git clean 前，墙裂建议加上 -n 参数来先看看会删掉哪些文件，防止重要文件被误删
git clean -nxfd
git clean -nf
git clean -nfd




## Git error: Encountered 7 file(s) that should have been pointers, but weren't
解决方法：
```
git rm --cached -r .
git reset --hard
git rm .gitattributes
git reset .
git checkout .
```
