# Git-Common-Command
Git常用命令

<b>初始化本地git仓库（创建新仓库）</b>
<pre>
git init
</pre>

<b>配置用户名</b>
<pre>git config --global user.name "xxx"</pre>

<b>配置邮件</b>
<pre>git config --global user.email "xxx@xxx.com"</pre>

<b>git status等命令自动着色</b>
<pre>git config --global color.ui true
git config --global color.status auto
git config --global color.diff auto
git config --global color.branch auto
git config --global color.interactive auto</pre>

<b>clone远程仓库</b>
<pre>
git clone git+ssh://git@192.168.53.168/VT.git</pre>

<b>查看当前版本状态（是否修改）</b>
<pre>git status</pre>

<b>添加xyz文件至index</b>
<pre>git add xyz</pre>

<b>增加当前子目录下所有更改过的文件至index</b>
<pre>git add</pre>

<b>提交</b>
<pre>git commit -m 'xxx'</pre>

<b>合并上一次提交（用于反复修改）</b>
<pre>git commit --amend -m 'xxx'</pre>

<b>将add和commit合为一步</b>
<pre>git commit -am 'xxx'</pre>

<b>删除index中的文件</b>
<pre>git rm xxx</pre>

<b>递归删除</b>
<pre>git rm -r *</pre>

<b>显示提交日志</b>
<pre>git log</pre>

<b>显示1行日志 -n为n行</b>
<pre>git log -1</pre>

<b>显示提交日志及相关变动文件</b>
<pre>git log --stat
git log -p -m</pre>

<b>显示某个提交的详细内容</b>
<pre>
git show dfb02e6e4f2f7b573337763e5c0013802e392818</pre>

<b>可只用commitid的前几位</b>
<pre>git show dfb02</pre>

<b>显示HEAD提交日志</b>
<pre>git show HEAD</pre>

<b>显示HEAD的父（上一个版本）的提交日志 ^^为上两个版本 ^5为上5个版本</b>
<pre>git show HEAD^</pre>

<b>显示已存在的tag</b>
<pre>git tag</pre>

<b>增加v2.0的tag</b>
<pre>git tag -a v2.0 -m 'xxx'</pre>

<b>显示v2.0的日志及详细内容</b>
<pre>git show v2.0</pre>

<b>显示v2.0的日志</b>
<pre>git log v2.0</pre>

<b>显示所有未添加至index的变更</b>
<pre>git diff</pre>

<b>显示所有已添加index但还未commit的变更</b>
<pre>git diff --cached</pre>

<b>比较与上一个版本的差异</b>
<pre>git diff HEAD^</pre>

<b>比较与HEAD版本lib目录的差异</b>
<pre>git diff HEAD -- ./lib</pre>

<b>比较远程分支master上有本地分支master上没有的</b>
<pre>git diff origin/master..master</pre>

<b>只显示差异的文件，不显示具体内容</b>
<pre>git diff origin/master..master --stat</pre>

<b>增加远程定义（用于push/pull/fetch）</b>
<pre>git remote add origin git+ssh://git@192.168.53.168/VT.git</pre>

<b>显示本地分支</b>
<pre>git branch</pre>

<b>显示包含提交50089的分支</b>
<pre>git branch --contains 50089</pre>

<b>显示所有分支</b>
<pre>git branch -a</pre>

<b>显示所有原创分支</b>
<pre>git branch -r</pre>

<b>显示所有已合并到当前分支的分支</b>
<pre>git branch --merged</pre>

<b>显示所有未合并到当前分支的分支</b>
<pre>git branch --no-merged</pre>

<b>本地分支改名</b>
<pre>git branch -m master master_copy</pre>

<b>从当前分支创建新分支master_copy并检出</b>
<pre>git checkout -b master_copy</pre>

<b>上面的完整版</b>
<pre>git checkout -b master master_copy</pre>

<b>检出已存在的features/performance分支</b>
<pre>git checkout features/performance</pre>

<b>检出远程分支hotfixs/BJVEP933并创建本地跟踪分支</b>
<pre>git checkout --track hotfixs/BJVEP933</pre>

<b>检出版本v2.0</b>
<pre>git checkout v2.0</pre>

<b>从远程分支develop创建新本地分支devel并检出</b>
<pre>git checkout -b devel origin/develop</pre>

<b>合并远程master分支至当前分支</b>
<pre>git merge origin/master</pre>

<b>合并提交ff44785404a8e的修改</b>
<pre>git cherry-pick ff44785404a8e</pre>

<b>将当前分支push到远程master分支</b>
<pre>git push origin master</pre>

<b>删除远程仓库的hotfixs/BJVEP933分支</b>
<pre>git push origin :hotfixs/BJVEP933</pre>

<b>把所有tag推送到远程仓库</b>
<pre>git push --tags</pre>

<b>获取所有远程分支（不更新本地分支，另需merge）</b>
<pre>git fetch</pre>

<b>获取所有原创分支并清除服务器上已删掉的分支</b>
<pre>git fetch --prune</pre>

<b>获取远程分支master并merge到当前分支</b>
<pre>git pull origin master</pre>

<b>重命名文件README为README2</b>
<pre>git mv README README2</pre>

<b>将当前版本重置为HEAD（通常用于merge失败回退）</b>
<pre>git reset --hard HEAD
git rebase</pre>

<b>删除分支hotfixs/BJVEP933（本分支修改已合并到其他分支）</b>
<pre>git branch -d hotfixs/BJVEP933</pre>

<b>强制删除分支hotfixs/BJVEP933</b>
<pre>git branch -D hotfixs/BJVEP933</pre>

<b>列出git index包含的文件</b>
<pre>git ls-files</pre>

<b>图示当前分支历史</b>
<pre>git show-branch</pre>

<b>图示所有分支历史</b>
<pre>git show-branch --all</pre>

<b>显示提交历史对应的文件修改</b>
<pre>git whatchanged</pre>

<b>撤销提交dfb02e6e4f2f7b573337763e5c0013802e392818</b>
<pre>git revert dfb02e6e4f2f7b573337763e5c0013802e392818</pre>

<b>内部命令：显示某个git对象</b>
<pre>git ls-tree HEAD</pre>

<b>内部命令：显示某个ref对于的SHA1 HASH</b>
<pre>git rev-parse v2.0</pre>

<b>显示所有提交，包括孤立节点</b>
<pre>git reflog
git show HEAD@{5}</pre>

<b>显示master分支昨天的状态</b>
<pre>git show master@{yesterday}</pre>

<b>图示提交日志</b>
<pre>git log --pretty=format:'%h %s' --graph
git show HEAD-3
git show -s --pretty=raw 2be7fcb476</pre>

<b>暂存当前修改，将所有置为HEAD状态/b>
<pre>git stash</pre>

<b>查看所有暂存</b>
<pre>git stash list</pre>

<b>参考第一次暂存</b>
<pre>git stash show -p stash@{0}</pre>

<b>应用第一次暂存</b>
<pre>git stash apply stash@{0}</pre>

<b>文件中搜索文本“delete from”</b>
<pre>git grep "delete from"
git grep -e '#define' --and -e SORT_DIRENT
git gc
git fsck</pre>
