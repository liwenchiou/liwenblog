# React CDN 效能優化：零構建不代表慢

探討如何透過預先載入、快取策略，讓 CDN-based 網站也能擁有驚人的初次渲染速度。

## 核心優化點

- **Preload**: 搶先載入 `index.css` 與關鍵圖片。
- **Browser Caching**: 利用瀏覽器的預設機制減少 API 調用。
- **Modular Load**: 只有需要用到時才去撈內容。

### 實際案例

> 「極簡不只在 UI，也在網絡封包裡。」
