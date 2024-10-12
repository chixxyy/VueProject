# Hero Store

這個專案是一個基於 Vue 3 的簡單電商應用，使用 Vite 進行構建，並使用 Pinia 來進行狀態管理。專案包含深色模式切換、購物車功能，以及使用 SweetAlert2 來實現互動彈窗。

![page](./public/home.png)

## 專案設置

```sh
npm install 安裝

npm run dev 開發

npm run build 壓縮打包

npm run lint 代碼檢查

```

## 實現思路

深色模式
應用允許用戶切換亮色和深色模式，選擇會儲存於 localStorage 中，當用戶重新訪問時，根據上次選擇自動應用。深色模式透過 Tailwind CSS 的 dark 類管理。

購物車功能
購物車使用 Pinia 全局管理，包括商品數量、總金額、折扣等狀態，實現了組件間狀態共享。

折扣碼應用
支持百分比折扣與固定金額折扣，用戶可以輸入折扣碼進行驗證，折扣會套用到購物車的總價中。

## 使用的主要技術

Vue3：主框架，用於構建前端應用。
Vite：作為快速開發和打包工具。
Pinia：Vue 3 的狀態管理工具，用於管理購物車狀態。
Tailwind CSS：實用的 CSS 框架，用於構建響應式 UI，並支援深色模式。
SweetAlert2：用於顯示互動彈窗的外部庫。
localStorage：用於儲存用戶的主題偏好（亮色或深色模式）。

## 遇到的挑戰和解決方案

深色模式與狀態保持
最初僅部分 UI 元素響應深色模式，因此我們將深色模式的切換應用到整個頁面，透過 document.documentElement 操作 dark 類來實現全局效果。並使用 localStorage 來保存用戶的主題偏好。

狀態管理
透過 Pinia 來實現購物車狀態的全局管理，讓購物車數據在不同組件間共享，並在應用中實現響應式更新。
