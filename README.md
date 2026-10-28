# design-software-like-simon

> 像 Herbert Simon 那样设计软件：用一套固定的设计认知，与开发者一起探讨、设计、评审、修订软件设计。

Simon 是一个**认知工程**组件：把与平台无关的设计认知，编译成某个 LLM harness 上可加载的 agent 与 skill。名字取自 Herbert Simon，但它不是历史人物本身，而是一个承担资深系统设计工程师职责的设计角色。

当前处于**穿刺阶段**：尚未经过真实项目验证，暂不设置验收规格与测试用例。

## 它能做什么

- 与开发者探讨问题、目标、约束、备选方案与风险。
- 形成可判断、可辩护的设计文档。
- 评审 Simon 生成或外部的设计文档。
- 按评审意见、未决问题或外部变化修订设计。
- 跨项目复用同一套设计判据。

## 它不做什么

- 不提供领域事实，不承诺领域正确性。
- 不替开发者做最终决策；可以推荐方案、辅助决策，但由开发者拍板。
- 不写代码、不编译、不部署。
- 不做过程记录、会议纪要或项目管理。
- 不做通用写作与文风润色。
- 不演进方法论；方法论固定，Simon 只应用。

## 目录

| 目录 | 作用 |
|---|---|
| `source_prompt/` | 平台无关的设计认知。入口是 `index.md`，按诉求路由 |
| `source_prompt/requests/` | 每个诉求一份文件：探讨、设计、评审、修订、复用、质疑与边界 |
| `source_prompt/references/` | 设计说明书 `design.md` 与固定文档结构 `template.md` |
| `compile_prompt/` | 平台相关的构建规则；当前目标为 opencode V2 |
| `build/` | 编译生成的 agent 与 skill；不手改，当前未入库 |

## 使用方式

1. 读 `source_prompt/index.md`，按诉求路由进入对应文件。
2. 按 `compile_prompt/opencode/装配说明.md` 生成 `build/opencode/`。
3. 按生成的 `build/opencode/使用指引.md` 安装到 opencode。
4. 穿刺阶段只按 `compile_prompt/opencode/穿刺验证.md` 做可用性检查与实战观察。

## 设计文档

完整设计说明书见 `source_prompt/references/design.md`。它说明 Simon 的背景、场景、边界、实现与当前穿刺状态，不作为运行时默认加载内容。

## 许可

[MIT](LICENSE)
