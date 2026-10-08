# NCCU-Student-Congress/.github

政大學生議會 GitHub 組織的共通治理層。只放跨 repo 共通、可公開的規則與範本；業務特則在各 repo。

- [`GOVERNANCE.md`](GOVERNANCE.md)：共通治理（正本、Project／執行者、工作鎖、PR／複查、AI 權限基線、共通 label）
- [`runbooks/nightly-inspection.md`](runbooks/nightly-inspection.md)：跨 repo 巡檢方法（治理凍結範圍）
- [`runbooks/nightly-operations.md`](runbooks/nightly-operations.md)：排程與存取核對備忘（非凍結）
- [`.github/pull_request_template.md`](.github/pull_request_template.md)：PR 範本（第一行複查狀態）
- [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/)：「一般工作」「待議長決定」Issue 範本

組織內沒有自己同類檔案的 repo，GitHub 會自動套用這裡的 Issue／PR 範本；`CLAUDE.md`／`AGENTS.md` 不會自動繼承，repo 採用本治理時，其入口檔應連回 `GOVERNANCE.md`。

修改本 repo 一樣走 branch＋PR，由製作者以外的執行者複查、議長合併。

## 給議長／秘書處（不用懂程式）

**每天只要看兩個地方：**
1. 等你決定的事：<https://github.com/search?q=org%3ANCCU-Student-Congress+is%3Aopen+label%3A%E5%BE%85%E8%AD%B0%E9%95%B7%E6%B1%BA%E5%AE%9A&type=issues>
   看完在該 Issue 留言回答（一句話就好，例如「選 A」）。
2. 等你合併的 PR：<https://github.com/pulls?q=is%3Aopen+is%3Apr+org%3ANCCU-Student-Congress>

**按合併前確認兩件事**（PR 頁最上面那段文字的第一行）：
- 寫的是「複查：通過」。
- 括號裡的 SHA，和 PR 頁「Commits」分頁最新一個 commit 的編號開頭相同。不同就先不要按，代表複查後又有人改過。
確認好，拉到 PR 最下面按綠色的「Merge pull request」→「Confirm merge」。

**各 repo 是做什麼的**
| repo | 內容 |
|---|---|
| `nccu-sc-website` | 議會官網（xms+）的樣式、程式、交接文件、會議資料上網清單 |
| `nccusa-regulations` | 法規各版本的整理、校對紀錄、上網清單 |
| `parliament-bills` | 議案系統（另有維護者，變更要先問他） |
| `.github`（本 repo） | 大家共用的規則與範本 |

**要 AI 做事時**：對任何一個 AI 說「看 ○○ repo 的 Issue #N，做下一步」就好，不用重講背景。
**出問題時**：先看該 Issue 最新一則留言寫的「下一步執行者」；看不懂就在那個 Issue 留言問。
