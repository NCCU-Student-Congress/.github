# nightly 操作備忘（非凍結）

本檔只記錄易變操作資訊，不能變更 [治理](../GOVERNANCE.md) 或 [巡檢方法](nightly-inspection.md)。

## 已有來源與本輪驗證範圍
- .github#5 記錄議長帳號 Claude 排程「議會 GitHub 每晚巡檢」每日21:50台北時間、需議長電腦開著 Claude 桌面版；換屆須移交或重建。
- 網站#29 第一則 Claude 盤點記錄：2026-10-06提示由 list_triggers 取得；.github 曾需議長電腦Chrome。這是來源紀錄，不能推定每輪都需要同一瀏覽器。
- 本輪 ChatGPT／Codex 實測 GitHub 連接器可讀 .github main、Issue／PR 並建立候選分支；**沒有取得或修改 Claude 排程原文**。因此方法為依#29公開已確認內容編製的候選，不宣稱完整逐字移轉。

## 每次先確認
測試當次 repo／證據讀寫、登入與複查工具，不把產品名當能力。不得把憑證、密碼或私有內部資料写進本公開檔案；有登入能力不等於正式環境授權。
只用具權限的既有工具入口。若無法取得 .github，不繞過存取限制，回寫未巡範圍。

## 合併後待核對
具存取及明確權限的原排程執行者，先讀原提示，對照 nightly-inspection.md，將缺漏以PR交獨立複查後再精簡；保留原有時間、工具入口與來源Issue回寫。在網站#29記錄完成或阻塞，不只留聊天。未核對前不得標整輪治理凍結完成。
精簡提示範例（入口文字，實際排程仍須按原工具確認）：
> 每日21:50（Asia/Taipei），讀 NCCU-Student-Congress/.github main 的 GOVERNANCE.md 與 runbooks/nightly-inspection.md，透過當次已授權工具執行，將結果寫回來源Issue／PR；依runbook通知。
