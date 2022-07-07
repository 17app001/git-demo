### 版本號
	- git --version

### 設定全域參數
	- git config --global user.name jerry
	- git config --global user.email jerry@gmail.com


### 目前設定值
	- git config --list


### 初始倉庫
	- git init (.git)

### 檢視狀態
	- git status

### 加入檔案
	- git add <filename>
	- git add . (一次將有變更的檔案確認)

### 查看object內容
	- git cat-file -s sha1
		- s (size)
		- p (內容)
		- t (型態)

### 查看暫存區控管的檔案
	- git ls-files 
	- git ls-files -s 
		- 查看完整資訊

### 修改後 A==>M (M==>D)
	- git add <filename>
		- 確定修改(刪除)
	- git restore <filename>
		- 反悔修改

### 儲存至倉庫區
	- git commit -am "memo"



### 檢視commit的紀錄
	- git log
	- git log --oneline(一行輸出)


### 修改上一次的commit紀錄
	- git commit --amend
		- 開啟vim (i:insert  esc==> :wq)


### 手動刪除(暫存區/倉庫區)
	- git restore <filename> 
		- 恢復
	- git add <filename>
		- 確認
		- git restore --staged <filename>
			- 恢復到手動刪除狀態

### 倉庫區的刪除
	- 手動同上
	- git rm
		- git commit 確認刪除
		- git restore --staged <filename>
			- 恢復到刪除狀態
				- git restore <filename> 
					- 恢復
				- git add <filename>
					- 確認


### 暫存/倉庫移除到工作區 
	- git rm --cached <filename>


### 檢視目前分支
	- git branch
	- 產生新分支
		- git branch <branch-name> 
	- 切換分支
		- git checkout <branch-name>


### 分支的產生(測試/修正)
	- git checkout master

	- 刪除
		- git branch -D <branch-name>

	- 合併
		- git merge test
		
	- 切換/新增一次到位
		- git checkout -b dev (常用)

	- 更改branch name
		- git branch -m old_name new_name


### git checkout 切換指令	
	- 切換分支 
		- git checkout branch-name

	- 切換commit-object 
		- git checkout commit-object
		
	- 迷路了?
		- git checkout master


### 回到過去修改
	- 產生新分支
		- git checkout -b <branch-name>
	- 修正/新增/刪除
		- git add .
		- git commit -am "note"
	
	- 切回主分支
		- git checkout master

	- 進行合併(如果需要)
		- git merge dev

	- 合併的衝突處理 
		- 以原本為主
		- 以新增為主
		- 兩個都保留

	- git add .
	- git commit -am "note"
	- git branch -D <branch-name>
	

### 觀看目前所有commit-object
	- git reflog
	- 方便切換任一個commit-object之上



### 實際上真的回到某一個commit-object
	- git reset commit-object
		- 保留新增檔案工作目錄(暫存區)
	- git reset --soft commit-object
		- 保留新增檔案在暫存區
	- git reset --hard commit-object
		- 刪除後面新增的檔案


### 快速切換HEAD	
	- git reset --hard HEAD
	- git reset --hard HEAD~1
	- git reset --hard ORIG_HEAD 
	- git reset --hard commit-object

### 綁定遠端的URL
	- git remote add origin https://github.com/17app001/git-demo.git
	- git remote -v
		- 檢視遠端的url


### 第一次同步分支
	- git push -u origin master
		- git push
	- git push -u origin dev

### 強制更新
	- git commit --amend (更新上一條的commit)
	- git push -f (force)
	

### 遠端同步近端
	- git pull 


### 新修改反悔
	- git checkout .

### 完整複製專案
	- git clone https://github.com/17app001/git-demo.git

###　git remote –v
	- 檢視遠端url



### MARKDOWN
	- https://www.mdeditor.tw/


