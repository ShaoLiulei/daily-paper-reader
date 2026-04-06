---
title: Structured stabilization in recurrent neural circuits through inhibitory synaptic plasticity
title_zh: 通过抑制性突触可塑性在循环神经环路中实现结构化稳定
authors: "Festa, D., Cusseddu, C., Gjorgjieva, J."
date: 2026-04-05
pdf: "https://www.biorxiv.org/content/10.1101/2024.10.12.618014v4.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 大型脉冲循环电路中的抑制性脉冲时间依赖可塑性
tldr: 本研究探讨了抑制性神经元如何通过突触可塑性同时实现网络稳定与功能计算。作者提出了一类抑制性脉冲定时依赖可塑性（iSTDP）规则，实现了“结构化稳定”：抑制性连接能自组织形成互惠连接或侧向抑制等特定基元。在大型脉冲神经网络中，这些规则诱导产生了“墨西哥帽”式连接，支持了视觉背景调制和空间模块化活动等复杂功能，揭示了iSTDP在构建功能性皮层回路中的关键作用。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-001.webp\", \"caption\": \"Figure 2: Parametric study of different shapes of iSTDP kernel in the reduced 2D model. A. Representation of four possible shapes of iSTDP kernel, labeled by their effects in the covariance-dominated regime (i.e. with near-zero rate-dependent terms). B. Parametric study based on the analytic solution for each of the four iSTDP kernels, varying 𝛼post and the net area under the iSTDP kernel, 𝐵 (see Eq. 1). The color map represents the level of inhibition, where 1 indicates that the excitatory neuron is completely silenced, and 0 indicates no inhibition, so that the excitatory firing rate matches the input current C,D,E. Final inhibitoryweight as a function of the incoming excitatory weight for three different iSTDP rules. Dots are numerical simulations, gray lines are analytic results (Methods, Eq. 11), color shades indicate different input levels. C. Results for the symmetric, self-stabilizing rule. The green dots represent the same conditions shown in Fig. 1F. D. Results for the antisymmetric, self-stabilizing rule. The green dots represent the same conditions shown in Fig. 1G. E. Results for the symmetric rule in a rate-dominated regime. F,G,H. Corresponding plots showing the rate of the excitatory neuron after convergence.\", \"page\": 6, \"index\": 1, \"width\": 969, \"height\": 799}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-002.webp\", \"caption\": \"Table 1: Numerical parameters used for Fig. 1. The parameters in Fig. 2 match those of Fig. 1 unless otherwise indicated in the figure caption.\", \"page\": 15, \"index\": 2, \"width\": 608, \"height\": 775}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-003.webp\", \"caption\": \"Figure 5: Response properties of the one-dimensional ring network. A. Representation of the stimuli (black) and of the network’s response (green), as a function of the neuron’s location relative to the stimulus center, averaged over 100 trials. B. Response to the center neuron only as a function of stimulus size. C. Schematics of the iso-contra stimulation protocol. The iso direction corresponds to excitatory inputs to excitatory neurons with matching receptive field. The contra direction generates instead an inhibitory input on the SST population. D. Profiles of the center, full iso and contra stimuli to the network. E. Mean response of the center neuron, averaged over 100 trials, for the three stimuli.\", \"page\": 10, \"index\": 3, \"width\": 990, \"height\": 340}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-004.webp\", \"caption\": \"Figure 1: Effects of plasticity on E/I connectivity motifs in a two-neuron circuit. A. Schematics of the two-neuron circuit model. Two time-varying coupled Poisson units, one excitatory and one inhibitory, are connected by a fixed excitatory weight 𝑤exc and a plastic inhibitory weight 𝑤inh. The instantaneous rates are computed as the convolution between each incoming spike and an exponential synaptic kernel that either increases (exc) or decreases (inh) the instantaneous firing probability. The input to the excitatory neuron ℎexc is fixed, whereas the inhibitory input changes dynamically, keeping the inhibitory neuron at a fixed rate 𝑟inh. Only the inhibitory synapse (dashed line) is plastic. The circuit is simulated in two configurations: unidirectional (U), with 𝑤exc = 0 and mutual (M), with 𝑤exc = 0.5. B,C,D. Pairwise interaction kernels of the three iSTDP rules tested (Eq. 1). We used the following numerical parameters. B. 𝐵 = 1, 𝛼pre = −25, 𝛼post = 0, 𝜏+ = 50 ms. C. 𝐵 = 0, 𝛼pre = −0.12, 𝛼post = 1.45, 𝜏+ = 50 ms, 𝜏− = 500 ms. D. 𝐵 = 0, 𝛼pre = −0.14, 𝛼post = 7.95, 𝜏+ = 30 ms, 𝜏− = 30 ms. E,F,G. Change in inhibitory synaptic weight over time for the M (brown) and U (light orange) circuit configurations, under the rules above each column. Dashed lines are analytic predictions for the fixed point (Methods, Eq. 11). H,I,J. Change in excitatory firing rate over time for the M (dark blue) and U (dark green) configurations, under the rules above. Dashed horizontal lines are the analytic predictions for the fixed-point (Methods, Eq. 11).\", \"page\": 3, \"index\": 4, \"width\": 984, \"height\": 546}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-005.webp\", \"caption\": \"Table 3: Numerical parameters for the one-dimensional ring model. The parameters that regulate neural dynamics are the same as in Table 2.\", \"page\": 18, \"index\": 5, \"width\": 762, \"height\": 924}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-006.webp\", \"caption\": \"Figure 3: RNNs of conductance-based LIF neurons self-organize into specific E/I motifs under different iSTDP rules. A left. Representation of the random network with (𝑁exc = 900, 𝑁inh = 100) spiking neurons. The inh-toexc weights form all-to-all connections and are plastic, all other weights are fixed. Exc-to-exc and exc-to-inh connections are sparse. A middle. Kernel of the symmetric, covariance-dominated iSTDP rule used in network 1 (panels B-F). A right. Kernel of the asymmetric, covariance-dominated iSTDP rule used in network 2 (panels G-K). Parameters in Table 2. B. Evolution of population mean firing rates over time, with final distribution of rates over the full populations. C. Evolution of inh-to-exc synaptic weights over time and final distribution. The weights are split into a “mutual” (brown) and a “unidirectional” (light orange) group. Only few weights reach the saturating value, set to 80. D. Example of incoming (blue) and outgoing (red) weights from a single inhibitory neuron, with correlation between them, and distribution of correlations for the full inhibitory populations across 10 random network realizations. E. Random portion of the fixed and sparse exc-to-inh weights (the full matrix, of size 900×100 is shown in SI, Fig. S4). F. Portion of the all-to-all and plastic inh-to-exc connections after learning, with indices matching panel E. For clarity the matrix has been binarized, with threshold-value 𝑤small defined as 0.1 times the 0.9-quantile of the full weight distribution. See SI, Fig. S4, for a continuous representation of synaptic weights. G-K. Equivalent plots in a second network with identical network dynamics and initial conditions, but using the asymmetric iSTDP (see also SI, Fig. S6)\", \"page\": 8, \"index\": 6, \"width\": 998, \"height\": 985}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-007.webp\", \"caption\": \"Table 2: Numerical parameters for the random RNN in Fig. 3.\", \"page\": 17, \"index\": 7, \"width\": 667, \"height\": 1100}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-008.webp\", \"caption\": \"Figure 4: Inhibitory self-organization in a spiking RNN topologically organized as a one-dimensional ring. A. Representation of the model. 800 excitatory neurons are arranged in a one-dimensional ring topology, connected to each other and to their inhibitory counterparts with weights that depend on their distance in tuning space (Methods, Eq. 15). 100 “PV” inhibitory neurons connect all-to-all to the excitatory neurons with plasticity following a symmetric iSTDP rule, 100 “SST” neurons connect all-to-all to excitatory neurons with plasticity following an antisymmetric iSTDP. For both rules 𝐵 = 0, 𝛼pre = −0.1, 𝛼post = 0. B. Full weight matrix after weight convergence. The excitatory weights (blue) are fixed, the inh-to-exc weights (red, lower right) are determined by plasticity. See SI, Fig. S4 for full weight matrix. C. Profile of the average outgoing weights as a function of tuning distance. For convenience, the profiles are normalized so that the maximum is either 1 or −1. D. Average effective interaction profile between the excitatory neurons, as a function of tuning (see Methods). E. Evolution of mean firing rate over time. F. Pearson correlation during spontaneous activity between an excitatory neuron and its neighbors, ordered by tuning distance and averaged over the entire population.\", \"page\": 9, \"index\": 8, \"width\": 987, \"height\": 351}]"
motivation: 探究抑制性突触可塑性如何从简单的稳态调节演变为支持复杂计算的结构化连接。
method: 在小型电路和大型脉冲神经网络中，分析并模拟了多种iSTDP规则对E/I连接基元及网络拓扑的影响。
result: 证明了不同iSTDP规则可诱导互惠或侧向抑制基元，并在环形网络中自组织形成“墨西哥帽”式连接及背景调制效应。
conclusion: 提出了一系列能同时稳定网络活动并促进功能性连接基元生成的iSTDP规则，为理解皮层自组织提供了理论基础。
---

