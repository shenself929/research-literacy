# 第一周 PPT 的规范内容层

本文件把课程整理稿 `week_1_notes.html` 中的课件正文按页码重组，供 `research-literacy` 引用。整理稿与原始 `week_1.pdf` 未随本技能分发。

**页码口径**：下文 `Pxx` 指 HTML 附录记录的课件页码（HTML 自称整理自 `week_1.pdf` 全部 81 页）。`week_1.pdf` 当前受密码保护，未能独立逐页读取；不得把这里的页码写成“已核对 PDF”。

**来源标签**：本文件内容默认 `[PPT原文]`。带“适配”字样的句子是 `research-literacy` 的延伸，不是课件原句。

---

## 1. 课程身份与总览（P1–P6）

### 1.1 课程身份

- 课程：GAMES 003 科研素养课 · 第一周。
- 主题：课程内容概览 & 建立领域视野。
- 讲师：彭思达、高俊、彭崧猷、王倩倩。

### 1.2 课程动机（P2）

低年级学生的常见情况：

- 缺乏研究策略；
- 面临科研困难；
- 遭遇情绪低落。

课程要回答的三件事：

- 如何选题与设计方法；
- 如何实验与提升方法；
- 如何写作与宣传工作。

目标：知道如何在科研过程中自我提升科研能力，成为一个快乐的研究人员。

### 1.3 科研全流程（P3–P4）

课程传授科研流程，解释每一步的具体操作，配合案例说明。整个流程分三大阶段：

```text
① 初始化科研课题
建立领域视野 → 选择科研课题 → 设计技术方案

② 迭代技术方案（循环）
基于技术方案设计实验 ⇄ 基于实验结果提升方案

③ 撰写学术论文
写作规划 → 故事梳理 → 论文画图 → 论文写作 → 论文评审
```

另分享科研软技能：学术报告技巧、日常科研习惯。

### 1.4 能教什么 / 不能教什么（P5）

| 能教 | 不能教 |
|---|---|
| 阐明 Research project 的步骤和过程：选题与 Idea 设计的流程、方法论；进行实验的流程、方法论；写论文的步骤流程。解释规则，分享经验。 | 想 Idea 的能力（创新能力、技术能力）；进行实验的能力（编程、分析、技术经验、沟通）；论文写作能力（表达、英语、艺术、时间规划）。这些只能通过实践经验培养。 |

这条边界是硬约束：技能可以教流程、给检查表、做诊断，但不能承诺替用户产生创新能力或替代实践训练。

### 1.5 如何从课程受益（P6）

```text
从课程学习科研流程与每个步骤的方法论
→ 根据自己的经验思考并总结方法论
→ 通过【实践】熟悉研究方法
→ 【重要】总结【你自己的】研究方法
```

---

## 2. 建立领域视野（P8–P10，P48–P65）

### 2.1 定义（P8）

领域（field）：特定科研方向，例如 3D reconstruction、Novel view synthesis。

视野包含两面：

1. **技术演变**：milestone papers、技术随时间的演变。
2. **重要问题**：终极目标、现有水平、未解决的问题、当前热点问题。

### 2.2 视野支撑什么（P9）

领域视野是五项科研工作的基础：

- 课题选择；
- 方法设计；
- 实验中迭代；
- 故事梳理；
- 论文写作。

最终目标是成为该领域的专家。

### 2.3 建立视野的流程（P10）

```text
确定 milestone papers
→ 查找每个里程碑前后的论文
→ 阅读它们的问题、pipeline、技术见解
→ 分别整理：技术演变轨迹 / 热点问题的演变
→ 跟踪并预测新技术、新问题
```

### 2.4 多视角重建示范案例（P49–P59）

这是课件用来示范“如何建立视野”的案例，不是所有领域的固定内容。

**两个驱动问题（P49）**：

- 这个领域的技术如何随时间演变？
- 现在还有哪些重要问题？

**技术时间线（P53，示例）**：

| 年份 | 里程碑 | 关键思路 |
|---|---|---|
| 2016 | COLMAP | 传统 MVS 集大成；解决多数相机位姿与稀疏观测深度 |
| 2018 | MVSNet | probability volume / cost volume + CNN |
| 2020 | NeRF | neural radiance field / 全局表示 + differentiable rendering |
| 2021 | Input-Level Inductive Biases | 把 multi-view images 视为 tokens，用 ViT tokens 预测 depth |
| 2023–24 | DUSt3R | 图像 tokenize 后用 ViT 融合 |
| 2023–24 | CAT3D | Multi-view Diffusion Model 融合 |

