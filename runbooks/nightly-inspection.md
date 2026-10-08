# 跨 repo 每晚巡檢 runbook

方法屬 GOVERNANCE §9 凍結範圍；權限與工作鎖先讀 [GOVERNANCE.md](../GOVERNANCE.md)。來源：[網站 #29](https://github.com/NCCU-Student-Congress/nccu-sc-website/issues/29)、[共通巡檢 #5](https://github.com/NCCU-Student-Congress/.github/issues/5)。操作實測另見 [非凍結備忘](nightly-operations.md)。

## 開始與範圍
1. 讀本 runbook 的 main 與共通治理；記錄當次基線、時間（Asia/Taipei）、可讀 repo。讀組織可存取 repo 的 open Issue／PR，相關全部留言、review、head/base 與 checks；不得把聊天或舊複查當最新狀態。
2. 先判斷來源 Issue 的工作鎖、製作者與主責工作線。若有他人「進行中」鎖，不搶改；直接正式留言交接。每個 PR 保持一個製作者，不在多處重複開工。
3. 本輪明確排除 parliament-bills 主分支與治理 PR #3 的變更、SP4U→SGC 搬遷及 Drive 檔案／分享權限；等待來源 Issue 的正式解除，不從巡檢推定授權。可讀狀態只作交接摘要，不代替正式維護者定案。
4. 任一來源不可讀，寫明「未巡範圍、具體原因、缺什麼、下一位執行者」。尤其 .github 不可讀時須明說「今晚未巡 .github」，不能宣稱全組織已巡完。

## PR 分流與複查
- 製作者不是 ChatGPT／Codex：依既有直接複查入口在 PR 請 @codex review；機器人不可用時列實際阻塞與替代複查者。不能把已送請求當已通過。
- 製作者是 ChatGPT／Codex：巡檢中的 Claude Code直接獨立複查，自己讀 diff 與支持主張的原始證據；不能再請 Codex 自查。無能力讀足證據則回報未驗證並交人工。
- 規則／驗收／發布結果變更不得當純文件跳過複查。複查留言鎖定完整 head SHA，記錄通過或需修正、證據與未驗證。
- 已複查後 head 改變：核對新增差異，受影響部分請原複查者重查；舊通過不可沿用到新 SHA。對已通過且 head 相等者，只依 GOVERNANCE §6 更新他人 PR 第一行複查索引。
- 需修正且工作鎖是 Claude Code：由其製作工作線在原分支修、更新交接、重新請獨立複查；其他製作者則正式交回，不代搶鎖。
- 每晚每個 PR 最多修一輪；持續 P0／P1 不停止追蹤。第三輪起若只有 P2／P3，不無限反覆修：把未解項與風險回寫來源 Issue／後續 Issue 並連結；**不得自行稱通過、跳過複查或接受風險**。若需跳過或風險裁決，交議長依 GOVERNANCE 辦理。
- 不重複催同一 head 的既有請求；新提交、具體失敗或需重查時才更新。

## 回寫與通知
把行動、head、review 連結、未驗證與下一步寫回各來源 Issue／PR；#29 只保存治理收尾依賴，不抄各工作的完整進度。
短通知列：等你合併（通過 SHA＝head）、等你決定（來源 Issue＋label）、卡住（原因／負責人）、未巡範圍。若沒有實質變化或需議長動作，不重複通知。
巡檢不合併、不改設定／權限、不碰正式環境、不關 Issue；日常交接不要求議長重新轉述。自動檢查成功不能替代正式環境驗收。

## 觸發、交接與排程精簡
現有來源記錄為議長 Claude 排程「議會 GitHub 每晚巡檢」，每日21:50 Asia/Taipei，負責人議長；換屆移交或重建。當次工具與登入依操作備忘核對。
合併後由具排程存取及明確權限者讀原提示、逐項比對本方法、留下核對紀錄，再精簡為時間＋讀 main runbook＋工具入口＋回寫來源正本。缺原文時不得宣稱遷移完整。
