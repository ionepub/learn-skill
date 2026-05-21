# learn - 关键词学习法AI助手

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-blue)](https://github.com/anthropics/claude-code)

基于关键词学习法的 AI 助手，自动生成结构化学习文档。

## 功能特性

- 📚 **结构化学习文档**：包含用户画像、核心关键词表格、学习建议
- 🎯 **二八法则**：聚焦20%核心概念，产生80%学习效果
- 🔄 **动态生成**：支持任意关键词，自动生成对应学习指南
- 📝 **多格式输出**：支持 Markdown 和 HTML 格式
- 👥 **个性化适配**：根据用户身份和水平调整内容

## 用法

```bash
/learn <关键词> [身份] [水平] [格式]
```

### 示例

```bash
/learn 人工智能                    # 生成人工智能学习指南（默认Markdown）
/learn RAG 后端开发工程师 入门    # 生成RAG学习指南（针对后端工程师）
/learn 区块链 学生 入门 html      # 生成区块链学习指南（HTML格式）
```

### 参数说明

| 参数 | 说明 | 默认值 |
|------|------|--------|
| 关键词 | 学习主题（必填） | - |
| 身份 | 用户身份（如学生、工程师） | 学生 |
| 水平 | 知识水平（入门/进阶/专家） | 入门 |
| 格式 | 输出格式（markdown/html） | markdown |

## 输出内容

每个学习指南包含：

1. **用户画像分析**：根据身份和水平推断学习特征
2. **核心关键词表格**：20-30个核心概念，包含学术解释、通俗解释、示例和故事
3. **学习建议**：优先级排序、分阶段学习路径、实践应用建议
4. **扩展学习**：书籍、课程、项目、社区资源推荐

## 安装

将本项目克隆到 Claude Code 的技能目录：

```bash
# 克隆到技能目录
git clone https://github.com/your-username/learn-skill.git ~/.claude/skills/learn

# 或者添加为 git submodule
cd ~/.claude/skills
git submodule add https://github.com/your-username/learn-skill.git learn
```

## 项目结构

```
learn/
└── SKILL.md          # 技能说明文档（定义技能行为和指令）
```

## 开发

技能基于 [Claude Code Skill](https://github.com/anthropics/claude-code) 系统开发。

### 修改学习内容

编辑 `SKILL.md` 中的指令部分，调整：
- 核心关键词表格的分类和内容
- 学习路径的阶段划分
- 实践应用建议

### 调试

```bash
# 查看技能文档
cat ~/.claude/skills/learn/SKILL.md
```

## 许可证

MIT License

## 贡献

欢迎提交 Issue 和 Pull Request！
