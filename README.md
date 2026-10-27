# 理財目標導航

以理財目標為核心的 PV / FV / PMT 試算網站。純靜態單一頁面，不需建置步驟，也沒有後端。

## 專案結構

```
.
├── index.html   # 整個網站（HTML、CSS、JavaScript）
├── _headers     # Cloudflare Pages 安全與快取標頭
├── .gitignore
└── README.md
```

注意：`index.html` 必須位在儲存庫最外層。

## 部署到 Cloudflare Pages（連結 GitHub）

1. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git。
2. 選擇這個 GitHub 儲存庫。
3. 建置設定：
   - Production branch：`main`
   - Framework preset：None
   - Build command：留空
   - Build output directory：`/`
4. 按 Save and Deploy，完成後會得到 `https://專案名稱.pages.dev`。

之後每次推送到 main 分支，Cloudflare 都會自動重新部署。

## 其他說明

- 字型由 Google Fonts 載入。
- 使用者的目標資料存在各自瀏覽器的 localStorage，不會上傳到伺服器。
- 本機預覽：直接用瀏覽器開啟 `index.html`。

## 聲明

本工具為試算與教育用途，報酬率為假設值、非保證，不構成投資建議。
