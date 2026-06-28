# 贡献指南

感谢你对 resume-interview 的关注！🎉

本项目欢迎任何形式的贡献——无论是修复 bug、添加新功能、完善参考知识库，还是改进文档。

## 目录

- [行为准则](#行为准则)
- [如何贡献](#如何贡献)
  - [提交 Issue](#提交-issue)
  - [提交 Pull Request](#提交-pull-request)
  - [完善参考知识库](#完善参考知识库)
- [开发指南](#开发指南)
- [代码规范](#代码规范)

## 行为准则

本项目采用 [Contributor Covenant](https://www.contributor-covenant.org/) 行为准则。通过参与，你同意遵守其条款。详见 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)。

## 如何贡献

### 提交 Issue

如果你发现了 bug、有功能建议，或者想讨论某个改进点，请先[搜索现有 Issues](https://github.com/CaHB2015/resume-interview/issues) 确认是否已被提出过。

**Bug 报告**请包含：
- 使用的 Skill 版本
- 复现步骤
- 期望行为 vs 实际行为
- 截图/日志（如有）

**功能建议**请包含：
- 你的使用场景
- 期望的效果
- 能否通过现有功能实现（可选分析）

### 提交 Pull Request

1. **Fork** 本仓库
2. 创建你的特性分支：`git checkout -b feat/your-feature-name`
3. 提交你的改动
4. 确保你的代码符合规范
5. 推送到你的仓库：`git push origin feat/your-feature-name`
6. 提交 Pull Request

### 完善参考知识库

`references/` 目录下的四个知识库文件是本 Skill 的核心。特别欢迎以下贡献：

- **capability-map.md**：增加更多技术栈到能力的映射（如新增 Rust、Kotlin 等）
- **interview-topics.md**：补充更多面试话题和追问方向
- **jd-keywords.md**：补充更多岗位类型的关键词
- **output-templates.md**：补充更多技术栈的输出示例

## 开发指南

### 目录结构

```
resume-interview/
├── SKILL.md                    # Skill 主文件（核心工作流和规则）
├── README.md                   # 项目说明
├── agents/
│   └── openai.yaml             # Agent 配置
├── references/
│   ├── capability-map.md       # 技术栈 -> 能力映射表
│   ├── interview-topics.md     # 能力 -> 面试话题映射表
│   ├── jd-keywords.md          # 岗位 JD 关键词库
│   └── output-templates.md     # 输出模板与示例
├── examples/
│   └── sample-output.md        # 完整输出示例
└── outputs/                    # 生成的输出文件（.gitkeep）
```

### 修改 SKILL.md

SKILL.md 是本 Skill 的核心。修改时请注意：

1. 保持 `---` 开头的 YAML front matter 格式
2. 遵守原有的 10 步流程框架
3. 新增的规则/步骤要在目录中更新
4. 确保「坏示例」和「好示例」同时更新

## 代码规范

- **Markdown**：使用 GFM（GitHub Flavored Markdown）格式
- **YAML**：缩进 2 空格
- **中文**：使用中文标点符号，中英文之间加空格
- **表格**：保持列对齐，方便阅读

再次感谢你的贡献！🙏