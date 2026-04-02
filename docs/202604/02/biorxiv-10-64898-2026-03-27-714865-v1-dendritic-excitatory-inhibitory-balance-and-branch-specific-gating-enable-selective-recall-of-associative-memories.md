---
title: Dendritic excitatory-inhibitory balance and branch-specific gating enable selective recall of associative memories
title_zh: 树突兴奋-抑制平衡与分支特异性门控实现了关联记忆的选择性提取
authors: "Berger, S., Agnes, E. J."
date: 2026-03-31
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.27.714865v1.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 生物物理脉冲电路与联想记忆
tldr: 本研究探讨了生物物理神经元电路如何实现联想记忆。通过构建具有分级树突和结构化递归相互作用的模型，发现局部树突的兴奋-抑制平衡能产生类二进制状态，而分支特异性抑制则充当门控，实现对重叠记忆的选择性提取。该框架揭示了树突动力学在扩大吸引子盆地和减少干扰中的关键作用，为解释树突成像数据提供了理论基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-27-714865-v1/fig-001.webp\", \"caption\": \"FIG. 2. Binary-to-biophysical mapping enables associative recall through dendritic EI balance. A, Membrane-potential fixed points, V (top; cf. Fig. 1C), the resulting firing rate (middle), and the corresponding binary state (bottom) as a function of excitatory input for different levels of inhibition. B, State-space of dendritic membrane potential (cf. Fig. 1D). The dashed line separates hyperpolarised (S = 0) and depolarised (S = 1) states. C, Schematic of the recurrent excitatory-inhibitory network. Key parameters shown: N, number of neurons; a, activity level; c, connection density; p, number of stored patterns. Superscripts E and I denote excitatory and inhibitory populations. D, Spike times of excitatory (red) and inhibitory (blue) neurons (top) and memory overlap (bottom) as a function of time. Shaded areas indicate periods of external stimulation. E, Examples of membrane potential (top) and currents (bottom) during active (left) and inactive (right) periods of a neuron during recall of two memory patterns (cf. panel D). F, Histograms of C(IE, II) for excitatory (left) and inhibitory (right) neurons, separated into active (black) and inactive (grey) populations. G, Distribution of interspike intervals (ISIs) for different initial condition sizes, defined as the fraction of the memory pattern that is externally activated. Key parameters: ν0, firing-rate during active recall; T, period of external activation; nT, interval spanning n activation periods. H, Distribution of the coefficient of variation of interspike intervals, CVISI (left), and neuronal firing rates (right). I, Examples of dendritic membrane-potential trajectories for different presentation times. J, Overlap between the final network state and the target memory pattern as a function of initial condition size (cf. panel G). K, Reliability of memory recall, defined as one minus the smallest initial condition size for which the average overlap exceeds 0.9 (from panel J), as a function of presentation time. Higher reliability indicates that smaller fractions of a memory pattern are sufficient to trigger full recall. Pink lines show the equivalent binary network without (dashed) and with (dotted) clamped initial-condition units.\", \"page\": 3, \"index\": 1, \"width\": 1114, \"height\": 301}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-27-714865-v1/fig-002.webp\", \"caption\": \"FIG. 3. Targeted dendritic inhibition switches which memory set is available for recall. A, Schematic of the simulated network with a second dendrite (extension of Fig. 2C). B, Memory storage and inhibitory gating. Bi, Schematic of a neuron with two distinct connectivity matrices, one per dendrite, ws1 i j and ws2 i j , storing two sets of memory patterns, s1 and s2. Bii, Schematic of inhibitory gating. External inhibitory connections target opposite dendrites, so that recalling memories stored in one dendrite requires shunting the other dendrite across the network. C, Temporal evolution of the input (top), dendritic membrane potential (middle), and network overlap with the stored memories (bottom) without inhibitory gating. Shaded areas indicate periods of external stimulation (cf. Fig. 2D). D, Gating through GABAA-α5 synapses. Di, Same as Fig. 1Aii, but with an added GABAA-α5 peak current. Dii, Same as Fig. 1D, but with constant GABAA-α5 input. E, Same as panel C, but with active inhibitory gating. Narrow shaded bars indicate periods of external stimulation (as in panel C), and broad coloured backgrounds indicate which memory set is accessible for recall: pink when s1 is accessible (dendrite 2 shunted) and purple when s2 is accessible (dendrite 1 shunted). F, Schematic showing that inhibitory gating switches which attractor landscape is accessible. x1 and x2 denote hypothetical reduced neuronal dimensions, and the vertical axis denotes the pseudo-energy of the system.\", \"page\": 4, \"index\": 2, \"width\": 531, \"height\": 554}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-27-714865-v1/fig-003.webp\", \"caption\": \"FIG. 4. Complex dendritic trees predict branch-specific signatures of inhibitory gating. A, Complex dendritic tree in which each branch bifurcates into two branches. Each leaf dendrite receives a distinct weight matrix, for example ws8 i j . B, Neuron with one recall leaf dendrite driving somatic output, one gated leaf, and isolated leaves that may be either depolarised or hyperpolarised. C, Three inhibitory gating strategies that select a single recall leaf dendrite (to ensure somatic access): gating all dendrites (All), only leaf dendrites (Memory-set-specific), or only branches sharing a branching point with the active path (Optimal). D, Number of hyperpolarised dendrites as a function of the number of memory sets for the strategies in C. E, Activity comparison for independent memories across three leaf dendrites: recall, gated, and isolated. Ei, Temporal evolution of membrane potential (top) and the corresponding fluorescence signal (bottom). Eii, Distributions of membrane potential (top) and fluorescence signal (bottom). Eiii, Pearson correlation distributions for membrane potential (left) and fluorescence (right) between the recall dendrite and gated or isolated dendrites. F, Activity comparison for overlapping memory sets. Fi, Distributions of membrane potential for memory-set overlap o = 0.5 (top) and o = 0.98 (bottom). Fii, Pearson correlation distributions for membrane potential (left) and fluorescence (right) for o = 0.5 (top) and o = 0.98 (bottom). G, Mean Pearson correlation between the recall dendrite and gated or isolated dendrites as a function of overlap (top), and the difference between recall-gated and recall-isolated pairs as a function of overlap (bottom).\", \"page\": 5, \"index\": 3, \"width\": 971, \"height\": 338}]"
motivation: 旨在解决经典联想记忆理论与具有复杂树突结构的生物物理神经回路之间缺乏统一理论框架的问题。
method: 通过构建包含分级树突、局部兴奋-抑制平衡及结构化递归连接的生物物理脉冲神经网络模型进行模拟分析。
result: 发现树突分支特异性的抑制门控能有效减少记忆干扰，且持续的树突动力学通过时间整合扩大了记忆提取的吸引子盆地。
conclusion: 树突电路机制通过局部平衡和分支门控实现了高效且选择性的联想记忆提取，为理解大脑皮层中的记忆存储与检索提供了新视角。
---

