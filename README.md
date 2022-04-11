# 網頁版 https://yuchenmvc.github.io/LearnGit/

<br>

# Conventional Commits 

<br>

## Standard
```
<type>: [subject]

[description]

[issue number]
```

<br>

## Illustrations

`type 種類`
> feat 新增擴充
\
> fix 修補
\
> docs 文件
\
> style 格式
\
> refactor 重構
\
> perf 效能最佳化
\
> test 測試功能
\
> build 建置系統
\
> ci 自動化CI/CD
\
> revert 回復commit

`subject` 
> 總結你做了什麼

`description` 
> 詳述為什麼修改及變動修改的原因

`issue` 
> 如果有 填寫issue編號

\
~~不一定要照這樣 跟RESTful一樣是種規範~~

<br>

## Example of use

```
feat: UploadFileController上傳檔案功能

客戶需求:
1.客戶打來要求 需求常改來改去
2.PM反應客戶要上傳速度快一點 不然每次批次檔都要等很久

調整項目:
1.應應快速需求對Controller與Service解耦合
2.Controller邏輯IFormFile改用Collection<T>解一次讀取多個檔案

issue #200
```

<br>


# Basic Git Commands

<br>

# `git version`
查看目前git安裝版本
```git
$ git version
```
查看git詳細安裝資訊
```git
$ git version --build-options
```

<br>

# `git config`
設定名稱與信箱 (字串中內容為範例)
```git
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
查看config內容
```git
$ git config --list
```

<br>

# `git init`
初始化git (會在該目錄資料夾建立Repository)
```git
$ git init
```

<br>

# `git status`
查看目前git狀態
```git
$ git status
```
查看目前git分支狀態
```git
$ git status --b
```
查看目前有哪些untracked檔案
```git
$ git status --untracked-files
```

<br>

# `git add`
加入變動檔案
```git
$ git add Example.cs
```
一次加入全部(請先設定.gitignore)
<br>
⚠️團隊合作pull時會影響到他人IDE環境,除非知道自己在幹嘛
```git
$ git add --all
```

<br>

# `git commit`
提交變更
```git
$ git commit -m "這串是github或gitlab上會顯示的commit訊息"
```
直接add commit(不建議,重傳要rebase有點麻煩)
<br>
個人習慣先add暫存再commit,有個緩衝空間
```git
$ git commit -a -m "內容"
```

<br>

# `git log`
查看commit提交紀錄
```git
$ git log
```
簡易版
```git
$ git log --oneline
```
查看分支圖
```git
$ git log --oneline --graph
```

<br>

# `git diff`
查看差異(建議GUI比較方便)
```git
$ git diff [commit1] [commit2]
```

<br>

# `git reset`
重設目前commit位置至指定commit位置(HEAD^表示目前所在分支的前一個commit)
```git
$ git reset --hard HEAD^
```

<br>

# `git branch`
切出新分支(會從當下位置分支出來)
```git
$ git branch [newBranchName]
```
查看所有分支
```git
$ git branch
```

<br>

# `git checkout`
切換分支位置
<br>
<br>
切換到原本master分支
```git
$ git checkout master
```
再切換回剛剛新分支
```git
$ git checkout [newBranchName]
```

<br>

# `git merge`
合併分支
<br><br>
假定我們在master分支, 要合併[newBranchName]分支
```git
$ git merge [newBranchName]
```

<br>

# `git conflict`
分支衝突
```git
//TODO: 最刺激的部分 待動工
```

<br>

# `git push`
推送commit至Github或Gitlab
```git
$ git remote add origin https://github.com/[name]/[repo].git
$ git push origin [branchName]
```

<br>

# `git pull`
拉commit至local端
```git
$ git pull origin [BranchName]
```
pull request
```git
//TODO: 待動工
```

<br>

# `git clone`
下載repository
```git
$ git clone https://github.com/[name]/[repo].git
```

<br><br>

## Resources
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)\
[Contributing to Angular](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type)
