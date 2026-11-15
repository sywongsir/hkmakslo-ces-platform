# 羅桂祥X現代：公經社科學習平台

初中公民、經濟與社會科（中一至中三）12 個單元的自學網站。每個單元有以下功能：

- 重點溫習：問題導入、學習目標、單元總結概念圖
- 重要詞彙：翻轉詞卡和可搜尋的列表
- 課前小測：每單元 20 題選擇題和填充題，供上課前預習，即時對答案和看解說
- 資料回應題：寫完答案後逐點「對照評分點」自評，亦可查看完整參考答案
- 課本搜尋：在 12 個單元的詞彙、單元總結和小測中搜尋，附單元和頁碼

網站是純靜態網頁，不使用 AI，不需要任何 API 金鑰或伺服器程式，也不會收集學生資料。學生的進度和答案只儲存在他們自己裝置的瀏覽器內。

## 檔案結構

```
index.html        網站主頁（全部介面和程式）
data/units.js     12 個單元的內容，可直接修改
assets/crest.jpg  校徽
assets/modern.jpg 現代教育研究社標誌
netlify.toml      Netlify 設定（只在用 Netlify 時需要）
```

## 部署方法（任選一種）

- **Netlify Drop（最簡單）**：登入 Netlify，把整個資料夾拖放到「Deploy manually」的方框，即可得到網址。
- **GitHub ＋ Netlify**：把資料夾上載到 GitHub repository，再在 Netlify 選「Import an existing project」連接該 repository。Build command 留空，Publish directory 填 `.`。之後修改 GitHub 的檔案，網站會自動更新。
- **GitHub Pages**：把資料夾上載到 GitHub repository，在 Settings → Pages 選擇 main branch 和根目錄（/ root）。

## 修改內容

所有教學內容都在 `data/units.js`。常見修改：

- **小測題目**：每題的 `a` 是正確答案的序號，0 代表 A，1 代表 B，如此類推。`e` 是解說。
- **資料回應題評分點**：每條開放題有 `points`，每點的 `t` 是內容，`m` 是分數。`note` 是補充說明，例如「任何兩項」。
- **重要詞彙**：每個詞的格式是［中文、英文、課本頁碼、定義］。

修改後請保留原有的逗號和引號格式。完成後，在瀏覽器打開 `index.html` 檢查一次。
