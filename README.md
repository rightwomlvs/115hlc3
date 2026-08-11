# 翰林技英 Choice 第三冊 互動教材

使用 `english-html-generator` Skill 產生的課堂互動教材，以 GitHub Pages 靜態發布。

## 目前課次

- **L01 What's in My B.O.B.?**
  - `L01/L01-flashcards.html` — 字卡總覽（點入自動朗讀、KK 音標、Phonics Grid）
  - `L01/L01-SV-challenge.html` — S+V 句型挑戰（分節 Tab、Show Hint、課文動畫）
  - `L01/L01-quiz.html` — 隨堂測驗互動評量（作答、即時計分、四類詳解）
- **L02 Colors Speak Louder than Words**
  - `L02/L02-flashcards.html` — 字卡總覽
  - `L02/L02-SV-challenge.html` — S+V 句型挑戰
  - `L02/L02-quiz.html` — 隨堂測驗互動評量
- **L03 The Necklace**
  - `L03/L03-flashcards.html` — 字卡總覽
  - `L03/L03-SV-challenge.html` — S+V 句型挑戰
  - `L03/L03-quiz.html` — 隨堂測驗互動評量
- **L04 Ask a Lawyer**
  - `L04/L04-flashcards.html` — 字卡總覽
  - `L04/L04-SV-challenge.html` — S+V 句型挑戰
  - `L04/L04-quiz.html` — 隨堂測驗互動評量
- **L05 The Sugar Trap**
  - `L05/L05-flashcards.html` — 字卡總覽
  - `L05/L05-SV-challenge.html` — S+V 句型挑戰
  - `L05/L05-quiz.html` — 隨堂測驗互動評量
- **L06 Getting Paid to Stay at Hotels**
  - `L06/L06-flashcards.html` — 字卡總覽
  - `L06/L06-SV-challenge.html` — S+V 句型挑戰
  - `L06/L06-quiz.html` — 隨堂測驗互動評量

## 課程開放／關閉管理（管理頁）

網站提供 `admin.html` 管理頁（首頁頁尾「🔧 課程管理」進入），可控制各課「隨堂測驗」開放或關閉：

- **關閉時**：首頁該課的「📝 隨堂測驗」按鈕隱藏，直接輸入測驗網址也會顯示「本單元尚未開放」；字卡與 S+V 挑戰維持開放。
- **開放／關閉設定**：存於根目錄 `config.json`（`quizzes` 欄位，`true`＝開放）。首頁與測驗頁都會讀取此檔。

### 第一次使用管理頁

1. 開啟 `https://rightwomlvs.github.io/115hlc3/admin.html`。
2. 建立 **Fine-grained Personal Access Token**（只限本 repo `rightwomlvs/115hlc3`，Repository permissions → **Contents: Read and write**）：
   `https://github.com/settings/personal-access-tokens/new`
3. 將 `github_pat_...` 貼入管理頁，點「儲存並驗證金鑰」。
   - Token 只存在瀏覽器 localStorage，不會寫進網站檔案；可隨時「清除金鑰」。
4. 用開關切換各課開放狀態，點「💾 儲存並發布」。

設定寫回 `config.json` 後，GitHub Actions 自動重建 Pages，約 1 分鐘內生效。

## 發布方式

1. 將新課次資料夾（如 `L02/`）放入本資料夾。
2. 更新 `index.html` 新增連結。
3. commit 並 push 至 GitHub，Pages 即自動更新。