**重要问题（P51，示例）**：One-2-3-45 代表的单图到 3D；稀疏视角重建。

**识别 milestone（P54）**：

- 找引用次数最多的论文，按日期排序；
- 请有经验的研究人员建议。

**两个里程碑之间怎么读（P55）**：

- 向前：读该里程碑引用的基础工作；
- 向后：读引用它的衍生工作；
- 工具：Connected Papers 的 Prior works / Derivative works。

**时间轴思维导图三步（P57）**：

1. 初始化时间轴，逐篇阅读：问题 / pipeline / 技术见解；
2. 按创新性标记 milestone 与 follow-up；
3. 总结每个里程碑的技术范式，以及 follow-up 的改进。

**热点与未解问题（P59）**：

- 按年份记录热点；
- 回答四问：终极目标是什么？当前水平到哪？哪些问题未解？当前热点是什么？

### 2.5 视野大小与能力匹配（P64–P65）

- 视野大小应与能力匹配；初学者先窄视野，能力和阅读量增长后再扩大。
- 额外建立视野的方式：听知名研究者演讲、与实验室伙伴/Senior advisor/专家交流。

> 适配：非计算机领域可把“milestone paper”替换为“标志性方法/标准/关键数据集/理论突破”，但“向前追基础、向后追衍生、按时间轴整理”的结构不变。

---

## 3. 初始化科研课题（P12–P19）

### 3.1 先把 setting 说清楚（P12）

选题前必须回答：

- Project setting 是什么：输入是什么、输出是什么、约束是什么？
- 要解决的 failure case 是什么？
- 这个 failure case 背后的 technical challenge 是什么？

一句话模板：

```text
在【对象/任务】上，给定【输入】和【约束】，产出【输出】；
现有【方法】在【failure case】上失效；
背后挑战是【technical challenge】。
```

### 3.2 好课题的三条标准（P13）

1. 发展空间大，且竞争小；
2. 任务难度与个人能力匹配：过难无法完成，过简单缺乏锻炼；
3. 影响大。

### 3.3 找好课题的四步（P14）

1. 建立领域视野；
2. 列出领域的重要问题，判断当前应该解决哪一个；
3. 评估竞争与发展空间，并匹配自己的能力；
4. Aim High：技术风险较大的课题可能有更高收益；努力完成达到自身能力极限的课题。

### 3.4 Junior / Senior 的差异（P15）

| 阶段 | 共同点 | 风险 | 任务定义 |
|---|---|---|---|
| Junior | 发展空间大、竞争小、well-defined | 技术风险小 | well-defined |
| Senior | 发展空间大、竞争小、well-defined | 可承担高风险 | 可做 ill-defined task |

### 3.5 方法设计是什么、为什么（P17）

选题后设计新颖的 pipeline 以达 SOTA。系统的方法设计能：

- 真正解决问题；
- 增强动机和 story；
- 保证 novelty；
- 提高 technical insights。

### 3.6 方法设计四步循环（P18）

```text
用第一性原理分析：当前 SOTA 为什么不足？
→ 依据原因设计方法
→ 判断设计是否合理
→ 读论文 / 讨论 / 做实验来改进
→（回到第一步）
```

### 3.7 方法设计三要点（P19）

1. 不止要 Work，还要有技术创新；
2. 尽量在 pipeline 层面解题，而不是只调参；
3. 检查是否产生新知识、新认识、新观点。

> 适配：非 pipeline 研究可把“pipeline 改动”映射为实验系统改动、理论证明链、数据处理链或决策流程；仍然要求“原因 → 改动 → 合理性 → 新认识”四段齐全。

---

## 4. 实验中迭代提升方法（P21–P26）

### 4.1 实验设计是什么（P21）

规划实验，以实现或提升 technical idea，并达到 SOTA。两个好处：

- 明确科学目的；
- 降低实验难度、提高效率。

### 4.2 核心：减少 exploration points（P22）

- **拆 pipeline**：从可控的 idea 开始，逐步加入需要探索/创新的模块；
- **拆 setting**：从简单设定开始，逐步增加难度直到真实 setting；
- **排优先级**：按 exploration point 的重要性排序，先验证最关键的假设。

