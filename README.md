# claude-project-template

在 AI 辅助开发中沉淀的可复用项目模板。新项目从此模板初始化，即可获得一致的 AI 协作基线。

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

## 维护原则

本模板只收录**跨项目通用**的约束和规范。与特定项目绑定的内容（如博客设计语言、某个框架的配置）不应进入此模板。