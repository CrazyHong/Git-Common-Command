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