### 4.3 初始 idea 通常不 work（P24）

实际路径往往不是“Good results”，而是“Not working”。这是常态，不是失败信号。

### 4.4 把改进类比 SGD（P25）

```text
提出 idea ⇄ 改进 idea

目标函数 1：|| Evaluate(idea) ||
目标函数 2：|| Experiment(idea) – Target result ||

误差 → 计算梯度 → 改进 idea → 循环
```

课件没有定义具体范数、优化器或更新公式，不要擅自补全成某个具体算法。

### 4.5 两条改进路径（P26）

| 路径 | 做什么 | 产出 |
|---|---|---|
| Learning | 从论文和研究者学习 | 尽可能多的 idea variants |
| Experiment | 实现 idea → 设计实验 → 分析结果 | 获得 gradient，据此改进 |

两条路径不是二选一：先学出候选，再用实验筛选和校正。

---

## 5. 论文写作（P28–P46）

### 5.1 写作 9 步（P28）

| 步骤 | 内容 |
|---|---|
| 1 | 画清楚的 pipeline figure 草图（理清方法流程），梳理论文 story，写一版 introduction 初稿 |
| 2 | 列出 comparison experiments 和 ablation studies，并开始做 |
| 3 | 写 method，同时做实验 |
| 4 | 改 introduction 和 method，同时做实验 |
| 5 | 实验差不多后，写 experiment |
| 6 | 写 related work |
| 7 | Review 论文，改 introduction、method、experiment |
| 8 | 写 abstract，取论文名字 |
| 9 | 反复 review、反复改 |

**为什么需要写作规划（P29）**：大幅提高投稿率；让做论文更轻松，避免最后几天熬夜。

### 5.2 故事梳理（P30–P33）

先整理论文方法流程：

```text
输入 → 模块1 → 中间输出1 → 模块2 → …… → 模块N → 输出
```

用文字描述 pipeline，再选择布局画简单流程图。

**4K4D 示范（P31–P33）**：

```text
点云序列 → 4D feature grid → 每个点的 feature
→ 几何/外观网络 → 每个点的 density / color
→ 点云渲染器 → 图片
```

随后回答四个 story 问题：

1. pipeline 有哪些贡献、新任务或挑战？
2. 这些贡献如何解决挑战，带来什么好处？
3. 产生了哪些新 insights？
4. 如何由以往方法引出这些 challenge 和 insights？

最后按“任务 → 旧方法与挑战 → 本文贡献 → 技术优势/insights”概述 story。

### 5.3 论文画图（P34–P40）

四类图：pipeline 图、teaser 图、定量结果图、定性结果图。图画得好能提高中稿率。

Pipeline 图的五步：

1. 文字描述；
2. 选布局、画草图；
3. 可视化输入、模块、中间输出、输出；
4. 配色；
5. 优化简洁布局，避免大空白。

**4K4D 的公式与术语（P37–P40，示范）**：

- `f = Θ(x,t)`：把时空点映射到外观/几何；
- Radius MLP → `r`（point radius）；
- Density MLP → `σ`（density）；
- SH MLP → spherical harmonics → `c_sh`（依赖视角方向）；
- Discrete IBR → `c_ibr`；
- `c_sh` 与 `c_ibr` 相加得视角相关 RGB `C`；
- Differentiable Depth Peeling 多 pass 渲染输出图片。

### 5.4 Method 怎么写（P41）

1. 先有 pipeline 草图；
2. 按模块规划 Method 的 subsections；
3. 每个 subsection 先说明：给定输入、步骤、输出；
4. 再解释：motivation、technical advantages。

**Neural Body 示范（P42–P44）**：

- SMPL posed 3D mesh 有 6890 个顶点；
- 结构化 latent codes：`Z = {z₁, z₂, …, z₆₈₉₀}`，每个 `z` 维度为 16；
- 帧参数记为 `S_t`；
- Code diffusion：5 mm × 5 mm × 5 mm 体素，SparseConvNet 多尺度 2×/4×/8×/16×；
- 从第 5/9/13/17 层插值并 concatenate，trilinear 查询得到 `ψ(x, Z, S_t)`；
- `σ_t(x) = M_σ(ψ(x, Z, S_t))`，`M_σ` 为四层 MLP；
- `c_t(x) = M_c(ψ(x, Z, S_t), γ_d(d), γ_x(x), ℓ_t)`，`M_c` 为两层 MLP，`ℓ_t` 维度 128，`γ_d`/`γ_x` 为 positional encoding。