## 摘要
从碎片化线索中重建完整记忆的能力是关联记忆的一个核心特征，这要求神经环路在存储许多重叠且冲突的记忆表征的同时，能够选择性地控制记忆的可访问性。吸引子动力学为关联记忆提供了主流的建模框架，并已被用于解释连接性与行为。尽管具有这种影响力，但在具有分室树突和结构化循环相互作用的生物物理脉冲神经网络中，基于吸引子的记忆是如何实现的仍未得到解决，且缺乏统一的理论框架来解释新兴的树突成像和连接组学数据。在这里，我们展示了局部树突的兴奋-抑制平衡创造了类二进制的膜电位状态，从而实现了关联提取；并且分支特异性抑制门控了对存储在树突树各处的记忆集的访问，限制了不同集合之间的干扰。我们进一步表明，连续的树突动力学通过随时间整合部分线索来扩大吸引盆，并且一个“赢者通吃”的读取电路能够自主实现记忆集选择，产生编码集合身份的中间神经元活动。我们的框架预测了分支特异性的电压和钙信号特征，为从印迹组织的角度解释树突测量结果提供了基础，将经典的关联记忆理论与树突环路机制联系起来。

## Abstract
The ability to reconstruct complete memories from fragmented cues is a defining feature of associative memory, which requires neural circuits to store many overlapping and conflicting memory representations while selectively controlling memory accessibility. Attractor dynamics provide the dominant modelling framework for associative memory and have been used to interpret connectivity and behaviour. Yet despite this influence, how attractor-based memory is implemented in biophysical spiking circuits with compartmental dendrites and structured recurrent interactions has remained unresolved, with no unifying theoretical framework for interpreting emerging dendritic imaging and connectomic data. Here we show that local dendritic excitatory-inhibitory balance creates binary-like membrane-potential states that enable associative recall, and that branch-selective inhibition gates access to memory sets stored across dendritic trees, limiting interference between distinct sets. We further show that continuous dendritic dynamics enlarge basins of attraction by integrating partial cues over time, and that a winner-take-all readout circuit implements memory-set selection autonomously, generating interneuron activity that encodes set identity. Our framework predicts branch-specific voltage and calcium signatures that provide a basis for interpreting dendritic measurements in terms of engram organisation, bridging classical associative memory theory with dendritic circuit mechanisms.

---

## 论文详细总结（自动生成）

这是一份关于论文《Dendritic excitatory-inhibitory balance and branch-specific gating enable selective recall of associative memories》的深度结构化总结：

### 1. 核心问题与研究动机
*   **核心问题**：经典的关联记忆理论（如 Hopfield 网络）通常依赖于抽象的二进制神经元，而生物大脑中的神经元具有复杂的**分室树突（Compartmental Dendrites）**和非线性动力学。如何在具有生物物理真实性的脉冲神经网络（SNN）中实现高容量、抗干扰且能选择性提取的关联记忆，一直缺乏统一的理论框架。
*   **研究动机**：现有的生物物理模型往往存储容量极低，且难以处理记忆间的重叠与冲突。作者旨在弥合抽象吸引子模型与真实树突电路之间的鸿沟，解释树突如何通过局部计算参与记忆的存储与检索。

