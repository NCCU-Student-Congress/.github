# nightly 操作備忘（非凍結）

本檔只記錄易變操作資訊，不能變更 [治理](../GOVERNANCE.md) 或 [巡檢方法](nightly-inspection.md)。時間與負責人只在 GOVERNANCE §8 維護。

## 排程沿革與目前運作（非凍結、依本輪工具／留言實測）

- **舊排程**：「議會 GitHub 每晚巡檢」`trig_01MnixRQbCtcWqE2njATZVWu` 曾綁定議長的 MSI-HOME 電腦，並非「只有 .github 讀寫需要電腦」。2026-10-08 已停用、尚未刪除，以保留紀錄。參見 [Claude 發現本機綁定的更正](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29#issuecomment-6054738928)。
- **新排程**：「議會 GitHub 巡檢與接手（雲端）」`trig_01MbviWzJnNvCisc1XPphqEf`，每日 21:50（Asia/Taipei）。Claude 2026-10-08 建立時收到 `local_device_not_required`，故不需開著 MSI-HOME 才能啟動；主責與規範時間仍依 GOVERNANCE §8。參見 [#29 排程切換紀錄](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29#issuecomment-6060684723)。
- **第一次實跑（2026-10-08）**：Claude 回報已用 `git clone` 取得 .github 的 GOVERNANCE 與兩份 runbook，巡查網站及文史兩 repo 的開啟 Issue／PR，並回寫來源。這只能證明已執行上述範圍，不能推定往後每輪成功。
- **明確未巡範圍**：當次雲端排程的 WebFetch 讀取 `.github` 公開 Issue／PR 時需要逐次授權，但排程無人核准而撤回；因此**未巡 .github 的 Issue／PR**。雲端 Claude 的 .github 寫入也未打通。此缺口交由具存取權的 ChatGPT／Codex GitHub 連接器補巡、必要時回寫；若要改用其他入口或預先授權，仍由議長決定，不能自行繞過授權。證據：[首次實跑範圍與阻塞](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29#issuecomment-6061556583)。

上述是可變的工具／排程現況，不更動 [巡檢方法](nightly-inspection.md)、[治理權限](../GOVERNANCE.md) 或來源 Issue 工作鎖。不同工具能讀寫的範圍不得互相推定。

## 原 prompt 的操作技巧（保留來源紀錄，使用前實測）
- 原本在議長電腦 Chrome 使用的 .github 瀏覽器入口屬**舊排程的歷史技巧**，不是新版雲端排程的必要條件。新版可唯讀 clone 規則檔，但 .github Issue／PR 的 WebFetch 仍受授權限制；請依本輪實際可用入口補位，不繞過限制。
- 留言框先點選，再用鍵盤輸入；送出後讀回確認。原提示記錄 commit 訊息可能被 Copilot 改寫，提交後核對實際訊息與檔案。
- Codex review 的 commit_id 表示其複查 SHA；不以 review 發表時間推定 head。原提示曾用 👍 或「對 head 無行內意見」判斷通過，這是介面辨識線索，**不能單憑反應或空白評論替代 GOVERNANCE 要求的鎖定 SHA 複查結論**。用 review／結論正文核對，缺完整證據則依巡檢方法交接。
- 原提示的三段、200字通知與固定無事訊息屬方法；新方法正本已明定通知內容與無變化不重複通知，不能用本備忘改回另一套標準。

## 執行入口、補位與後續驗證

新排程已建立、舊版已停用；不能再將「等待在 MSI-HOME 核准精簡原排程」當作目前阻塞。雲端版的提示已改為讀最新 `.github/main` 的治理與巡檢 runbook，並在符合工作鎖時直接接手 GitHub 任務；真正執行情況仍依每次來源 Issue／PR 留言核對。

實際巡檢範圍：能查的 repo 正常巡，讀不到的 repo 列清楚「未巡、原因、下一位執行者」，不能寫成「全組織完成」；.github Issue／PR 暫由有連接器權限的 ChatGPT／Codex 補巡。若要讓 Claude 雲端版完全涵蓋 .github，須先取得合規的唯讀入口與授權，並再做實跑驗證。

本文件只處理平台操作與能力記錄；原定巡檢時間、風險升級、PR 複查、禁止自行合併／擴權等，以 GOVERNANCE §8／§9 和 [nightly-inspection.md](nightly-inspection.md) 為準。網站治理總收尾仍以 [nccu-sc-website#29](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29) 為正本，尚未由主筆宣告凍結生效。
