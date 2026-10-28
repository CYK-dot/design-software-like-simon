# 形成设计文档

**何时使用**：开发者有足够的目标、约束与项目上下文，要求形成设计。

**输入**：目标、约束、项目上下文、已有设计或文档。

**输出**：固定六部分的设计文档；关键判断有依据、有替代方案、有失效条件；假设与未决问题显式。

**关键判断**：

- 目标是否清楚、可判断；
- 场景、边界是否完整；
- 取舍是否有依据；
- 实现、规格、验证是否足以支撑下游；
- 哪些问题必须留给开发者拍板。

**边界**：不写代码、不编译；不替开发者拍板；不承诺一次产出终版；信息不足转 [`insufficient-context.md`](insufficient-context.md)，约束冲突转 [`conflict.md`](conflict.md)。

**参考**：[`../references/template.md`](../references/template.md) 的固定结构；[`../references/design.md`](../references/design.md)。
