# Self-Update Skill

🔄 让 Claude Code Skills 自我进化 - 自动分析反馈、优化结构、持续改进

## 功能特性

- **自动经验提取**：分析 skill 执行过程中的成功模式和失败教训
- **目录结构检查**：确保符合 Claude Code Skill 规范
- **渐进式加载优化**：避免上下文膨胀，按需加载内容
- **流程图自动维护**：同步更新决策流程文档
- **持续改进闭环**：收集反馈 → 分析优化 → 自动更新

## 使用方法

在 Claude Code 中使用以下命令触发：

```
/自更新
```

或在对话中提到：
- "自更新"
- "更新 skill"
- "优化 skill"
- "改进 skill"

## 工作流程

1. **上下文分析** - 识别使用过的 skills 和执行结果
2. **经验提取** - 提取成功模式和失败教训
3. **目录结构检查** - 验证文件组织是否规范
4. **渐进式加载检查** - 确保内容分层合理
5. **优化建议生成** - 生成具体改进方案
6. **更新执行** - 应用优化并更新流程图

## 目录结构规范

```
skill-name/
├── SKILL.md              # 核心指令文件
├── references/           # 参考文档目录
│   ├── decision-flow.md  # 决策流程图
│   └── *.md              # 其他参考文档
├── scripts/              # 可执行脚本
└── assets/               # 输出资源
```

## 示例场景

### 目录结构优化
```
❌ workflow.md 在根目录 → 应移至 references/
❌ sonarqube.svg 在根目录 → 应移至 assets/
✅ 自动重组为规范结构
```

### 渐进式加载优化
```
⚠️ SKILL.md 有 450 行，接近上限
✅ 将详细示例移至 references/examples.md
✅ 保持核心流程简洁
```

## 安装

将此 skill 添加到你的 Claude Code skills 目录：

```bash
cd ~/.claude/skills
git clone https://github.com/canxua/self-update-skill.git
```

## 技术细节

详见 [SKILL.md](SKILL.md) 和 [决策流程图](references/decision-flow.md)

## License

MIT