### 2. 方法论：核心思想与技术细节
*   **树突固定点理论**：利用 NMDA（兴奋性）和 $GABA_B/Kir$（抑制性）电流的非线性电压依赖性，在树突分室中创造出稳定的“高电位”和“低电位”固定点。这种局部**兴奋-抑制（EI）平衡**使树突能模拟二进制开关状态。
*   **二进制到生物物理的映射**：开发了一种数学映射方法，将经过优化（使用修改后的感知机学习规则 modPLR）的二进制权重矩阵转化为脉冲神经元的突触电导。
*   **分支特异性门控**：在复杂的树突树中，利用分流抑制（Shunting Inhibition，如 $GABA_A-\alpha5$ 受体）来关闭特定的树突分支。这允许神经元在不同的树突分支上存储不同的“记忆集”，并通过抑制信号选择性地激活其中一个集合。
*   **自主读取电路**：设计了一个闭环系统，包含记忆网络、读取网络（Winner-Take-All 竞争机制）和门控神经元。读取网络识别当前提取的记忆，并反馈信号给门控神经元，从而自主稳定当前的记忆提取状态。

### 3. 实验设计与基准对比
*   **场景设计**：
    *   **单神经元模拟**：验证不同抑制模式（毯式抑制 vs. 匹配抑制）对树突 EI 平衡的影响。
    *   **递归网络提取**：测试从受损线索（部分激活）中恢复完整记忆模式的能力。
    *   **多记忆集选择**：模拟具有 2 个或更多树突分支的神经元，测试在存在干扰项时选择性提取目标记忆的能力。
*   **基准（Benchmark）**：对比了经典的**二进制 Hopfield 网络**。
*   **对比方法**：
    *   对比了有无树突分室的模型（证明单分室模型无法访问高电位固定点）。
    *   对比了不同的抑制门控策略（全部抑制、特定记忆集抑制、最优路径抑制）。
    *   对比了不同呈现时间（Presentation Time）对吸引子盆地（Basin of Attraction）大小的影响。

### 4. 资源与算力
*   **算力说明**：论文中**未明确说明**具体的硬件配置（如 GPU/CPU 型号、数量）或具体的训练时长。
*   **实现方式**：模型基于生物物理神经元方程（基于电导的 Leaky Integrate-and-Fire 模型扩展）进行数值模拟，通常这类模拟在标准科学计算工作站上即可完成。

### 5. 实验数量与充分性
*   **实验规模**：
    *   进行了大量的参数扫描（Parameter Sweeps），涵盖了神经元数量（N=100 到 1000）、记忆负载（$\alpha$）、活动稀疏度（$a_E, a_I$）以及正则化强度（$\rho$）。
    *   包含了针对独立记忆和高度重叠记忆（重叠度达 0.98）的鲁棒性测试。
    *   提供了针对树突电压和钙信号（$\Delta F/F$）的预测性模拟。
*   **充分性评价**：实验设计非常系统且充分。作者不仅证明了模型的有效性，还通过消融实验展示了 NMDA 和 $GABA_B$ 电流的必要性，并探讨了结构连接组学（如每对神经元的突触数量）的预测，具有很高的客观性和理论深度。

### 6. 主要结论与发现
*   **局部平衡是关键**：树突内的局部 EI 平衡是实现类二进制吸引子动力学的生物物理基础。
*   **时间整合优势**：相比于瞬时更新的二进制网络，生物物理树突通过连续的时间整合，能够利用更小的初始线索触发完整的记忆提取（扩大了吸引子盆地）。
*   **门控解决冲突**：分支特异性抑制能有效解决重叠记忆间的干扰，使神经元能像“多路复用器”一样工作。
*   **实验可观测性**：模型预测了在记忆提取过程中，被门控的分支、被隔离的分支和活动的提取分支之间存在显著的电压和钙信号差异，这为未来的实验验证提供了指南。

### 7. 优点与亮点
*   **理论桥梁**：成功将抽象的计算神经科学理论（吸引子）与微观的生物物理机制（树突非线性、特定中间神经元类型）联系起来。
*   **生物真实性**：考虑了多种离子通道动力学、受体类型（AMPA, NMDA, $GABA_A, GABA_B$）以及复杂的树突形态。
*   **功能自主性**：通过引入读取电路，实现了无需外部干预的记忆集切换和冲突消解。

### 8. 不足与局限
*   **学习机制缺失**：论文假设连接权重已经通过 modPLR 优化好，并未展示这些复杂的权重如何通过生物可信的局部塑性规则（如 STDP）自发学习而成。
*   **形态简化**：虽然讨论了复杂树突树，但模拟中仍采用简化的分室模型，未完全考虑极度复杂的神经元形态对信号衰减的全部影响。
*   **参数敏感性**：尽管做了鲁棒性分析，但实现精确的树突固定点可能需要对多种电导比例进行精细调控，这在生物发育过程中可能面临挑战。

（完）
