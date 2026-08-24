# Jeju Trip 2026

濟州島 5 天 4 夜自駕行程頁（2026/09/02 – 09/06）

## 檔案

```
Jeju_Trip_2026/
├── index.html    ← 行程頁本體（單一檔案，含 CSS 與 JS）
├── .nojekyll     ← 讓 GitHub Pages 直接輸出靜態檔
└── README.md
```

## 本機預覽

把資料夾放到桌面後，直接用瀏覽器打開 `index.html` 即可。

或用終端機起一個本機伺服器：

```bash
cd ~/Desktop/Jeju_Trip_2026
python3 -m http.server 8000
# 瀏覽器開 http://localhost:8000
```

## 發布到 GitHub Pages

1. 在 GitHub 建立新的 repository，例如 `Jeju_Trip_2026`
2. 在本機資料夾內執行：

```bash
cd ~/Desktop/Jeju_Trip_2026
git init
git add .
git commit -m "濟州島行程頁"
git branch -M main
git remote add origin https://github.com/<你的帳號>/Jeju_Trip_2026.git
git push -u origin main
```

3. 到 repo 的 **Settings → Pages**，Source 選 `Deploy from a branch`，
   branch 選 `main`、資料夾選 `/ (root)`，儲存。
4. 約一分鐘後即可在 `https://<你的帳號>.github.io/Jeju_Trip_2026/` 開啟。

## 要修改內容時

所有內容都在 `index.html` 裡，用文字編輯器（VS Code、記事本）打開即可：

- **人員與房間**：搜尋 `車輛與人員安排`、`房型與床位安排`
- **每日行程**：搜尋 `<article class="day" id="day1">`（day1 ~ day5）
  每個行程項目的結構是：
  ```html
  <div class="item">
    <div class="time">10:30</div>
    <div class="tag">景點</div>
    <div class="box">
      <h3>標題</h3>
      <p>說明文字</p>
      <div class="tip">補充（門票、提醒）</div>
    </div>
  </div>
  ```
  在 `class="item"` 加上 `key`（`class="item key"`）可把時間點標成重點。
- **配色**：檔案開頭 `:root` 區塊的 CSS 變數

## 備註

頁面中不含任何證件號碼、訂單編號、電話個資或 Email。
