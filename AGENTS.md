## My-AI 規則索引

本 workspace 的 AI 整合包：

> **通用大腦：** `./my-ai/AGENTS.md`  
> **後端知識（若已加入 submodule）：** `./back-ai/AGENTS.md`  
> **架構說明（維護必讀）：** `./my-ai/ARCHITECTURE.md`

將本檔複製到父 repo 根目錄，並依使用的 Agent 更名（例如 Cursor → `AGENTS.md`，Claude → `CLAUDE.md`）。

---

## Headroom

見 `./my-ai/headroom/start-headroom.ps1`。

---

## 引導師速查

完整列表見 `./my-ai/AGENTS.md`。常用：`@plan-maker`、`@pr-review`、`@summary`、`@story-log`、`@loop-spec`、`@update-repo`。

---

## 規範入口

- 架構說明：`./my-ai/ARCHITECTURE.md`
- AI 入口：`./my-ai/AGENTS.md`
- 前端/UI：`./.rules.md`（各 repo 根目錄，若無須先詢問）

將本檔複製到父 repo 根目錄並依 Agent 更名（例如 `.cursor/rules/general.mdc` 或 `.clinerules`）。

---

## 回復規則

- 回覆一律以繁體中文為主
- 除非我一開始就跟你說需要流程根結構，不然只給結論，若我有想知道其餘的會再問你(可以給提醒，不要流程跟結構就好)
