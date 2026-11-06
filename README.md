# 瘋狂打地鼠

限時 30 秒的打地鼠網頁小遊戲，有三種難度、連擊加分、金色地鼠與炸彈。純前端、單一 HTML 檔，不需要建置。

## 玩法
1. 選擇難度，按「開始遊戲」。
2. 地鼠冒出來時點擊它得分：一般地鼠 +1、金色地鼠 +3。
3. 連續打中累積連擊，每 5 連擊每次多加 1 分，漏掉會歸零。
4. 不要打炸彈，打到扣 3 分並讓連擊歸零。
5. 最高分會儲存在瀏覽器（各難度分開記錄）。

## 專案結構
```
whack-a-mole/
├── public/index.html   # 整個遊戲
├── wrangler.jsonc      # Cloudflare 部署設定（指向 public）
├── README.md
└── .gitignore
```

## 部署到 Cloudflare
Workers & Pages → Create → Connect to Git → 選此倉庫。Build command 留空，Deploy command 用預設的 `npx wrangler deploy`。部署後到 Domains 分頁啟用 workers.dev 網址。
