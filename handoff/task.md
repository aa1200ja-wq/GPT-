# 目前任務

## 一、任務基本資料

- 任務編號：TEST-001
- 任務名稱：Codex 連線與交接流程測試
- 任務狀態：已批准執行
- 核准人：老闆
- 執行者：Codex
- 驗收者：GPT／小安

> Codex 只有在「任務狀態」明確寫為「已批准執行」時，才可以開始工作。

## 二、任務目標

驗證 Codex 能否正確讀取 `AGENTS.md` 與本任務，使用獨立分支完成一項無風險的小型修改、更新執行回報，並建立 Pull Request。

## 三、唯一允許執行的工作

1. 從最新 `main` 建立獨立分支：`test/codex-handoff-001`
2. 新增檔案：`checks/codex-connection.md`
3. 該檔案必須依照以下五行內容建立：

    # Codex Connection Test

    - Task: TEST-001
    - Status: completed
    - Repository: aa1200ja-wq/GPT-
    - Protected repository untouched: aa1200ja-wq/online_rollcall

4. 更新 `handoff/report.md`
5. 提交變更並建立 Pull Request，目標分支為 `main`
6. 完成後立即停止

## 四、允許修改的檔案

- `checks/codex-connection.md`
- `handoff/report.md`

除以上兩個檔案外，不得修改任何其他檔案。

## 五、禁止修改的範圍

- 不得操作 `aa1200ja-wq/online_rollcall`
- 不得直接修改 `main`
- 不得修改 `AGENTS.md`
- 不得修改根目錄 `README.md`
- 不得修改 `handoff/task.md`
- 不得修改 `handoff/README.md`
- 不得安裝任何套件
- 不得新增無關功能
- 不得自行重構
- 不得寫入密碼、API Key 或 Token

## 六、驗收條件

- 使用分支 `test/codex-handoff-001`
- 只變更 `checks/codex-connection.md` 與 `handoff/report.md`
- `checks/codex-connection.md` 內容符合任務指定內容
- `handoff/report.md` 已完整回報
- 已建立以 `main` 為目標的 Pull Request
- `aa1200ja-wq/online_rollcall` 完全未被操作

## 七、必須執行的測試

1. 執行 `git diff --check`
2. 確認 `checks/codex-connection.md` 存在且內容正確
3. 確認變更清單只有：
   - `checks/codex-connection.md`
   - `handoff/report.md`

## 八、交付要求

完成任務後必須：

1. 更新 `handoff/report.md`
2. 列出所有修改檔案
3. 寫明測試指令與結果
4. 使用指定獨立分支
5. 建立 Pull Request
6. 完成後立即停止

## 九、停止條件

遇到以下情況必須立即停止並回報：

- 無法建立指定分支
- 無法讀取本任務或 `AGENTS.md`
- 需要修改未授權檔案
- 無法建立 Pull Request
- 測試無法執行
- 發現可能影響其他儲存庫

未經 GPT／小安驗收及老闆說「通過」，不得自行執行下一個任務。