### 5.5 自评 checklist（P45–P46）

自评的目的：在投稿前用审稿人视角检查论文。

| 类别 | 检查问题 |
|---|---|
| 技术贡献 | failure case 是否常见？技术是否 well-explored？贡献是否足够？ |
| 写作清楚 | Introduction 是否清楚？pipeline figure 是否清楚？细节是否可复现？每个模块是否有 motivation？ |
| 效果足够 | 相对以往方法提升多少？是否 impressive？ |
| 实验充分 | ablation 是否充分？baseline 是否合适？metric 是否合适？是否在复杂数据上验证？ |
| 方法合理 | setting 是否现实？技术是否有缺陷？模块是否鲁棒？benefit 是否被更强的 limitation 抵消？ |

---

## 6. 作业（P66）

正式作业只有一个：

> 在自己的研究方向上整理一份**时间轴思维导图**，并总结该方向在当前时间点**仍未解决的重要问题**；提交 PDF。

课件给出的示例是“多视角重建时间轴思维导图”。

课件没有规定页数、模板、截止日期或额外附件，不要替用户补这些要求。

以下任务是过程性练习或 Project 里程碑，不是 P66 正式作业：

- 按 P60–P63 的解析树读一篇论文并回答各树问题；
- 针对开源 baseline 设一个简单改进并实现，以目标驱动读代码；
- 在新数据/setting 上跑 SOTA，找 failure case，回答 setting/input/output 的独特性；
- 列 techniques 脑图、组合 pipelines、讨论并做验证实验；
- 做 demo/application，扩大影响；
- 按 9 步完成论文投稿。

---

## 7. QA 环节（P68–P78）

### Q1（P68）：代码怎么读？

不要无目的地读代码，效率低。给论文算法设一个简单改进任务并实现；改进目标会驱动你理解代码，同时提升编程能力。

### Q2（P69）：怎么从零建立领域认知？

做时间轴思维导图（同 P57 三步法）。

### Q3（P70）：新领域或超前课题怎么上手？

先跑开源 baseline，再设一个小改进。

### Q4（P71）：怎么选研究方向？

先明确自己想做的 product，再看 research 与 product 之间的 gap。

### Q5（P72）：怎么选新课题？

回到 P14 的四步：视野 → 重要问题 → 竞争/空间/能力匹配 → Aim High。

### Q6（P73–P75）：怎么从工程问题提炼科学问题？

```text
判断当前工程方案还有多大提升空间
→ 找到其中重要的问题
→ 用第一性原理分析其本质
```

### Q7（P76）：怎么判断课题有没有价值？

依赖领域视野、实验经验、与同行讨论。

### Q8（P77）：怎么确定解决方案？

沿 P18 的方法设计四步走。

### Q9（P78）：海量技术路线怎么选？

仍依赖领域视野、实验经验、讨论。

---

## 8. Project 时间规划（P79）

课件以 CVPR（2024-11-15 截稿）为例倒推：

| 节点 | 日期 | 任务 |
|---|---|---|
| 启动 | 5/25 | 启动 Project |
| 节点 1 | 5/31 | 规划 task、建立领域视野、确认 SOTA、评估竞争/发展空间/能力匹配 |
| 节点 2 | 6/15 | 在新数据/setting 跑 SOTA，找 failure case 和 technical challenge，回答 setting/input/output 的独特性 |
| 节点 3 | 6/31* | 第一性原理分析 SOTA 为何不 work；列 techniques 脑图、组合 pipelines、讨论 |
| 节点 4 | 8/31 | 用 SGD 式循环验证与迭代 |
| 节点 5 | 9/30 | 做 demo/application，扩大影响 |
| 节点 6 | 11/15 | 按 9 步完成论文至投稿 |

`*` 课件原文写的是“2024 年 6 月 31 日”，这是无效日期，HTML 也特别保留了这一写法。不要静默改成 6 月 30 日；引用时标 `[课件原文待确认]`，并提示用户按实际年份和月份核对。

## 9. Panel Discussion（P80）

课件列出的讨论问题：

- 课程如何帮助科研入门？
- 入门时最大的困难是什么，怎么解决？
- Project 陷入困难或停滞怎么办？
- 科研能力什么时候会快速提升？
- 为什么选择现在的研究方向？
- 是否会为了就业选择工业界热门方向？
- 如何寻找科研的动力和热情？

