# CSS Glassmorphism 實戰：打造 Pro Max 質感

如何利用 `backdrop-blur` 與 `box-shadow` 營造高品質的毛玻璃效果。

## 關鍵技術點

1. **柔和背景**: `bg-white/40`。
2. **深度模糊**: `backdrop-blur-xl`。
3. **光澤邊框**: `border-white/20`。
4. **細膩陰影**: `shadow-glass`。

### 示範 Tailwind 代碼

```html
<div class="bg-white/40 backdrop-blur-xl border border-white/20 shadow-glass">
  Content here.
</div>
```

> 「質感藏在 0.1 像素的邊框裡。」
