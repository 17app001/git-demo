# GIT-DEMO

- 版本檢視
	- git --version	

- 設定使用者資訊 
	- git config --global user.name "jerry"
	- git config --global user.email "jerry@gmail.com"


- git設定資訊
	- git config --list

- 切換目錄 cd(Change Directory)
	- cd\
		- 切換到根目錄
	- cd d:\
		- 切換對應的槽別
	- cd cd C:\Users\USER\Desktop\django\GIT\demo
		- 切換對應的Floder


- 初始本地倉庫
	- git init (初始化)

- 檢視目前狀態
	- git status
		- Untracked (未控管)

- 加入控管
	- git add <filename>
		- Untracked -> Added(加入)
		- Added -> Modified(修改)

	- 四種狀態
		- U->A->M
		- D

	- 以文字檔為主

	- git add .
		- 將所有未加入跟變動一次確認

- 修改後確認
	- M->A (git add filename)


- 新增忽略檔案
	- .gitignore  (檔案名稱)
		-*.jpg
		-.vscode/


- 恢復編輯的上一個動作
	- git checkout .


- 恢復刪除後的檔案
	- git restore <filename>
		- git restore . (恢復所有未確認刪除的檔案)
	

- 查找控管檔案
	- git ls-files -s


- 檢視object內容物
	- git cat-file -t sha-1
		- t (型態(blob))
		- p (內容)


- 正式儲存到倉庫區
	- git commit -m "message"
		     -am  =>add+message

	- git commit --amend
			- 合併上一次commit 
			- vim
				- i(insert)
				- esc (切換命令列)
				- :wq (寫入後離開)				


- 檢視目前幾個commit 
	- git log
		- q(強制離開)
	- git log --oneline
		- 每個commit(縮成一行檢視)

	

- git cat-file -p commit-sha1
	- git cat-file -p tree-sha1
	

- git rm -f  
	- 檔案在暫存區
		- 完整刪除
	- 檔案在倉庫區(曾經git commit)
		- 刪除
			- git add (確認刪除)
		- 恢復
			- git restore --staged (暫存區)
				- git add (確認刪除)
				- git restore (恢復)	
	
- git rm --cached <filename> 
	- 暫存/倉庫區檔案
		- 移回工作目錄(不控管)

- git branch(分支指令)
	- master(預設)
	- git branch 
		- 分支列表
	- git branch <branch-name>
		- 新增分支
	
- git checkout(切換分支)
	- git checkout <branch-name>
		- -b(切換跟產生分支)

	- git checkout -commit(sha1)

- git merge(分支合併)
	- 通常是master合併其他分支
	- 切換git checkout master
		- git merge test

	- 合併發生衝突
		- 選擇以哪個分支(current/incoming/both)
		- git merge abort 
			- 取消合併

- git branch -D <branch-name>
	- 刪除分支(-D，直接刪除)


- git reset 
	- 重置指令
	- git reset commit(sha1) 
	- git reset --soft commit(sha1) 
	- git reset --hard commit(sha1) 
	- 反悔reset
		- git reset ORIG_HEAD
		
		
- git reflog
	- 查找過往的commit紀錄
		- git reset commit(sha1) 

- git checkout HEAD
	- HEAD~1(前幾個分支）



- vscode
	- ctrl+shift+p
	- 更改預設terminal
		- 搜尋　default(改成cmd)

	- cls
		- 清空terminal

- github

- 加入遠端倉庫
	- git remote add origin https://github.com/17app001/git-demo.git


- git remote -v
	- 顯示目前連結的遠端倉庫

- git push -u origin master
	- 從本地推送到遠端(第一次需要建立遠端的分支名稱)

- git push 
	- git push -f 
		- 強制更新到遠端(不管衝突)

- git clone
	- git clone https://github.com/17app001/git-demo.git
	- 複製專案到本地端
	- 本地端新增修正後	
		- git add .
		- git commit -m "message"
		- git push (確保遠端永遠最新)	

- git pull
	- 從遠端同步到本地端
		- 開啟專案後的的第一步

- git push --delete origin dev
	- 刪除遠端分支的方法

## GIT Respository
- echo "# git-demo" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M master
- git remote add origin https://- - github.com/17app001/git-demo.git
- git push -u origin master
	
	

