HTML

架構：單頁式履歷，分成 header（標題）、aside > nav（側邊導覽）、main > article（履歷內容）、footer（聯絡方式）。內容有 7 個 section，每個都有 id，導覽列用錨點連結跳到對應區塊。

元件選用

語意化標籤：header、nav、main、section 等，讓頁面結構清楚。
dl 描述清單：就讀資訊、人格特質這類「名稱＋說明」的內容。
svg 雷達圖：直接畫在 HTML 裡，不用外部套件。
meter：用來表示技能程度。
details / summary：證照可以展開或收合，不需要 JavaScript。
time、address：日期和聯絡資訊；email 和電話是可以點的連結。
img（loading="lazy"）：照片捲動到附近才載入。
blockquote ＋ embed.js：用 Instagram 官方方式嵌入貼文。
CSS

架構：設計變數 → 基本設定 → 版面 → 共用元件 → 各區塊 → 響應式。

元件選用

CSS 變數：顏色、間距、字級統一管理，改一處就能改整體風格。
Grid 版面：用 Grid 分成側邊導覽和主內容兩欄；標題列和導覽列用 sticky 固定在上方。
卡片風格：半透明白底、模糊背景、直角深灰外框。
共用元件：堆疊清單、兩欄排版、輪播都只寫一次，各區塊用變數調整。輪播用 scroll-snap 讓滑動時自動對齊卡片。
圖片比例：用 aspect-ratio 固定比例，object-fit 自動裁切照片。
響應式：螢幕寬度 860px 以下改成單欄、導覽列變成橫向；560px 以下輪播一次顯示約 1 張。
