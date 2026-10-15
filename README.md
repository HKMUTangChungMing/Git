# Git

This is using Git to upload single large file  !!! ~~~🐺


# 使用 git 來上傳單個容量比較大的檔案


<img width="129" height="59" alt="image-20250322141801164" src="https://github.com/user-attachments/assets/20fa13be-079b-46a9-ab59-029a4b0260a4" />


下載

https://git-scm.com/

## Step 1 : 在當前文件夾，使用CMD。


<img width="482" height="430" alt="image-20250322015554170" src="https://github.com/user-attachments/assets/88a85b37-753b-4b73-a16d-433ffff8d009" />
---

## Step 2 : 進入CMD 後，輸入以下 Command

<img width="686" height="319" alt="image-20250322015631599" src="https://github.com/user-attachments/assets/02761334-d163-4664-beaa-df92ceda8e26" />


````
git init
````

初次化 git。

```
git lfs install
```

為Git 安裝一個擴充工具(LFS)，支援上傳 大型檔案。

```
echo "Library/" >> .gitignore
echo "Logs/" >> .gitignore
echo "obj/" >> .gitignore
echo "Temp/" >> .gitignore
echo "Build/" >> .gitignore
echo ".vs/" >> .gitignore
echo ".vscode/" >> .gitignore
echo "*.csproj" >> .gitignore
echo "*.sln" >> .gitignore
echo "UserSettings/" >> .gitignore
```

關於Unity GAME 的 設定檔，自動避免推送唔必要嘅檔案去 GitHub，並把這些訊息寫進.gitignore。

```
git lfs track "*.psd"
git lfs track "*.png"
git lfs track "*.jpg"
git lfs track "*.fbx"
git lfs track "*.wav"
git lfs track "*.mp3"
git lfs track "*.mp4"
git lfs track "*.avi"
git lfs track "*.unity"
git lfs track "*.prefab"
```

指定要用 LFS 管理咩檔案。

```
git add .
```

`git add .` 係 Git 指令，用嚟將**目前資料夾內（包括子資料夾）**所有已追蹤或未追蹤嘅變動檔案，**加入到 staging area（暫存區）**，準備下一步 `commit`。

```
git commit -m "Initial commit"
```

將已經加到 staging area（暫存區）嘅檔案，正式建立一次 **提交紀錄（commit）**，並加上訊息 `"Initial commit"`。

`git commit` 👉 將你之前 `git add` 嘅檔案「鎖住」變成一個版本紀錄

`-m` 👉 message（訊息）的縮寫

`"Initial commit"` 👉 你寫俾呢次 commit 嘅描述，通常第一次就寫 "Initial commit"

---

## Step 3 : 將本機嘅 Git 倉庫，連接到 GitHub 上嗰個倉庫（remote repository）

<img width="1089" height="844" alt="image-20250322021303469" src="https://github.com/user-attachments/assets/679df1bd-ff95-49c4-8ab5-03640545ff84" />
```
git remote add origin https://github.com/HKMUTangChungMing/hhh.git
git branch -M main
git push -u origin main
```

---

<img width="129" height="59" alt="image-20250322141801164" src="https://github.com/user-attachments/assets/6c0e04d3-6c7a-4d3f-ba29-77e634d19a39" />
