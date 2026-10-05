# NCCU-Student-Congress/.github

政大學生議會 GitHub 組織的共通治理層。只放跨 repo 共通、可公開的規則與範本；業務特則在各 repo。

- [`GOVERNANCE.md`](GOVERNANCE.md)：共通治理（正本、Project／執行者、工作鎖、PR／複查、AI 權限基線、共通 label）
- [`.github/pull_request_template.md`](.github/pull_request_template.md)：PR 範本（第一行複查狀態）
- [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/)：工作 Issue、待議長決定 Issue 範本

組織內沒有自己同類檔案的 repo，GitHub 會自動套用這裡的 Issue／PR 範本；`CLAUDE.md`／`AGENTS.md` 不會自動繼承，所以各 repo 的入口檔都要連回 `GOVERNANCE.md`。

修改本 repo 一樣走 branch＋PR，由製作者以外的執行者複查、議長合併。
