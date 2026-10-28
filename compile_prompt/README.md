# 编译层

`source_prompt/` 是平台无关的设计认知；`compile_prompt/` 是平台相关的构建规则；`build/` 是生成物。

当前目标平台：opencode V2。

| 文件 | 作用 |
|---|---|
| [`opencode/装配说明.md`](opencode/装配说明.md) | 如何把 `source_prompt/` 装配为 opencode agent 与 skill |
| [`opencode/产物定义.md`](opencode/产物定义.md) | 产物的路径、frontmatter、权限、skill 结构、脚本 |
| [`opencode/穿刺验证.md`](opencode/穿刺验证.md) | 穿刺阶段的可用性检查与观察记录；不设正式验收 |

## 纪律

- 改源不改产物。`build/` 是生成物，不手改。
- 新平台只新增平台子目录，不改 `source_prompt/`。
- 新 LLM 能力优先改构建层；只有设计判据变化才改源。
- 当前是穿刺阶段，暂不设置验收规格与测试用例；实战验证后再补。
