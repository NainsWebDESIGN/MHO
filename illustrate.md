# 情境說明

## 專案目標

架設 **MHO 遊戲資料網站**（查表／圖鑑類），資料以 **JSON** 為主、**暫不放圖片**；資料內容晚點再建立。希望 **不花錢** 上線。

Repo：`https://github.com/NainsWebDESIGN/MHO.git`  
預期網址：`https://NainsWebDESIGN.github.io/MHO/`

---

## 架站結論

- **方案：** GitHub Pages（免費、與現有 GitHub repo 最搭）
- **型態：** 靜態前端 + JSON（不必先做後端／資料庫）
- **備選：** Cloudflare Pages、Vercel、Netlify（之後若要換再評估）
- **資料變複雜時再考慮：** Supabase / Firebase（免費額度）

不建議一開始就租 VPS 或上完整後端。

---

## GitHub Pages 用法

### 啟用

1. 開 GitHub repo → **Settings → Pages**
2. Source 選 `Deploy from a branch`
3. Branch 選 `main`，資料夾二選一：
   - `/ (root)`：網站檔放在 repo 根目錄
   - `/docs`：網站檔放在 `docs/`（較乾淨，AI 規則等可留在根目錄）
4. Save 後約 1～2 分鐘生效

### 建議目錄（資料晚點再建也可）

```
index.html          # 或放在 docs/index.html
data/               # 之後放 monsters.json 等
```

### 讀 JSON

- 用相對路徑，例如：`fetch('./data/monsters.json')`
- 網站路徑有 `/MHO/` 前綴，連結與 `fetch` 請用 `./`，避免寫成從網域根目錄開始的絕對路徑

### 更新流程

改檔 → `git add` → `commit` → `push` → Pages 自動更新

---

## 對話中遇過的 Git 問題（本機）

| 現象 | 原因 | 處理 |
|------|------|------|
| `無法辨識 'git'` | 未安裝或未進 PATH | 安裝 Git for Windows，勾選 Add to PATH，重開終端機 |
| commit 失敗：Author identity unknown | 未設 `user.name` / `user.email` | `git config --global user.name` / `user.email` |
| `src refspec main does not match any` | 第一次 commit 失敗，沒有分支可推 | 設好身分後重新 `commit`，再 `push` |
| `remote origin already exists` | origin 已加過 | 不用再加；用 `git remote -v` 確認即可 |

首次推送範例（身分設好之後）：

```powershell
git add README.md
git commit -m "first commit"
git branch -M main
git push -u origin main
```
