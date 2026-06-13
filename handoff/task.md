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
2. 新增檔案 `checks/codex-connection.md`
3. 該檔案內容必須完全如下：

```markdown
# Codex Connection Test

- Task: TEST-001
- Status: completed
- Repository: aa1200ja-wq/GPT-
- Protected repository untouched: aa1200ja-wq/online_rollcall
