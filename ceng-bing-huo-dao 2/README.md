# 曾阿牛的冰火島

用 3D 小島認識債券、股票、黃金、房產、選擇權、虛擬貨幣、期貨。純靜態網站，沒有後端、沒有資料庫、沒有建置步驟。

## 檔案

| 檔案 | 說明 |
| --- | --- |
| `index.html` | 整個網站（畫面、資料、3D 場景都在這一個檔案） |
| `vendor/three.min.js` | three.js r128（MIT 授權，已自帶，不依賴外部 CDN） |
| `vendor/three.LICENSE.txt` | three.js 授權檔，請一併保留 |

只有 Google Fonts 字體是線上載入；字體載入失敗時會自動改用系統字體。

## 本機預覽

不能直接雙擊開 `index.html`，請用本機伺服器：

```
cd 這個資料夾
python3 -m http.server 8080
```

瀏覽器開 http://localhost:8080

## 部署到 Render（靜態網站）

1. 在 GitHub 建新 repo，把這個資料夾內容放在根目錄：https://github.com/new
2. 到 Render 建立 Static Site：https://dashboard.render.com/select-repo?type=static
3. 選剛建的 repo，設定：
   - Build Command：留空（或填 `echo skip`）
   - Publish Directory：`.`
4. 按 Create Static Site，完成後會得到 `https://xxx.onrender.com` 網址。
5. 之後只要 push 到 GitHub，Render 會自動更新。

替代方案：GitHub Pages（repo 的 Settings → Pages → Deploy from a branch → main / root），同樣不用建置。

## 要改什麼，改哪裡

`index.html` 裡搜尋下列關鍵字：

- 各島文字、官方連結：`var ASSETS = [`
- 島與島的關聯與說明：`var LINKS = [`
- 比較表：`var COMPARE = {`
- 「船長一句話」：`var CAP = {`
- 島的位置與大小：ASSETS 內的 `pos`、`R`
- 網站名稱：搜尋 `曾阿牛的冰火島`（`<title>`、`og:title`、品牌卡各一處）

## 注意事項

- 內容為一般性教育導覽，不含即時報價，也不構成投資建議；官方連結與規則請定期檢查是否仍有效。
- 虛擬貨幣的監理規範仍在變動，該島的說明只指向金管會公告，請自行定期核對。
- 頁面中的人物、船隻與島嶼皆為原創武俠設計，與任何現有武俠小說、影視作品及其角色，以及任何政治人物、政黨、競選團隊都沒有關係。
