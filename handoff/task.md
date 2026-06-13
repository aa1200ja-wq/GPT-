# 目前任務

## 一、任務基本資料

* 任務編號：TEST-001
* 任務名稱：Codex Cloud 連線與交接流程測試
- 任務狀態：已完成，禁止重跑
* 核准人：老闆
* 執行者：Codex
* 驗收者：GPT／小安
* 基準分支：由 Codex Cloud 介面選定，目前為 `main`
* 工作分支：使用 Codex Cloud 平台提供的工作分支

> Codex 只有在「任務狀態」明確寫為「已批准執行」時，才可以開始工作。

## 二、任務目標

驗證 Codex Cloud 能否：

1. 正確讀取根目錄 `AGENTS.md`
2. 正確讀取本文件
3. 只修改獲准的檔案
4. 更新 `handoff/report.md`
5. 保留平台產生的變更並停止

## 三、唯一允許執行的工作

1. 直接使用 Codex Cloud 平台提供的工作分支

2. 新增檔案 `checks/codex-connection.md`

3. 該檔案內容必須為：

   # Codex Connection Test

   * Task: TEST-001
   * Status: completed
   * Repository: aa1200ja-wq/GPT-
   * Protected repository untouched: aa1200ja-wq/online_rollcall

4. 更新 `handoff/report.md`

5. 如實填寫任務結果、修改檔案、測試結果與 Codex Cloud 交付狀態

6. 保留平台產生的變更

7. 完成後立即停止

## 四、允許修改的檔案

* `checks/codex-connection.md`：允許新增
* `handoff/report.md`：允許修改

除以上兩個檔案外，不得修改任何其他檔案。

## 五、禁止修改的範圍

* 不得操作 `aa1200ja-wq/online_rollcall`
* 不得修改 `AGENTS.md`
* 不得修改根目錄 `README.md`
* 不得修改 `handoff/README.md`
* 不得修改 `handoff/task.md`
* 不得自行更改任務批准狀態
* 不得直接推送或合併至 `main`
* 不得自行執行 `git fetch`
* 不得要求存在 `origin` remote
* 不得自行建立、切換或重新命名分支
* 不得新增任何套件
* 不得新增無關功能
* 不得自行重構
* 不得寫入密碼、API Key、Token 或其他機密資料

## 六、Codex Cloud 執行規則

* 直接使用平台提供的工作分支
* 不得因本地沒有 `main` 分支而停止
* 不得因不存在 `origin` remote 而停止
* 不得執行 `git fetch`
* 不得手動建立或切換分支
* 不得自行推送或合併至 `main`
* 任務完成後保留平台變更
* Pull Request 由 Codex Cloud 介面後續處理
* 若尚未建立 Pull Request，於回報中填寫「待 Codex Cloud 介面建立」

## 七、驗收條件

* 已新增 `checks/codex-connection.md`
* 檔案內容符合任務指定內容
* 已更新 `handoff/report.md`
* 變更範圍只有：

  * `checks/codex-connection.md`
  * `handoff/report.md`
* 未修改 `handoff/task.md`
* 未修改 `AGENTS.md`
* 未操作 `aa1200ja-wq/online_rollcall`
* 未寫入任何機密資料
* 已保留 Codex Cloud 平台產生的變更
* 完成後已停止

## 八、必須執行的測試

1. 執行 `git diff --check`
2. 執行 `cat checks/codex-connection.md`
3. 執行 `git status --short`
4. 確認變更清單只有：

   * `checks/codex-connection.md`
   * `handoff/report.md`

## 九、交付要求

完成任務後必須：

1. 更新 `handoff/report.md`
2. 寫明任務編號與任務名稱
3. 寫明完成內容
4. 列出所有修改與新增檔案
5. 寫明全部測試指令與結果
6. 填寫 Codex Cloud 工作分支資訊
7. Pull Request 尚未建立時，填寫「待 Codex Cloud 介面建立」
8. 保留平台產生的變更
9. 完成後立即停止

## 十、停止條件

遇到以下情況必須立即停止並回報：

* 無法讀取 `AGENTS.md`
* 無法讀取本任務
* 需要修改未授權檔案
* 任務要求操作其他儲存庫
* 測試無法執行
* 發現可能破壞既有內容
* 發現密碼、API Key、Token 或其他機密資料
* 無法依照允許範圍完成任務

未經 GPT／小安驗收及老闆說「通過」，不得自行執行下一個任務。
