# kxn-project-governance-style

`kxn-project-governance-style` 是一个通用项目治理风格 skill，用来让 AI 尽量按 `kxn` 在 `codex-remote-feishu` 这个项目里体现出的方式推进软件工作。

它不是项目文档改写版，也不是仓库专有命令集合，而是一份抽象后的治理风格 skill，强调：

- issue / 任务合同化
- 先共享模型，再铺表层入口
- 分阶段推进，并在阶段间复评
- 把 maintainability 当持续工作流
- 把风险、交付、文档测试和产品语言治理纳入主线

## 这个 skill 从哪里来

这个 skill 不是手工随意总结出来的，它来自两个上游来源：

- 风格生成器：[`repo-style-skill-builder`](https://github.com/RichardCao/repo-style-skill-builder)
- 证据来源仓库：[`kxn/codex-remote-feishu`](https://github.com/kxn/codex-remote-feishu)

也就是说，这个仓库里的 skill 是基于 `kxn/codex-remote-feishu` 的 issues、commits、代码、测试和文档证据抽象出来的发布结果。

## 仓库结构

这个发布仓库把 repo 级文档放在根目录，把真正的 skill payload 放在 `skill/` 下面。这样仓库可以有 README 和 LICENSE，同时不污染 skill 本体目录。

```text
kxn-project-governance-style/
  README.md
  .gitignore
  skill/
    kxn-project-governance-style/
      SKILL.md
      agents/openai.yaml
      references/
```

## 安装

把下面这个目录复制到你的 Codex skills 目录中：

```text
skill/kxn-project-governance-style
```

例如：

```bash
mkdir -p "$HOME/.codex/skills"
cp -R skill/kxn-project-governance-style "$HOME/.codex/skills/"
```

## 使用方式

安装完成后，可以直接这样调用：

```text
用 $kxn-project-governance-style 推进这项工作：
- 背景：...
- 目标：...
- 范围：...
- 非目标：...
- 当前代码位置 / 系统上下文：...
- 已知风险 / 历史包袱 / 约束：...
先输出实施合同和分阶段计划。
```

这个 skill 更适合：

- 容易 scope 漂移的 feature
- 需要先收敛 shared model / source of truth 的改动
- 需要同时考虑交付、文档、测试和风险边界的任务

它不适合：

- 明确定位的极小修补
- 不涉及共享模型、用户入口、交付路径或风险边界的纯小改
