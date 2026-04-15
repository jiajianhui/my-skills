# My Skills

这个项目用于存放我日常使用、持续维护和逐步沉淀的 Codex skills。

这里的 skill 会围绕不同工作场景进行整理，例如设计、开发、产品等，方便我自己复用，也方便后续同步到 GitHub 做版本管理、备份和分享。

## 使用方式

每个 skill 以独立文件夹存在，核心文件为 `SKILL.md`。后续可以按主题继续新增不同 skill 文件夹。

当前仓库结构：

- `design/`：设计相关 skill
- `dev/`：开发相关 skill
- `product/`：产品相关 skill

其中 `design/` 当前细分为：

- `ui-direction/`：专注网站、产品界面、落地页、后台等 UI 设计方向
- `brand-direction/`：专注品牌气质、品牌关键词和视觉语言方向
- `graphic-design/`：专注海报、KV、社媒图、宣传物料等平面设计

## 制作 Skill 的两个关键原则

1. `SKILL.md` 要短、准，只写 agent 真正需要的流程、判断标准和执行方式。
2. 大段资料不要堆进主文件，拆到 `references/`、`scripts/` 或 `assets/`，这样更容易维护，也更节省上下文。

## 对目录的理解

- `references/`：放参考资料、方法论、风格标准、检查清单，供 agent 按需读取。
- `assets/`：放可直接复用的模板、素材、示例文件，供 agent 产出结果时使用。
- `scripts/`：只在确实需要固定脚本或重复自动化时再加；不是每个 skill 都需要。

## Skill 是什么

Skill 可以理解为给 agent 使用的专项工作说明书。

它的作用不是替代 agent 思考，而是为 agent 提供：

- 适用场景
- 工作流程
- 判断标准
- 输出结构
- 可复用参考资料

## Skill 如何触发

Skill 的触发主要取决于 `SKILL.md` 中的 `name` 和 `description`，以及用户当前任务是否与之匹配。

常见触发方式：

- 用户的需求和 skill 的描述高度匹配
- 用户在任务里直接点名某个 skill
- agent 判断当前任务适合使用某个 skill

## Skill 如何工作

当某个 skill 被命中后，通常按这个顺序发挥作用：

1. agent 先根据 `name` 和 `description` 判断是否使用该 skill
2. 命中后读取该 skill 的 `SKILL.md`
3. 如有需要，再按需读取 `references/`
4. 如有可复用模板，再使用 `assets/`
5. 最终按这套规则组织分析、判断和输出

## 实际使用方式

1. 把 skill 文件夹放到 Codex 可读取的 `skills` 目录中
2. 正常描述你的真实工作任务
3. 如果想更稳定地触发某个 skill，可以直接点名它，或让任务描述更贴近它的 `description`

## 优化 Skill 的最佳实践

先真实使用，再根据问题修改，不要一开始就写得过大过满。

一个实用迭代流程：

1. 用 skill 完成一次真实任务
2. 记录输出哪里不满意
3. 判断问题出在哪一层
4. 只修改对应文件
5. 再用相似任务验证效果

可按这套规则判断改哪里：

- 触发不准：改 `description`
- 主流程不稳：改 `SKILL.md`
- 细节标准不够：改 `references/`
- 输出模板想复用：改 `assets/`
