# nightly 操作備忘（非凍結）

本檔只記錄易變操作資訊，不能變更 [治理](../GOVERNANCE.md) 或 [巡檢方法](nightly-inspection.md)。時間與負責人只在 GOVERNANCE §8 維護。

## 原排程核對來源
[Claude 2026-10-08 獨立複查](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29#issuecomment-6053940575) 已透過 list_triggers 讀原排程「議會 GitHub 每晚巡檢」完整 prompt，逐項核對方法。Claude 回報排程啟用、最近一次 10-07 成功。這是 Claude 的原始工具查證紀錄，ChatGPT 本輪不能直接存取同一排程；未宣稱修改或精簡完成。

排程是雲端觸發，設定沒有綁定議長電腦；依 Claude 本次存取實測，只有 .github 讀寫需要議長電腦上的已登入 Chrome。電腦／Chrome 不可用時其他可讀 repo 照巡，.github 覆蓋情形依凍結 runbook 回報。此資訊可隨工具能力改變更新，不能用來擴權。ChatGPT／Codex 本輪 GitHub 連接器則實測可讀寫 .github 的候選 PR；不同工具的能力不可互相推定。

## 原 prompt 的操作技巧（保留來源紀錄，使用前實測）
- Claude 的 .github 入口：議長電腦已登入 Chrome；可在瀏覽器工具允許範圍用 fetch 讀取。只使用已授權入口，不繞過限制。
- 留言框先點選，再用鍵盤輸入；送出後讀回確認。原提示記錄 commit 訊息可能被 Copilot 改寫，提交後核對實際訊息與檔案。
- Codex review 的 commit_id 表示其複查 SHA；不以 review 發表時間推定 head。原提示曾用 👍 或「對 head 無行內意見」判斷通過，這是介面辨識線索，**不能單憑反應或空白評論替代 GOVERNANCE 要求的鎖定 SHA 複查結論**。用 review／結論正文核對，缺完整證據則依巡檢方法交接。
- 原提示的三段、200字通知與固定無事訊息屬方法；新方法正本已明定通知內容與無變化不重複通知，不能用本備忘改回另一套標準。

## 合併後執行入口
Claude 可依其既有存取核對最新合併版，取得明確排程修改授權後精簡；留下舊／新 prompt 對照與工具成功結果到網站 #29。未完成前不標整輪凍結。
入口提示範例（不重複方法規則）：
> 依既有排程時間，讀 NCCU-Student-Congress/.github main 的 GOVERNANCE.md 與 runbooks/nightly-inspection.md，工具入口見 runbooks/nightly-operations.md；結果回寫來源 Issue／PR。