## 摘要
在皮层环路中，抑制性中间神经元发挥着双重作用：调节整体活动水平以防止兴奋失控，并参与多种计算。虽然非结构化的抑制性突触连接通过稳态调节放电率来实现前者，但计算任务通常需要结构化的兴奋-抑制（E/I）连接。在此，我们考虑了一类广泛的成对抑制性脉冲时间依赖可塑性（iSTDP）规则，展示了抑制性连接如何通过自组织同时稳定兴奋并产生功能相关的连接基序——我们将这一过程称为“结构化稳定”。我们表明，在小型 E/I 环路和大型脉冲循环神经网络中，iSTDP 规则的选择可以导致相互连接的 E/I 对，或者导致侧向抑制（即抑制性神经元连接到并不直接反向连接它的兴奋性神经元）。在一个包含两个遵循不同 iSTDP 规则的抑制性亚群的一维环形网络中，兴奋性单元之间的有效连接自组织成类似墨西哥帽的轮廓，即中心为兴奋性影响，远离中心处为抑制性影响。这产生了涌现的网络响应，例如视觉皮层中的上下文调制效应，以及发育期自发活动所特有的空间模块化活动。我们的理论工作引入了一系列规则，在保留基于脉冲时间的可塑性的广泛适用性和简单性的同时，稳定了活动并促进了支持涌现网络计算的特定连接基序。

