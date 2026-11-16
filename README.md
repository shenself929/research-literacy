# research-literacy

把 GAMES 003《科研素养课》第一周的科研流程，封装成一个可复用到任意学科的研究教练 Skill。

它不是“替你想 idea”的灵感机器，而是把课件里的方法论变成可执行动作：先定位你卡在科研流程的哪一环，再用课件的问题清单把模糊的研究问题压成可检查的产物。

## 它解决什么

| 你的状态 | Skill 的回应 |
|---|---|
| 刚入门，不知道怎么建立领域认识 | 时间轴思维导图 + 重要问题四问 |
| 有方向但不会选题，担心竞争或做不完 | 研究问题 brief + 选题评估表 |
| 有题但方案不清，想证明创新点 | 方法设计四步 + 预期 insight |
| baseline 不 work，不知道先试什么 | exploration points 拆解 + 优先级 |
| 要写论文，但讲不清故事 | story 五段 + 写作 9 步 + 自评 checklist |
| 要读论文、做组会或审稿准备 | Abstract / Introduction / Method / Experiments 四棵解析树 |
| 要从截止日期倒排 Project | 节点表 + 风险熔断 + 周节奏 |
| 想复习第一周课件 | 按“位置 → 原意 → 例子 → 易错点 → 自测 → 下一步”讲解 |

## 结构

```text
research-literacy/
├── SKILL.md
├── references/
│   ├── ppt-derived-framework.md       # PPT 规范内容层（P1–P81 页码锚点）
│   ├── general-research-adaptation.md # 跨学科对应式延伸规则
│   ├── paper-question-trees.md        # 论文解析四棵树
│   └── quality-boundaries.md          # 来源标签、不编造、作业口径、PDF 说明
└── assets/
    ├── research-problem-brief.template.md
    ├── field-timeline.template.md
    ├── method-experiment-loop.template.md
    ├── paper-story-writing-plan.template.md
    └── project-backward-plan.template.md
```

## 安装

把整个目录放到 ZCode 的用户级技能目录：

```text
~/.agents/skills/research-literacy/
```

Windows 下通常是：

```text
C:\Users\<你的用户名>\.agents\skills\research-literacy\
```

新开一个会话或刷新技能索引后生效。

## 使用

直接说触发词即可，例如：

```text
用 research-literacy 帮我把这个研究问题写成 brief。
我的 baseline 不 work，按这套课的方法帮我拆 exploration points。
帮我为这个方向做一份时间轴思维导图和未解问题清单。
用四棵解析树带我读这篇论文。
从投稿日期倒排我的 Project 计划。
讲讲第一周课件里的“建立领域视野”。
```

也可以显式调用：

```text
/skill research-literacy <你的问题>
```

## 设计原则

1. **以 PPT 为主体**：三阶段主线、P12 setting、P22 exploration points、P28 写作 9 步、P46 自评、P57 时间轴三步、P60–P63 解析树、P79 倒排计划，全部按页码锚定。
2. **允许跨学科，但只做对应式延伸**：保留课件的判断维度，替换领域名词；每次映射都写明“把 X 对应为 Y，因为……”。
3. **先要事实，再给方法**：信息不足时最多一次问 4 个关键问题，缺项标 `[待确认]`，不编造文献、SOTA 或实验数字。
4. **落到可检查的产物**：brief、时间轴、评估表、实验矩阵、story 五段、写作计划、倒排表；不以“多读论文、多思考”收尾。
5. **边界明确**：正式作业只认“时间轴思维导图 + 未解决重要问题 + PDF 提交”；baseline 改进、读代码、Project 节点属于过程性任务。

## 来源与边界

- 课件正文来自课程整理稿 `week_1_notes.html`，该整理稿自称整理自 `week_1.pdf` 全部 81 页。
- 原始 `week_1.pdf` 受密码保护，未能独立逐页读取；技能中的 `Pxx` 均指 HTML 记录的课件页码，不代表已完成 PDF 独立核验。
- 整理稿与原始 PDF 未随本仓库分发。
- 本仓库只包含方法论提炼与模板，不包含课程幻灯片原文或图片。

## License

MIT