---

## 10. 术语与公式速查

### 10.1 流程术语

Research project、field/domain、milestone paper、follow-up、SOTA、project setting、input/output、failure case、technical challenge、technical idea、first principles、pipeline、novelty、insight、technical contribution、technical advantage、Aim High、well-defined/ill-defined task、exploration point、SGD process、idea variant、baseline、comparison experiment、ablation study、evaluation metric、demo/application、product–research gap。

### 10.2 写作与阅读术语

Abstract、Introduction、Method、Experiments、Related Work、pipeline figure、teaser、quantitative/qualitative results、motivation、failure/limitation、technical reason、why work、review、投稿。

### 10.3 课件出现的技术案例术语

4D feature grid、point cloud sequence、density、color、Radius/Density MLP、SH（spherical harmonics）、Discrete IBR、view-dependent RGB、differentiable rendering / depth peeling；SMPL、posed 3D mesh、latent code、implicit field、code diffusion、SparseConvNet、3D sparse convolution、multi-scale volume、voxel、trilinear interpolation、positional encoding、latent embedding。

### 10.4 公式的读法边界

- `|| Evaluate(idea) ||`、`|| Experiment(idea) – Target result ||`：只有目标函数的示意，没有定义范数、优化器和更新规则。
- 4K4D 与 Neural Body 的公式用于示范“如何把方法拆成模块”，不代表用户研究方向必须使用同样的表示。

---

## 11. 页码索引（HTML 记录）

| 页码 | 内容 |
|---|---|
| P1 | 封面/课程身份 |
| P2 | 低年级痛点与课程目标 |
| P3–P4 | 科研三阶段流程与软技能 |
| P5 | 能教/不能教边界 |
| P6 | 学习—反思—实践—形成个人方法论 |
| P7 | 第一部分章节页 |
| P8 | 领域视野定义与两面 |
| P9 | 视野支撑五项工作 |
| P10 | 建立视野流程 |
| P11 | 章节页 |
| P12 | setting、failure case、technical challenge |
| P13 | 好课题三标准 |
| P14 | 找好课题四步 |
| P15 | Junior/Senior 风险与任务定义 |
| P16 | 章节页 |
| P17 | 方法设计是什么/为什么 |
| P18 | 方法设计四步 |
| P19 | 方法设计三要点 |
| P20 | 第二部分章节页 |
| P21 | 实验设计定义与好处 |
| P22 | 减少 exploration points |
| P23 | 章节页 |
| P24 | 初始 idea 常不 work |
| P25 | 改进类比 SGD |
| P26 | learning 与 experiment 两条路径 |
| P27 | 第三部分章节页 |
| P28 | 写作 9 步 |
| P29 | 写作规划的价值 |
| P30 | 以 pipeline 草图梳理 story |
| P31–P33 | 4K4D 案例与 story 四问 |
| P34–P40 | 四类论文图与 4K4D 图的逐步完善 |
| P41 | Method 写作步骤 |
| P42–P44 | Neural Body Method 案例 |
| P45 | 自评目的 |
| P46 | 五类自评 checklist |
| P47 | 第四部分章节页 |
| P48 | 领域视野回顾 |
| P49 | 多视角重建的两个问题 |
| P50 | 为什么需要视野 |
| P51 | 案例中的重要问题 |
| P52 | 建立视野流程 |
| P53 | 多视角重建技术时间线 |
| P54 | 识别 milestone papers |
| P55 | 里程碑之间查论文 / Connected Papers |
| P56、P58 | 时间轴思维导图完整案例 |
| P57 | 梳理技术脉络三步 |
| P59 | 按年份记录热点并总结四问 |
| P60 | 论文解析树引入 |
| P61 | Abstract 树 |
| P62 | Introduction 树 |
| P63 | Method / Experiments 树 |
| P64 | 视野规模与能力匹配 |
| P65 | 演讲与交流 |
| P66 | 作业 |
| P67 | QA 章节页 |
| P68–P70 | 入门 QA：读代码、建立领域、上手新方向 |
| P71 | 选研究方向 |
| P72–P76 | 选课题、工程提炼科学问题、价值判断 |
| P77–P78 | 选解决方案、海量路线 |
| P79 | Project 倒推计划 |
| P80 | Panel Discussion |
| P81 | 致谢 |
