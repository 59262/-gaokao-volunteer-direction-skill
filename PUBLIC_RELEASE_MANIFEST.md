# 公开发布范围说明

本项目按“公开学习材料”和“本地工作资料”分开管理。公开仓库只提供框架、核心 Skill、实现逻辑、使用说明、架构说明和虚构示例，不提供真实业务数据、数据库资料或历史恢复包。

## 建议公开

- `高考志愿填报方向选择Skill.md`
- `README.md`
- `docs/usage.md`
- `docs/architecture.md`
- `examples/sample-input.md`
- `CONTRIBUTING.md`
- `LICENSE-CHOICE.md`，或作者确认许可证后替换为正式 `LICENSE`
- `.gitignore`
- `PUBLIC_RELEASE_MANIFEST.md`

## 保留在本地，不提交

- `提问文档.docx`、`prd文档.docx`
- `_compare_extract/`
- `_prd_render/`
- `.obsidian/workspace.json` 及其他本地工作区状态
- `SECURITY.md`
- `SECURITY_AUDIT.md`
- `OPEN_SOURCE_CHECKLIST.md`
- 任何数据库导出、数据库连接信息、历史恢复包、日志、备份、用户输入、真实案例和内部安全材料

这些文件不会被删除；`.gitignore` 只用于防止误提交。公开发布前应通过暂存区检查确认本地资料没有进入提交。

## 公开内容边界

公开内容可以解释：

- Skill 的角色、触发条件和多轮提问流程
- 输入、输出、失败处理和风险边界
- 报告模板、评分框架和官方核验逻辑
- 虚构示例和可复用的文档结构

公开内容不应包含：

- 真实考生分数、位次、预算、偏好或完整对话
- 数据库文件、数据库连接信息、恢复包和备份
- API Key、Token、Cookie、密码、私钥和内部域名
- 内部安全事件、历史审计记录和本地路径

## 发布前最小检查

```powershell
git status
git add .
git diff --cached --name-only
```

暂存区文件应只来自“建议公开”列表和作者明确确认的新增源代码。不要把 `git diff --cached` 的敏感内容复制到公开 Issue 或聊天中。
