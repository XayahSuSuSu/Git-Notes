# Git-Notes

1.删除Commit(n为向前删除的Commit次数):

	1)本地删除Commit记录
	git reset --hard HEAD^n

	2）向远程仓库提交强制申请
	git push origin HEAD -f

2.从其他远程仓库导入项目

	1)首先将导入仓库克隆到本地
	git clone <gitUrl(导入仓库)>

	2)cd 到该项目根目录

	3)将该项目强制导入到被导入项目
	git push --mirror <gitUrl(被导入仓库)>

3.导入其他仓库的Commit记录

	1)cd 到被导入项目根目录

	2)将该库加为远程仓库
	git remote add target <gitUrl(导入仓库)>

	3)将远程代码抓取到本地
	git fetch target

	4)使用cherry-pick命令提交转移
	git cherry-pick <commitHash>

4.修改最新的一条Commit记录信息

	1)cd 到被导入项目根目录

	2)git commit --amend

	3)输入i进入插入模式

	4)修改Commit记录信息

	5)按Esc退出

	6)输入:wq保存

	7)git push -f
