# 第二大腦互動教學（涂子沛 · 自寫課程）

繁體中文（zh-Hant-MO）靜態站：消化《第二大腦》後以圖像、圖表、互動問答與 Logseq 實作路徑呈現，**非原文轉載**。

## 本地預覽

```bash
cd /workspace/second-brain-course
python3 -m http.server 8765
# 瀏覽器開啟 http://127.0.0.1:8765/
```

或直接用瀏覽器開啟 `index.html`（部分瀏覽器對 `file://` 的 localStorage 仍可用）。

## 站點結構

| 路徑 | 說明 |
|------|------|
| `index.html` | 總覽與學習路徑 |
| `chapters/` | 推薦序、第一～五章、結語（每章 ≥3 互動題） |
| `practice/index.html` | Logseq 實作：安裝→塊標籤頁→四類→日記→Query |
| `css/` `js/` | 樣式、進度（localStorage）、問答批改 |
| `assets/svg/` | 圖表 SVG |
| `assets/practice-data/` | 練習 Markdown／示例 graph／zip |

## 練習資料

- 本地：`assets/practice-data/second-brain-practice-pack.zip`
- Google Drive 資料夾（上傳後見 `DRIVE_UPLOAD_MANIFEST.md`）

## 部署建議

### GitHub Pages
1. 新建公開 repo（例如 `second-brain-course`）
2. 將本目錄內容推上 `main`
3. Settings → Pages → Source: Deploy from branch `main` / root
4. 取得 `https://<user>.github.io/second-brain-course/`

### Netlify / Cloudflare Pages
直接拖曳本資料夾，或接 Git repo，Publish directory 設為站點根目錄。

### 本機簡易分享
`python3 -m http.server` 或任何靜態檔伺服。

##  regenerating

若修改 `_build.py`：

```bash
python3 _build.py
```

之後若有手改章節增補，注意重新執行 build 會覆寫 `chapters/*.html` 與 `practice/index.html`。

## 授權與來源

課程內容為教學轉化與重組，僅供個人／內部學習。原著：《第二大腦》，涂子沛，三采文化。請自行購買正版圖書。


## 部署狀態（2026-10-29 Asia/Macau）

- **本地預覽就緒**：`python3 -m http.server 8765`（本機驗證 index／chapters／practice／zip 皆 HTTP 200）
- **GitHub Pages**：box 上 `gh` 尚未登入（`gh auth status` 顯示未登入），無法代為建立 repo／啟用 Pages。請在本機登入後依上方步驟推送，或把資料夾拖到 Netlify／Cloudflare Pages。
- **練習資料／整站 zip**：已上傳 Google Drive 資料夾 `1ZCUVje9qwt6XFagqQQFJ7Pdbyq1Y342B`（詳見 `DRIVE_UPLOAD_MANIFEST.md`）
- 整站壓縮包：https://drive.google.com/file/d/1F_39RqGxVYMz1d5Wi0DPeB9uh6vd9x-i/view?usp=drivesdk
- 預期 Pages 網址（repo 建好並推送後）：`https://wayneleong-byte.github.io/second-brain-course/`
- 尚待：Drive 資料夾設「知道連結的任何人＝檢視者」；GitHub 新建公開 repo 後 push
