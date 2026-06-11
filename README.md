# claude-project-template

在 AI 辅助开发中沉淀的可复用项目模板。新项目从此模板初始化，即可令较差模型获得较好的工作质量。

## 对谁有用？

模板的核心思路是**把工程判断编码为机械可执行的规则**，因此最佳受益者是"有足够智力理解规则，但还没聪明到能自主做出那些判断"的模型。

| 效果 | 代表模型 | 说明 |
|------|----------|------|
| 锦上添花 | Claude Opus 4.5+、GPT-5.0-high、Gemini 3.5 Pro | 模型自己能做出好判断，模板只是免提的保险 |
| 改善明显 | Qwen 3.6、GLM-5.1、Claude Sonnet 4.5、DeepSeek-V4、Gemini 3.0 Pro、GPT-4.1 | 有推理能力但容易 drift scope、过度工程、静默编造——模板的规则恰好堵住这些缺口 |
| 减少伤害 | 低于 GPT-4o / Claude Sonnet 4.0 / DeepSeek-V3 | 机械规则部分可执行，判断力部分空转。不会变好，但撞车时伤得轻 |

## 包含内容

- **CLAUDE.md 模板** —— 预置占位符（技术栈、命令、目录结构、工作流），填入项目信息即可使用；同时包含「回答质量约束」章节（事实/推论分隔、工具失败降级、信源选择规则），无需额外配置
- **engineering-mindset skill** —— Google 级 code review 标准的工程思维规范，要求 AI 以清晰性优先、推断意图、拒绝过度工程、不自作主张扩大范围

## 使用方法

1. 将本仓库复制到新项目根目录：

```bash
git clone git@github.com:KaleidScoper/claude-project-template.git my-new-project
rm -rf my-new-project/.git
```

2. 编辑 `CLAUDE.md`，取消各占位符的注释并填入项目实际信息
3. 如果项目有专属设计语言或额外规范，在 `.claude/skills/` 下添加对应 skill
4. 视情况在 `.claude/settings.local.json` 中配置权限

或：

1. 只复制你需要的部分
2. 享受您的生活和 Agent 的高质量回复

## 维护原则

本模板只收录**跨项目通用**的约束和规范。与特定项目绑定的内容（如博客设计语言、某个框架的配置）不应进入此模板。