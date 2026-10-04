# 安装与升级

## Gemini Spark + NotebookLM（推荐）

1. 从 [v1.9.20 Release](https://github.com/jbky97/rosa-skill/releases/tag/skill-v1.9.20) 下载 `rosa-skill-v1.9.20.zip`。
2. 在 Spark 的技能／文件管理环境中导入 ZIP；若该环境要求先解压，请保留完整 `rosa/` 文件夹，以 `rosa/SKILL.md` 为入口，保持 `references/` 与 `assets/` 的相对路径。
3. 确认当前任务能读取 `SKILL.md` 和它指向的 references。仅把 ZIP 附到普通聊天，不等于平台已经持久安装技能。
4. 在支持 NotebookLM 的宿主中，挂载你有权限使用的笔记本。需要直接引文时，应让宿主读取实际检索片段；笔记本名称或书目本身不能替代原文。
5. 使用 README 的试用提示，提供实际经文及译本名称，确认 ROSA 按当前任务作答并诚实披露缺失资料。

Gemini/Spark 与 NotebookLM 的界面和可用接口因环境而异。本指南描述必要步骤，不保证每一种 Gemini 部署都提供持久技能安装或 NotebookLM 连接。

## Claude、Codex 与其他 Agent

若平台支持文件式 skill，按该平台的技能安装方式放置完整 `rosa/` 目录，并使 Agent 能读取 `SKILL.md` 与 references。不要只复制一个入口文件。

若平台只支持聊天附件，可解压后提供必要运行文件并明确要求从 `SKILL.md` 开始；将这种方式视为当前会话加载，不要假定跨会话自动保留。不同平台的持续安装流程尚需分别确认。

## 校验下载

Windows PowerShell：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath .\rosa-skill-v1.9.20.zip
```

将结果与同一 Release 的 `SHA256.txt` 比对。校验对象是安装 ZIP，不是 GitHub 自动生成的 Source code archive。

## 升级保留个人资料

1. 备份已有 `rosa/references/user_toolbox.md`。
2. 更新官方运行内容，保持文件结构。
3. 恢复并检查个人文件。首次安装没有个人文件属于正常情况；包里提供空白模板。
4. 重新运行试用提示，并确认使用的新版本。

若宿主会整目录替换，务必先导出个人文件再升级。
