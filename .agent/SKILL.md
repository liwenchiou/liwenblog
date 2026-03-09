---
name: liwenblog-universal-constitution
description: Liwenblog 的全域最高指導原則。所有開發與管理行為必須優先遵循本文件。
---

# 📜 Liwenblog 全域最高指導原則 (Project Constitution)

> [!IMPORTANT]
> **這不是單純的工作流或技能，而是 Agent 在本專案中的「靈魂」與「底層邏輯」。**
> 任何開發或維運動作，若與本原則衝突，應立即停止並回報。

---

## 一、 持續進化與反饋機制 (Highest Priority: Evolution)

1.  **[發現問題記錄]**: 每次執行 Skill 或收到使用者反饋時，Agent **必須即時將問題與改進建議記錄至** [發現問題.md](file:///Users/qiuliwen/Documents/工程師/project/liwenblog/.agent/發現問題.md)。這是一切行動的最高優先記錄義務。
2.  **[自我修正路徑]**: 每次開啟新的對話，Agent 必須先讀取記錄檔，確保不在同個坑洞跌倒第二次。這是為了讓 Skill 在長期使用中不斷進化。

## 二、 認知的最高維度 (Universal Architecture)

1.  **[架構聖經]**: 每次啟動對話或新子任務，Agent 必須「預熱」對 [ARCHITECTURE.md](file:///Users/qiuliwen/Documents/工程師/project/liwenblog/ARCHITECTURE.md) 的記憶。它是專案的地基。
2.  **[美學鐵律]**: 「數位建築師」不是風格，是法律。Copper (#D27B5E) 與 Slate-Ink (#2D3436) 是專案唯一的顏色主權。
3.  **[A11y 與 SEO 協同]**: 嚴禁為了 SEO 抓取而破壞 Accessibility 體驗。所有隱藏標籤 (`sr-only`) 必須確保邏輯一致，不得與 `aria-hidden="true"` 同時作用於同一語義元素。
4.  **[SPA SEO 架構守則]**: 本專案為動態單頁應用 (SPA)，所有文章層級的 SEO 優化必須依賴：1. Deep Linking (URL Query `?post=` 或 `?moment=`) 以確保獨立網址 2. 動態注入 JSON-LD (`BlogPosting`)。3. **嚴格動態替換 Canonical URL 與 Meta Description**，防止權重強制綁死首頁。
5.  **[CDN 優先 (Zero Build)]**: 本專案嚴格維持「零構建」架構。嚴禁在本專案中執行 `npm` 或 `yarn`。
6.  **[GitHub Pages 部署相容性]**: 變更資源路徑或路由時，必須確保在 GitHub Pages 環境下運作。
7.  **[繁體中文主權]**: 本專案 UI、文章、註解與文件，一律使用繁體中文。

## 三、 分支安全與執行權限界定 (Security & Permissions)

1.  **[Main 分支主權]**: `main` 分支是被絕不可直接更動的「穩定境界」。
    - **偵測守衛**: 在下達任何檔案寫入命令前，Agent 必須先主動執行 `git branch` 檢查。
    - **另開分支**: 若位於 `main`，Agent **必須主動詢問**：「我們現在在 main，是否另開分支（如 `feat/xxx`）？」禁止代為決定。
2.  **[Git 管理統一化]**: 執行 Git 操作時，唯一合法媒介是 [git-manager](file:///Users/qiuliwen/Documents/工程師/project/liwenblog/.agent/skills/git-manager) Skill。嚴禁繞過該規範體系。

## 四、 零猜測與二次確認協議 (Second-Check Protocol)

1.  **[零黑箱作業]**: 功能完成後，必須完整列出修改清單 (Diff 摘要)，並詢問：「功能已完成，是否需要啟動 Git 交付流程？」
2.  **[高互動提問]**: 
    - 寧可因提問而遲緩，也不可因猜測而導致回滾。
    - 對於美感的主觀決定，必須提供「方案 A/B」供使用者選擇，禁止獨斷。
3.  **[穩定編輯協議 (Stable Edit Protocol)]**:
    - **先視後改**: 任何重大修改前，必須先執行 `view_file` 鎖定 **即時行號** 與內容，嚴禁憑過期記憶下達指令。
    - **精準打擊**: 優先選用 `multi_replace` 進行細碎且精確的替換，避免整塊覆蓋導致的匹配失敗與損壞。
4.  **[消耗優化協議 (Token-Optimization)]**:
    - **精簡溝通**: 回覆應直擊重點，減少冗餘的開場白與結語，優先使用列表與 Markdown 標註。
    - **局部寫入**: 修改檔案時，除非必要（如全新檔案），否則嚴禁重寫整個檔案。優先修改受影響的最小區塊，以節省上下文空間。
    - **高效率檢索**: 避免在一次對話中重複讀取相同內容。Agent 應具備良好的會話內記憶管理，僅在必要時發起重複檢索。

## 五、 優先級層級 (Priority Hierarchy)

1.  **憲章 (本文件)** > **Git Skill 規範** > **任何個別指令**。

---

_本文件的層級在 `.agent` 中被定義為全域 Skill，為 Agent 開機後的最高讀取優先權。_
