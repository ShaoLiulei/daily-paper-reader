---
title: "The Cerebellar Engine: Multiscale Digital Brain Co-simulations Reveal How Cerebellar Spiking Architecture Shapes Cortical Coherence"
title_zh: 小脑引擎：多尺度数字大脑联合仿真揭示小脑脉冲架构如何塑造皮层相干性
authors: "Geminiani, A., Meier, J. M., Perdikis, D., Ouertani, S., Casellato, C., Ritter, P., D'Angelo, E. U."
date: 2026-04-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.02.715849v1.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 下橄榄-小脑微回路的脉冲神经网络架构
tldr: 本研究旨在揭示细胞活动如何跨尺度影响全脑动力学，重点探讨了小脑在感觉运动集成中的作用。研究者开发了一种多尺度数字大脑共模拟器，将小脑脉冲神经网络嵌入小鼠虚拟大脑，并与皮层模块双向连接。通过模拟发现，小脑内的脉冲处理是驱动初级运动皮层与感觉皮层间伽马频段相干性的关键。该成果为小脑如何促进感觉运动预测提供了机械论解释，并为多尺度脑科学研究开辟了新路径。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-001.webp\", \"caption\": \"\", \"page\": 5, \"index\": 1, \"width\": 1875, \"height\": 998}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 1875, \"height\": 998}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-003.webp\", \"caption\": \"\", \"page\": 5, \"index\": 3, \"width\": 1875, \"height\": 497}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 1841, \"height\": 970}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 1841, \"height\": 970}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 1841, \"height\": 970}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-007.webp\", \"caption\": \"\", \"page\": 10, \"index\": 7, \"width\": 1881, \"height\": 917}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-008.webp\", \"caption\": \"\", \"page\": 11, \"index\": 8, \"width\": 1881, \"height\": 878}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-009.webp\", \"caption\": \"\", \"page\": 12, \"index\": 9, \"width\": 1881, \"height\": 1380}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-010.webp\", \"caption\": \"\", \"page\": 12, \"index\": 10, \"width\": 1881, \"height\": 458}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-011.webp\", \"caption\": \"\", \"page\": 14, \"index\": 11, \"width\": 1879, \"height\": 709}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-04-02-715849-v1/fig-012.webp\", \"caption\": \"\", \"page\": 15, \"index\": 12, \"width\": 1879, \"height\": 676}]"
motivation: 探索细胞层面的神经活动如何跨尺度驱动全脑动力学，并阐明小脑在感觉运动集成中的具体因果机制。
method: 开发了一种多尺度数字大脑共模拟器，将小脑微回路脉冲神经网络与基于图谱的小鼠虚拟大脑皮层模块进行双向耦合。
result: 模拟实验表明，小脑回路内的脉冲处理过程是维持M1和S1皮层间伽马频段相干性及感觉运动集成的核心要素。
conclusion: 研究证实了小脑在促进皮层间感觉运动关联中的关键作用，并为研究大脑生理与病理状态提供了一种有效的多尺度建模方法。
---

## 摘要
细胞活动对大规模大脑动力学的影响被认为决定了大脑的功能与疾病，然而跨尺度的神经机制因果关系仍不清楚。最近有报道称，小脑在感觉运动整合过程中会影响全脑动力学。为了揭示其潜在机制，我们开发了一种多尺度数字大脑联合仿真器，其中下橄榄-小脑微回路的脉冲神经网络被嵌入到小鼠虚拟大脑中，并利用基于图谱的远程连接组与其他节点相连。脉冲下橄榄-小脑网络与其他速率编码模块之间的参数和双向接口经过调整，以匹配初级感觉和运动皮层（M1 和 S1）功率谱密度及神经元脉冲率的实验数据。随后，通过在计算机内（in silico）损伤关键电路连接，分析了小脑回路在感觉运动整合中的作用。仿真结果表明，小脑回路内的脉冲处理是解释感觉运动整合期间 M1 和 S1 之间伽马频段相干性的关键。这些结果为小脑如何促进相关皮层模块中感觉运动偶联的形成提供了机械论解释，这也是其在感觉运动预测中发挥关键作用的基础。从更广泛的角度来看，这种建模方法为研究与特定细胞和微回路特性相关的大脑生理及病理状态提供了多尺度研究的新视角。

## Abstract
The impact of cellular activities on large-scale brain dynamics is thought to determine brain functioning and disease, yet the causal relationships of neural mechanisms across scales remain unclear. Recently, the cerebellum has been reported to affect whole-brain dynamics during sensorimotor integration. To disclose the underlying mechanisms, we have developed a multiscale digital brain co-simulator, in which a spiking neural network of the olivo-cerebellar microcircuit is embedded in a mouse virtual brain and wired with other nodes using an atlas-based long-range connectome. Parameters and bi-directional interfaces between the spiking olivo-cerebellar network and other rate-coded modules were tuned to match experimental data of primary sensory and motor cortex (M1 and S1) power spectral densities and neuronal spiking rates. Then, the role of the cerebellar circuitry on sensorimotor integration was analyzed by lesioning critical circuit connections in silico. Simulations showed that spike processing within the cerebellar circuit is key to explaining the gamma-band coherence between M1 and S1 during sensorimotor integration. These results provide a mechanistic explanation of how the cerebellum promotes the formation of sensorimotor contingencies in relevant cortical modules as the basis of its critical role in sensorimotor prediction. On a broader perspective, this modelling approach opens new perspectives for the multiscale investigation of brain physiological and pathological states in relation to specific cellular and microcircuit properties.

