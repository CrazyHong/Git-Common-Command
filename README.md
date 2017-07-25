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

<b></b>
