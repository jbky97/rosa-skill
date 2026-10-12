# ROSA — Reformed Orthodoxy Study Assistant

以改革宗正统为底色的研经、神学研究与教学备课助手。

**[下载 v1.9.21 r16 · 有限保证版](https://github.com/jbky97/rosa-skill/releases/tag/skill-v1.9.21-r16-limited)** · [安装指南](INSTALL.md) · [发行限制](LIMITED-RELEASE-NOTES.md) · [更新记录](CHANGELOG.md)

当前有限保证版用于讨论、研究草案与备课，不是完整独立验收 PASS。引文／作者归属、精确定位和双层 PDF 使用前须人工核对。以下 v1.9.20 特性描述是历史说明，不代表新版自动可靠性保证；[v1.9.20 完整验收基线](https://github.com/jbky97/rosa-skill/releases/tag/skill-v1.9.20) 仍保留。

本仓库提供正式安装包、校验文件和用户说明。GitHub 自动生成的 **Source code ZIP / TAR 不是 ROSA 安装包**，请使用上方下载链接。

## 三步开始

1. 下载 `rosa-skill-v1.9.21-r16-package.zip`，并阅读随附有限保证说明。
2. 按 [安装指南](INSTALL.md) 将 ROSA 导入你的平台；推荐 Gemini Spark 配合 NotebookLM。
3. 提供一段你实际使用的经文文本，再让 ROSA帮助你开始查经、研究或备课。

试用提示：

> 请使用 ROSA。以下是我提供的经文文本：〔贴入经文及译本名称〕。先说明如何开始研读，并提出两个观察问题；暂时不要生成完整教案。需要引用外部资料时，请区分已读来源与尚未核实的内容。

## v1.9.20 带来什么

- 检查引用后提出具体修复方案，由用户批准后应用并重新检查。
- 区分“已批准”“已修改”与“已解决”，避免把计划当作完成。
- 支持带领者与学员材料；学员版保留必要的来源限制，隐藏内部审计标识。
- 强化经文来源、引文定位和 PDF 导出核验。

ROSA 的证据规则帮助减少错误；生成内容仍需要带领者审阅。没有可读原文时，ROSA 应披露限制，不应编造引文或页码。

## 校验与升级

当前 Release 同时提供 [SHA256.txt](https://github.com/jbky97/rosa-skill/releases/download/skill-v1.9.21-r16-limited/SHA256.txt)。当前 ZIP 是冻结 r16 的原始字节副本，有限接受不等于独立验收。旧 v1.9.20 Release 与校验文件原样保留。

升级前备份你自己的 `references/user_toolbox.md`。安装包不含个人文件；更新时保留或恢复它，不要因为新包没有该文件而删除个人资料。

包内 `rosa/` 为运行内容，`release-notes/` 为人类阅读的发布记录。包内冻结的阶段文字不代表当前发行状态；本公开发行以版本 Release 与 checksum 为准。
