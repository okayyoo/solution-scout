# Solution Research · 方案调研

在实现前调查现成做法，帮助用户选定适合当前约束的方向。

[English](README.md) · [完整规则](SKILL.md) · [类似 skill 对比](docs/related-skills.md)

## 适用场景

- 提出了非琐碎的新功能或新流程，尚未确定怎么做。
- 想找现成工具、成熟开源实现，或比较不同架构与服务。
- 希望得到有来源、有推荐、有明确取舍的选型建议。

明确的小改动、常规 bug 修复和按既定方案执行的任务，不会自动进入一轮新的选型。

## 工作方式

1. 读取已有上下文与相关项目，明确目标、约束和真正待定的问题。
2. 检查现有能力，调研成熟产品、开源实现和适用实践。
3. 通常比较 2–4 个可行方案，说明关键差异、成本、限制与直接来源。
4. 给出推荐；需要用户选择时询问，已有选择或用户已委托决策时继续原任务。

用户只要求调研时，交付研究结论后结束。联网或来源读取受限时，明确标注未核实的部分。

## 安装

下载或克隆仓库，将内容放入代理配置的 skill 目录，目录名为 `solution-research`，并确保该目录根部包含 `SKILL.md`。`agents/openai.yaml` 是供支持它的宿主读取的界面元数据。

已安装同名 skill 时，先比较内容再决定是否替换。按所用代理的说明刷新或重新发现 skill。

## 使用示例

```text
用 $solution-research 调研桌面应用离线搜索的实现方案。
沿用现有技术栈，优先考虑维护成本，给我推荐、取舍和来源。
```

```text
对比现成服务、开源自建和复用现有组件三种方向。
先给建议，等我选定后再实现。
```

规则正文使用中文，输出沿用用户语言。工具名不写死，由代理选用当前环境可用的搜索、网页、仓库和提问能力。

## 文件

- `SKILL.md`：触发条件、研究流程、证据要求和选择边界。
- `agents/openai.yaml`：界面显示名称、简介和默认调用提示。
- `docs/related-skills.md`：类似项目的来源及定位差异。

这是纯指令 skill，无运行时依赖。已完成结构检查和决策边界静态评审，尚未进行跨代理行为实测。

## 版本

- [v1.0.0](https://github.com/okayyoo/solution-research/tree/v1.0.0)：原始 skill，保存在首次提交中。
- [v1.1.0](https://github.com/okayyoo/solution-research/tree/v1.1.0)：完善决策边界、证据要求、工具兼容及使用文档。

[提交历史](https://github.com/okayyoo/solution-research/commits/main/) · [版本差异](https://github.com/okayyoo/solution-research/compare/v1.0.0...v1.1.0)
