# 安装与升级

## Gemini Spark + NotebookLM（推荐）

1. 从 [v1.9.23 r13 有限保证版](https://github.com/jbky97/rosa-skill/releases/tag/skill-v1.9.23-r13-limited) 下载 `rosa-skill-v1.9.23-r13-package.zip`，先阅读随附 [发行限制](https://github.com/jbky97/rosa-skill/releases/download/skill-v1.9.23-r13-limited/LIMITED-RELEASE-NOTES.md)。引文、精确定位及 PDF 使用前须人工核对。本版为 CURRENT_LIMITED / USER_ACCEPTED_LIMITED，不是完整独立验收 PASS；旧版 Release 原样保留。
2. 包内只有完整的 `rosa/` 文件夹，可在 Gemini Skills 页面拖放 ZIP“替换技能”，或以“更新已有 rosa”安装；不要新建第二个 rosa。若该环境要求先解压，请保留完整 `rosa/` 文件夹，以 `rosa/SKILL.md` 为入口，保持 `references/` 与 `assets/` 的相对路径。
3. 安装后开新对话，核对 `SKILL.md` 的 Integration Revision 与 references 版本行为 `v1.9.23 r13`，确认能读取当前文件。仅把 ZIP 附到普通聊天，不等于平台已经持久安装技能。
4. 在支持 NotebookLM 的宿主中，挂载你有权限使用的笔记本。需要直接引文时，应让宿主读取实际检索片段；笔记本名称或书目本身不能替代原文。
5. 使用 README 的试用提示，提供实际经文及译本名称，确认 ROSA 按当前任务作答并诚实披露缺失资料。

Gemini/Spark 与 NotebookLM 的界面和可用接口因环境而异。本指南描述必要步骤，不保证每一种 Gemini 部署都提供持久技能安装或 NotebookLM 连接。

## Claude、Codex 与其他 Agent

若平台支持文件式 skill，按该平台的技能安装方式放置完整 `rosa/` 目录，并使 Agent 能读取 `SKILL.md` 与 references。不要只复制一个入口文件。

若平台只支持聊天附件，可解压后提供必要运行文件并明确要求从 `SKILL.md` 开始；将这种方式视为当前会话加载，不要假定跨会话自动保留。不同平台的持续安装流程尚需分别确认。

## 校验下载

Windows PowerShell：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath .\rosa-skill-v1.9.23-r13-package.zip
```

将结果与同一 Release 的 [SHA256.txt](https://github.com/jbky97/rosa-skill/releases/download/skill-v1.9.23-r13-limited/SHA256.txt) 比对。r13 安装 ZIP 为 108455 bytes，SHA-256：`4567bc9824e57f179dc510c2542414eb276f96226f13ef4025037f7395d643db`。校验对象是安装 ZIP，不是 GitHub 自动生成的 Source code archive。

## 升级保留个人资料

### Gemini Spark 升级须知

- 升级前用 `/toolbox-export` 导出并另存当前 `references/user_toolbox.md`；不要使用聊天或沙盒中的旧副本。
- 在 Gemini Skills 页面拖放“替换技能”，或以“更新已有 rosa”安装，保留现有 `references/user_toolbox.md`；不要新建第二个 rosa。这里只在你的安装副本中保留个人文件，不改写公开安装包。
- 安装后开新对话，核对版本行为 `v1.9.23 r13`，再用 `/toolbox-list` 对照个人条目编号与名称。
- 安装包本身不含个人 Toolbox，只含空白模板。没有个人文件时无需制造一份。

1. 备份已有 `rosa/references/user_toolbox.md`。
2. 更新官方运行内容，保持文件结构。
3. 恢复并检查个人文件。首次安装没有个人文件属于正常情况；包里提供空白模板。
4. 开新对话，重新运行试用提示，并确认使用的新版本及个人条目编号。

若宿主会整目录替换，务必先导出个人文件再升级。
