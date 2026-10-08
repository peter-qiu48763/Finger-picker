# 🖐️ 指尖抽籤分組 (Finger Picker)

> 聚會、聚餐買單、活動分組必備的多人觸控隨機抽籤 PWA 網頁應用。

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?logo=github)](https://github.com/)
[![PWA Ready](https://img.shields.io/badge/PWA-Ready-green?logo=pwa)](https://web.dev/progressive-web-apps/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## ✨ 核心特色

* **🎲 抽籤模式（Pick Mode）**：支援選出 $1 \sim 5$ 位贏家，具備動態聚光燈與呼吸光環特效。
* **👥 分組模式（Group Mode）**：支援將現場玩家隨機分成 $2 \sim 5$ 組，以鮮明 HSL 霓虹色彩平滑漸變分組。
* **💫 流暢物理動態**：手指放置時具備旋轉鎖定環；鬆開時具備平滑縮小淡出動畫，告別生硬消失。
* **📱 深度行動端優化**：
  * **Screen Wake Lock API**：放置等待期間螢幕自動保持常亮，防止手機休眠。
  * **iOS Safari 防手勢衝突**：全面攔截 Safari 3 指以上縮放、選單呼叫與橡皮筋滾動。
  * **全螢幕沉浸體驗**：直向鎖定，支援「加到主畫面」如同原生 App 般運行。
* **⚡ 離線運作 (PWA)**：內建 Service Worker 快取，無網路環境亦可隨時啟動。
* **🎨 精緻現代視覺**：深色主題介面搭配 Google Fonts **LINE Seed JP** 字型與現代扁平幾何圖示。

---

## 🚀 部署至 GitHub Pages 教學

專案已配置好所有 GitHub Pages 必需檔案（包含 `.nojekyll` 與 GitHub Actions 自動部署腳本），請依照以下步驟上傳：

### 方法一：透過 GitHub Actions 自動部署（推薦）

1. **建立遠端倉庫**：在 GitHub 上建立一個新的公開（Public）倉庫（例如：`Finger-picker`）。
2. **推動程式碼**：在本地專案目錄執行下列終端機指令：
   ```bash
   git init
   git add .
   git commit -m "feat: initial commit for finger picker"
   git branch -M main
   git remote add origin https://github.com/<你的GitHub帳號>/<你的倉庫名稱>.git
   git push -u origin main
   ```
3. **啟用 GitHub Pages**：
   * 進入該 GitHub 倉庫的 **Settings** $\rightarrow$ **Pages**。
   * 在 **Build and deployment** $\rightarrow$ **Source** 選項中，選擇 **GitHub Actions**。
   * 系統將自動執行 `.github/workflows/deploy.yml`，約 1~2 分鐘後即可透過下列網址存取：
     ```text
     https://<你的GitHub帳號>.github.io/<你的倉庫名稱>/
     ```

### 方法二：傳統分支部署（Branch Deploy）

若不想使用 GitHub Actions，亦可直接使用分支部署：
1. 進入 GitHub 倉庫的 **Settings** $\rightarrow$ **Pages**。
2. 在 **Build and deployment** $\rightarrow$ **Source** 選擇 **Deploy from a branch**。
3. **Branch** 選擇 `main`（或 `master`），資料夾保持 `/ (root)`，點擊 **Save** 即可。

---

## 📲 如何安裝為桌面應用 (PWA)

### iOS (iPhone / iPad)
1. 使用 **Safari** 瀏覽器開啟專案網址。
2. 點擊瀏覽器底部的 **分享按鈕**（向上箭頭圖示）。
3. 向下滑動並選擇 **「加入主畫面」**（Add to Home Screen）。
4. 點擊右上角「新增」，即可從桌面全螢幕開啟。

### Android
1. 使用 **Chrome** 瀏覽器開啟專案網址。
2. 點擊右上角選單（三個點）或畫面底部的安裝提示。
3. 選擇 **「安裝應用程式」** 或 **「新增至主螢幕」** 即可。

---

## 📂 專案檔案架構

```text
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions 自動部署腳本
├── .gitignore              # Git 忽略檔案設定
├── .nojekyll               # 停用 GitHub Pages 預設的 Jekyll 靜態建置
├── icon-192.png            # PWA 桌面圖示 (192x192)
├── icon-512.png            # PWA 高清啟動圖示 (512x512)
├── index.html              # 應用主程式
├── manifest.json           # PWA 應用設定檔
├── sw.js                   # Service Worker 離線快取控制腳本
└── README.md               # 專案說明與部署指南
```

---

## 📄 開源授權

本專案採用 [MIT License](LICENSE) 授權。