---

## 论文详细总结（自动生成）

### 论文结构化总结：小脑引擎——多尺度数字大脑联合仿真研究

#### 1. 核心问题与研究动机
*   **核心问题**：探讨细胞层面的神经活动如何跨越空间和时间尺度，驱动全脑尺度的动力学，特别是小脑微回路的脉冲架构如何塑造大脑皮层间的相干性（Coherence）。
*   **研究动机**：感觉运动集成（Sensorimotor Integration）是复杂行为的基础，实验表明小脑在其中起关键作用，但其微观脉冲处理如何影响宏观皮层同步（如 M1 和 S1 之间的伽马频段相干性）的因果机制尚不明确。传统的单一尺度模型无法同时兼顾微观回路细节与全脑连接。

#### 2. 方法论：多尺度联合仿真框架
*   **核心思想**：构建一个“多尺度数字大脑联合仿真器”，将高精度的**脉冲神经网络（SNN）**嵌入到**全脑平均场模型（Mean-field Model）**中。
*   **关键技术细节**：
    *   **宏观尺度（TVMB）**：基于 Allen 小鼠大脑连接组图谱，使用 Wilson-Cowan 神经质量模型模拟皮层和大部分皮层下区域。
    *   **微观尺度（NEST）**：使用 E-GLIF（扩展广义漏电积分发放）神经元模型构建下橄榄-小脑微回路，包含颗粒细胞、Purkinje 细胞、小脑核团（CN）等。
    *   **跨尺度接口**：
        *   **TVMB → NEST**：将宏观节点的活动速率通过线性变换转为泊松脉冲序列，输入 SNN。
        *   **NEST → TVMB**：计算 SNN 输出群体的瞬时频率，通过低通滤波集成回宏观模型。
    *   **参数推断（SBI）**：利用基于模拟的推理（Simulation-Based Inference）算法，自动拟合模型参数，使仿真结果匹配实验观测到的功率谱密度（PSD）和相干性。

#### 3. 实验设计
*   **实验场景**：模拟小鼠的**自由胡须运动（Free Whisking）**，这是一个典型的感觉运动集成任务。
*   **基准（Benchmark）**：以 Popa et al. (2013) 的电生理实验数据为基准，重点关注小脑失活后 M1-S1 伽马相干性的下降。
*   **对比方法与消融实验**：
    *   **CerebON vs. CerebOFF**：验证小脑存在与否对皮层相干性的影响。
    *   **虚拟损伤（Virtual Lesions）**：在 SNN 内部切断特定连接（如 MOStoCN 兴奋路径、PCtoCN 抑制路径、MLI 抑制路径），观察对皮层动力学的反馈。

#### 4. 资源与算力
*   **算力平台**：研究指出仿真和 SBI 拟合是在柏林健康研究所（BIH）的高性能计算集群（HPC）上完成的。
*   **细节说明**：文中未明确给出具体的 GPU/CPU 型号、核心数量及单次训练/仿真的具体时长。但考虑到多尺度联合仿真的复杂性，此类计算通常需要大规模并行处理能力。

#### 5. 实验数量与充分性
*   **实验规模**：每种损伤条件下均进行了 10 组独立的仿真运行（每组包含双侧半球数据），并进行了统计学显著性检验（t-test, FDR 校正）。
*   **充分性评价**：实验设计较为充分。研究不仅复现了已有的实验现象，还通过多组消融实验（针对小脑内部四种不同的突触连接）深入探讨了内部机制。使用了 SBI 进行参数空间搜索，增加了结果的客观性和鲁棒性。

#### 6. 主要结论与发现
*   **小脑是频率转换器**：小脑能够增强输入信号的伽马频段功率并抑制西塔（Theta）频段功率。
*   **脉冲处理的关键性**：M1-S1 之间的伽马相干性并非简单的信号透传，而是依赖于小脑内部的脉冲处理。
*   **路径分工**：
    *   **直接路径（苔藓纤维-CN）**：是维持皮层间相干性的必要条件。
    *   **间接路径（Purkinje 细胞-CN）**：通过抑制作用实现“去相关”，优化信息容量，对感觉运动预测至关重要。
*   **因果链条**：小脑微回路的损伤会改变 CN 的脉冲同步性，进而通过丘脑皮层环路破坏 M1 和 S1 的功能耦合。

#### 7. 优点（亮点）
*   **跨尺度融合**：首次实现了详细的小脑脉冲模型与全脑虚拟大脑模型的双向闭环耦合。
*   **机械论解释**：不仅观察到现象，还解释了小脑如何通过内部脉冲相位锁定（Phase-locking）来调节远端皮层同步。
*   **高度生物学可信度**：模型参数基于解剖图谱和单细胞电生理数据，具有很强的生物学约束。

#### 8. 不足与局限
*   **连接组限制**：Allen 图谱对小脑与非运动区（如关联皮层）的连接描述可能不完整，限制了模型在认知功能研究中的应用。
*   **接口滤波效应**：NEST 到 TVB 的接口涉及低通滤波，可能会损失部分极高频的脉冲细节。
*   **任务简化**：胡须运动路径被简化为最小化路径，未考虑更复杂的并行子环路补偿机制。
*   **临床转化**：虽然为疾病研究提供了工具，但目前主要基于小鼠模型，向人类大脑的转化仍需进一步验证。

（完）
