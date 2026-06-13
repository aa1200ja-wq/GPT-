# GPT × Codex Cloud 專案範本

此資料夾用來保存可複製到其他 GitHub 專案的 GPT × Codex Cloud 協作範本。

此處的文件是範本，不是目前專案的即時任務文件。

## 範本文件

- `AGENTS.template.md`
  - Codex Cloud 的專案執行規則
  - 複製到新專案根目錄後，重新命名為 `AGENTS.md`

- `task.template.md`
  - GPT／小安派發單一任務時使用
  - 複製到新專案的 `handoff/task.md`

- `report.template.md`
  - Codex 完成任務後填寫的執行回報
  - 複製到新專案的 `handoff/report.md`

## 新專案套用順序

1. 在新專案根目錄建立 `AGENTS.md`
2. 在新專案建立 `handoff` 資料夾
3. 建立 `handoff/task.md`
4. 建立 `handoff/report.md`
5. 將任務狀態維持為「尚未派發」
6. GPT／小安完成任務規格後，才可改為「已批准執行」
7. 在 Codex Cloud 選擇正確的儲存庫與基準分支
8. Codex 完成修改後更新執行回報
9. GPT／小安驗收 Pull Request
10. 老闆說「通過」後才可合併
11. 合併後將任務狀態改成「已完成，禁止重跑」

## 重要限制

- 每次只允許一個已批准任務
- Codex 不得自行修改任務內容或批准狀態
- Codex 不得自行操作其他儲存庫
- Codex 不得自行合併 Pull Request
- 未經 GPT／小安驗收及老闆通過，不得執行下一個任務
- 每個新專案都必須重新填寫允許操作的儲存庫名稱
- 不得直接沿用其他專案的儲存庫名稱、檔案路徑或測試指令