## Abstract
In cortical circuits, inhibitory interneurons play a dual role: they regulate overall activity levels to prevent runaway excitation, and contribute to diverse computations. While unstructured inhibitory synaptic connections achieve the first role by homeostatically regulating firing rates, computational tasks often require structured excitatory-inhibitory (E/I) connectivity. Here, we consider a broad class of pairwise inhibitory spike-timing dependent plasticity (iSTDP) rules, demonstrating how inhibitory connections can self-organize to both stabilize excitation and generate functionally relevant connectivity motifs--a process we call "structured stabilization". We show that in both small E/I circuits and large spiking recurrent neural networks the choice of iSTDP rule can lead to either mutually connected E/I pairs, or to lateral inhibition, where an inhibitory neuron connects to an excitatory neuron that does not directly connect back to it. In a one-dimensional ring network with two inhibitory subpopulations following these distinct iSTDP rules, the effective connectivity within the excitatory units self-organizes into a Mexican-hat-like profile, with excitatory influence in the center and inhibitory influence away from the center. This leads to emergent network responses such as contextual modulation effects as in the visual cortex and spatially modular activity characteristic of developmental spontaneous activity. Our theoretical work introduces a family of rules that retains the broad applicability and simplicity of spike-timing-based plasticity, while stabilizing activity and promoting specific connectivity motifs which support emergent network computations.

---

## 论文详细总结（自动生成）

以下是对论文《Structured stabilization in recurrent neural circuits through inhibitory synaptic plasticity》（通过抑制性突触可塑性在循环神经环路中实现结构化稳定）的深度总结：

### 1. 论文的核心问题与整体含义（研究动机和背景）
*   **核心问题**：大脑皮层中的抑制性神经元不仅负责维持网络活动的稳态（防止兴奋失控），还参与复杂的计算。然而，传统的抑制性突触可塑性（iSTDP）研究多侧重于非结构化的放电率调节。本研究探讨了**iSTDP规则如何通过自组织产生特定的连接基元（Motifs）**，从而在稳定网络的同时实现功能性的“结构化稳定”。
*   **整体含义**：论文提出，抑制性连接的结构化（如互惠连接或侧向抑制）是实现复杂皮层功能（如视觉背景调制、空间模块化活动）的关键，而这些结构可以通过特定的脉冲时间依赖规则自发形成。

