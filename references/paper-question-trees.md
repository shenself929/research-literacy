# 论文解析树

来自课件 P60–P63 的阅读方法：把“读论文”变成“回答问题”。每棵树先让用户自己答，再对照论文修正。

使用方式：

1. 先读摘要，填 Abstract 树；
2. 读引言，填 Introduction 树；
3. 读方法，填 Method 树；
4. 读实验，填 Experiments 树；
5. 每填一栏，标出证据位置：`§`、`Fig.`、`Table`、附录、代码 `file:line`。

答案指不回来源时写 `[待核对]`；论文没写的写“论文未说明”，不要用常识补。

---

## 1. Abstract 树（P61）

| 问题 | 填什么 | 证据位置 |
|---|---|---|
| Task | 论文要解决什么任务？ | 摘要第 1–2 句 |
| Challenge | 以往方法的技术挑战是什么？ | 摘要中 “however/because” 附近 |
| Key insight / motivation | 一句话核心洞察是什么？ | 摘要中 “we observe/we find/our key idea” |
| Technical contributions | 每条贡献做了什么？带来什么好处？ | 摘要贡献句 |
| Experiment | 用什么实验证明？ | 摘要最后 1–2 句 |

注意区分两种“insight”：

- **high-level insight**：对整个问题的新理解（为什么以前不行）；
- **technical contribution**：具体模块/设计（怎么做到的）。

摘要常把两者压成一句话，拆开填。

**填表示例（4K4D，P31–P33）**：

> 来源说明：4K4D 的 pipeline 术语（点云序列、4D feature grid、几何/外观网络、density/color、点云渲染器、Differentiable Depth Peeling）来自课件；下表中 Task/Challenge/Experiment 的措辞是技能为示范“怎么填”而概括的，**不是课件原句**。

| 字段 | 内容 |
|---|---|
| Task | 从多视角视频重建可渲染的动态 3D 场景（技能概括） |
| Challenge | 动态场景的表示与高效渲染难以兼顾（技能概括） |
| Key insight | 用 4D feature grid 表示时空，再用点渲染输出（课件 pipeline 的概括） |
| Contributions | 4D 表示、几何/外观网络、可微深度剥离渲染（课件术语） |
| Experiment | 定量/定性对比与渲染质量（技能概括） |

这是填表示例，不是要求所有论文都长这样，也不能当作课件对 4K4D 的完整评价。

---

## 2. Introduction 树（P62）

| 问题 | 填什么 | 证据位置 |
|---|---|---|
| Task / application | 任务是什么？有什么应用价值？ | 第 1 段 |
| Challenge | 有哪几个具体挑战？ | 第 2–3 段 |
| Previous methods | 每个挑战下，以往方法怎么做？ | 对应段落 |
| Failure case | 它们具体在哪里失败？ | 对应段落/图 1 |
| Technical reason | 为什么失败？机制层面的原因是什么？ | 对应段落 |
| Our pipeline | 本文的整体流程是什么？ | 方法总览段/图 1 |
| Contributions | 每条贡献怎么做、有什么 advantage/insight？ | 贡献列表 |
| Demos / applications | 有什么演示或应用？ | 最后一段/项目页 |

关键检查：

- “挑战”是否被拆成多个具体问题，而不是一句“性能不好”；
- 每个 failure case 是否对应一个 technical reason；
- 贡献是否逐条回应前面的挑战，而不是各说各话。

---

## 3. Method 树（P63）

### 3.1 Overview

| 问题 | 填什么 |
|---|---|
| 输入是什么？ | 数据类型、形状、前提 |
| 输出是什么？ | 预测/重建/决策结果 |
| 有哪几个步骤？ | 按数据流列 3–7 步 |
| 每步的中间输出是什么？ | 变量名、维度、含义 |

### 3.2 每个模块

对每个 subsection 填：

| 问题 | 填什么 |
|---|---|
| Motivation | 为什么需要这个模块？不加上一步会怎样？ |
| 做法 | 具体操作是什么？ |
| Why work | 为什么这样能解决问题？ |
| Technical advantage | 相比替代方案好在哪？代价是什么？ |

课件要求 Method 的每个小节先写“给定输入 → 步骤 → 输出”，再写 motivation 和 technical advantage。读论文时反过来检查：作者有没有把这三件事说清。

**填表示例（Neural Body，P42–P44）**：

> 来源说明：模块名、公式符号、维度（6890 顶点、16 维 latent、128 维 `ℓ_t`、四层/两层 MLP）来自课件；Motivation 列的措辞是技能概括，不是课件原句。

| 模块 | Motivation | 做法 | 输出 |
|---|---|---|---|
| Structured latent codes | 把人体先验注入辐射场 | SMPL 6890 顶点各一个 16 维 latent | `Z={z₁,…,z₆₈₉₀}` |
| Code diffusion | 把顶点特征扩散到空间 | 5 mm 体素 + SparseConvNet 多尺度 + trilinear 查询 | `ψ(x,Z,S_t)` |
| Density regression | 预测几何 | 四层 MLP `M_σ` | `σ_t(x)` |
| Color regression | 预测视角相关颜色 | 两层 MLP `M_c` + positional encoding | `c_t(x)` |

这份表是“怎么读方法”的示范，不是要求用户领域也有 latent code。

---

## 4. Experiments 树（P63）

| 问题 | 填什么 | 证据位置 |
|---|---|---|
| Comparison | 和哪些方法比？为什么选这些 baseline？ | 实验设置 |
| Metrics | 用什么指标？指标定义是什么？ | 实验设置 |
| Main results | 主结果提升多少？在哪些数据/条件下？ | 主表 |
| Ablation | 每个核心组件去掉后掉多少？ | 消融表 |
| Design choices | 每个设计选择（超参、模块、训练策略）影响多大？ | 消融/敏感性分析 |
| Core contributions | 哪条贡献被哪个实验直接支持？ | 贡献—实验对应表 |
| Failure cases | 什么条件下方法失效？ | 定性图/讨论/附录 |

检查三件事：

1. 每条贡献是否有对应实验；
2. baseline 是否覆盖了真正的竞争方法；
3. 提升是否在复杂/真实 setting 下仍然成立。

---

## 5. 跨领域映射

| 课件词 | 实验科学 | 理论 | 临床 | 社科 |
|---|---|---|---|---|
| pipeline | 实验流程 | 证明链 | 诊疗路径 | 数据/识别流程 |
| module | 实验步骤 | 引理 | 干预环节 | 测量/模型组件 |
| ablation | 单因素去除 | 去掉假设 | 去掉某分层规则 | 去掉某控制变量 |
| comparison | 阳性对照 | 已有界/定理 | 标准疗法 | 替代识别策略 |
| metric | 效应量/误差 | 界的紧度 | 主要终点 | 偏差/覆盖率 |

映射时写一句“这里把 module 对应为实验步骤，因为……”，不要假装课件原句就是这么说的。

---

## 6. 输出格式

给用户的解析结果按这个结构：

```markdown
# 论文解析：<标题>

## 一句话
<Task + challenge + insight>

## Abstract 树
<表>

## Introduction 树
<表>

## Method 树
<表>

## Experiments 树
<表>

## 贡献—证据对照
| 贡献 | 证据 | 强度 |

## 未解决/待核对
- ...
```

最后两节不能省：没有证据的贡献要降级，没读到的部分要标出来。
