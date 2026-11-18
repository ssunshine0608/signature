Adobe Team Email 簽名檔產生器

檔案：
- index.html
- assets/weblink x adobe.svg（右上 Logo）
- assets/pic.svg（右下裝飾圖）
- assets/icon-phone.png
- assets/icon-pin.png
- assets/icon-web.png
- assets/rainbow-line.png
（assets/icon-mail.png 目前沒有使用）

簽名檔組成：
- 一張 600×156 的簽名圖片（以 2 倍解析度 1200×312 輸出），內容含姓名、職稱、電話分機、
  技術信箱、公司地址、網站。字型為思源黑體（Noto Sans TC，由 Google Fonts 載入）。
- 各元素位置集中在 index.html 的 LAYOUT 設定，要微調位置改那裡即可。
- 圖片下方一行可點擊的文字「技術信箱：adbeservice@weblink.com.tw」，
  收件人的信箱擋圖片時，仍看得到、點得到技術信箱。

使用方式：
1. 整個資料夾部署到 Netlify / GitHub Pages 等 HTTPS 網址。
2. 同事開啟網頁，填寫中文姓名、英文姓名、職稱、分機。
3. Outlook：按「複製簽名檔」，到簽名設定貼上。
4. 需要單獨的圖片檔時，可用「下載圖片檔」。

注意：
- 不要直接雙擊 index.html 開啟，瀏覽器會封鎖圖片輸出。請用部署後的網址，
  或在本機用 `python3 -m http.server` 開啟。
- 技術信箱、地址、網站寫在 index.html 最上方的 COMPANY 設定，改一次全員適用。
- Logo 與裝飾圖已換成 SVG 向量檔（文字已轉外框），輸出清晰。
  SVG 不需設定寬高，程式會依 viewBox 自動處理。
- 小圖示（電話、地址、網站）與彩虹線仍是從試作圖裁切的低解析 PNG，
  之後可換成 SVG，並修改 index.html 裡 COMPANY.assets 的檔名。
