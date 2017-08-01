## 指令部分
* clone an existing repository 克隆现有库
	git clone ssh://user@domain.com/repo.git
* create a new repository 初始化一个新的库
	git init
* changed filed in your working directory 查看更改的工作目录
	git status
* changes to tracked files 追踪被更改文件
	git diff
* add all current changes to the next commit 添加当前所有更改到暂存区等待下一次提交
	git add .
* add some changes in <file> to the next commit 添加某个文件更改到暂存区等待下一次提交
	git add -p <file>
* commit all local changes in tracked files 提交本地所有被追踪的（暂存区）的更改文件
	git commit -a
* commit previously staged changes 提交之前的动作
	git commit
* change the last commit 修改上一次的提交，但不要修改已经发布的提交
	git commit --amend
* show all commit,starting with newest 打印所有提交，由最近的一次开始
	git log
* show changes over time for a specific file 打印某个文件的更改
	git log -p <file>
* who changed what and when in <file> 打印某个文件的具体更改处
	git blame <file>
* list all existing branches 列出所有现有分支
	git branch -av
* switch HEAD branch 切换当前分支
	git checkout <branch>
* create a new branch based on your current HEAD 基于当前分支新建新分支
	git branch <new-branchh>
* create a new tracking branch based on a remote branch 基于某个远程分支新建新分支 
	git checkout --track <remote/branch>
* deletea a lacal branch 删除本地分支
	git branch -d <branch>
* mark the current commit with a tag 用标签标记当前提交
	git tag <tag-name>
* list all currently configured remotes 打印当前所有的远程配置
	git remote -v
* show information about a remote 显示远程仓库信息
	git remote show <remote>
* add new remote repository ,named <remote> 添加新的远程仓库 仓库名 链接
	git remote add <shortname> <url>
* download all changes from <remote>,but don't integrate into HEAD 从远程下载所有文件更改，当不与当前项目合并
	git fetch <remote>
* download changes and directly merge/integrate into HEAD 下载某远程分支的文件更改并直接与当前项目合并
	git pull <remote> <branch>
* publish local changes on a remote 发布本地更改到远程分支
	git push <remote> <branch>
* delete a branch on the remote 删除某个远程分支
	git branch -dr <remote/branch>
* publish your tags 发布你的标签
	git push --tags
* merge <branch> into your current HEAD 合并分支到你的当前项目
	git merge <branch>
* rebase your current HEAD onto <branch>,Don't rebase published commit 变基到你的当前项目的某个分支，但在发布提交时不变基
	git rebase <branch>
* abort a rebase 终止变基
	git rebase --abort
* continue a rebase after resolving conflicts 在解决冲突后继续变基
	git rebase --continue
* use your configured merge tool to solve conflicts 使用你的配置合并工具来解决冲突
	git mergetool
* use your editor to manually solve conflicts and (after resolving) mark file as resolved 使用你的编辑器去手动解决冲突并在解决后标记为已解决
	git add <resolved-file> //开始手动解决
	git rm <resolved-file> //已解决
* discard all local changes in your working directory 在工作目录中丢弃所有的本地更改文件
	git reset --hard HEAD
* discard local changes in a specific file 在某个文件夹中丢弃该文件夹内所有本地更改文件
	git checkout HEAD <file>
* revert a commit (by producing a new commit with contrary changes) 回复一个提交（在产生一个与文件更改相反的提交时）
	git revert <commit>
* reset your HEAD pointer to a previous commit 回滚你的项目代码到某次提交时的状态
...and discard all changes since then 并丢弃之后的所有更改
	git reset --hard <commit>
...and preserve all changes as unstaged changes 并保存所有非阶段改变的更改
	git reset <cmmit> 
...and preserve uncommitted local changes 并保存未提交的本地更改
	git reset --keep <commit>