### 2. 论文提出的方法论
*   **核心思想**：定义了一类广义的iSTDP规则，通过调整可塑性窗口（Kernel）的形状和参数，使抑制性突触能够根据神经元间的相关性（协方差）或放电率进行演化。
*   **关键技术细节**：
    *   **iSTDP 规则模型**：突触权重 $w$ 的变化取决于突触前（抑制性）和突触后（兴奋性）脉冲的时间差 $\Delta t$。规则包含：
        1.  **放电率相关项**（$\alpha_{pre}, \alpha_{post}$）：调节基础放电率。
        2.  **协方差相关项**（核函数 $K(\Delta t)$）：捕捉脉冲间的精确时间相关性。
    *   **规则分类**：
        *   **对称规则**：对 $\Delta t$ 的正负响应一致，倾向于加强具有强相关性的 E-I 对（形成互惠连接）。
        *   **反对称规则**：对正负 $\Delta t$ 响应相反，倾向于抑制不直接连接回它的兴奋性神经元（形成侧向抑制）。
    *   **分析框架**：首先在简化的二维（一电一抑）模型中进行解析推导，随后在大型脉冲神经网络（SNN）中验证。

### 3. 实验设计
*   **实验场景**：
    1.  **双神经元电路**：测试不同 iSTDP 规则在单向（U）和互惠（M）配置下的收敛情况。
    2.  **随机循环神经网络（RNN）**：包含 900 个兴奋性神经元和 100 个抑制性神经元，验证在大规模随机连接中是否能自发涌现出特定的连接基元。
    3.  **一维环形网络（Ring Network）**：模拟具有拓扑结构的皮层，包含 PV 类（遵循对称规则）和 SST 类（遵循反对称规则）抑制性神经元。
*   **对比方法**：对比了对称与反对称、协方差主导与放电率主导等多种 iSTDP 变体规则。
*   **Benchmark**：以经典的稳态 iSTDP（如 Vogels et al., 2011）为基准，观察其在结构化连接形成方面的差异。

### 4. 资源与算力
*   **算力说明**：论文中**未明确说明**具体的 GPU 型号或训练时长。
*   **实现细节**：根据文中描述，模拟使用了基于电导的 Leaky Integrate-and-Fire (LIF) 神经元模型，通常这类模拟在标准工作站或高性能计算集群（HPC）上使用 Python（如 Brian2 或 NEST 仿真器）完成。

### 5. 实验数量与充分性
*   **实验规模**：
    *   进行了参数空间扫描（如 Fig. 2 中的 $\alpha_{post}$ 与 $B$ 的关系）。
    *   在随机网络中进行了 10 次随机实现的重复实验以验证统计显著性。
    *   在环形网络中测试了多种刺激协议（中心刺激、全域刺激、对比刺激）。
*   **充分性评价**：实验设计较为充分，从简单的解析模型过渡到复杂的拓扑网络，逻辑链条完整。通过消融实验展示了不同规则对网络功能（如墨西哥帽连接形成）的必要性。

### 6. 论文的主要结论与发现
*   **结构化稳定**：iSTDP 不仅能稳定放电率，还能根据规则形状诱导产生互惠连接（Reciprocal）或侧向抑制（Lateral inhibition）基元。
*   **墨西哥帽结构的自组织**：在环形网络中，结合对称和反对称规则，网络能自发形成“中心兴奋、外围抑制”的有效连接轮廓。
*   **功能涌现**：这种自组织的结构支持了视觉皮层中常见的**外周抑制（Surround Suppression）**效应，并能产生类似于发育早期观察到的模块化自发活动。

### 7. 优点
*   **理论与仿真结合**：通过数学解析预测了突触权重的固定点，并在复杂的脉冲网络中得到了验证。
*   **功能导向**：不仅关注连接的形成，还成功解释了生物学上的视觉调制现象，增强了模型的说服力。
*   **规则的普适性**：提出的框架涵盖了多种已知的 iSTDP 规则，具有很强的通用性。

### 8. 不足与局限
*   **神经元模型简化**：主要使用 LIF 神经元，未深入探讨树突计算或更复杂的生物物理特性对可塑性的影响。
*   **拓扑结构限制**：环形网络虽然经典，但仍是高度简化的皮层抽象，在更复杂的 2D 或 3D 真实脑区拓扑下的表现尚待验证。
*   **多重可塑性交互**：现实中兴奋性突触（eSTDP）和抑制性突触可塑性是同时发生的，本文主要固定了兴奋性连接，简化了两者间的动态交互。

（完）
