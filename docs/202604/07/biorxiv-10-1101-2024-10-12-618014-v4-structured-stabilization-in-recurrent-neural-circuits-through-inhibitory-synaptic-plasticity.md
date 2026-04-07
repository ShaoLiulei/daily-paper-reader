---
title: Structured stabilization in recurrent neural circuits through inhibitory synaptic plasticity
title_zh: 通过抑制性突触可塑性在循环神经环路中实现结构化稳定化
authors: "Festa, D., Cusseddu, C., Gjorgjieva, J."
date: 2026-04-05
pdf: "https://www.biorxiv.org/content/10.1101/2024.10.12.618014v4.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 脉冲递归电路中的抑制性脉冲时间依赖可塑性 (iSTDP)
tldr: 本研究探讨了皮层回路中抑制性突触的可塑性如何兼顾活动稳定与功能计算。通过引入一类成对抑制性脉冲时间依赖可塑性（iSTDP）规则，研究者展示了“结构化稳定”过程：抑制性连接能自组织形成互惠连接或侧向抑制等特定基元。在大型脉冲神经网络中，这些规则使系统自发产生墨西哥帽状连接，进而实现视觉皮层中的背景调制和空间模块化活动。该工作为理解抑制性可塑性如何驱动复杂网络计算提供了重要理论基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-001.webp\", \"caption\": \"Figure 2: Parametric study of different shapes of iSTDP kernel in the reduced 2D model. A. Representation of four possible shapes of iSTDP kernel, labeled by their effects in the covariance-dominated regime (i.e. with near-zero rate-dependent terms). B. Parametric study based on the analytic solution for each of the four iSTDP kernels, varying 𝛼post and the net area under the iSTDP kernel, 𝐵 (see Eq. 1). The color map represents the level of inhibition, where 1 indicates that the excitatory neuron is completely silenced, and 0 indicates no inhibition, so that the excitatory firing rate matches the input current C,D,E. Final inhibitoryweight as a function of the incoming excitatory weight for three different iSTDP rules. Dots are numerical simulations, gray lines are analytic results (Methods, Eq. 11), color shades indicate different input levels. C. Results for the symmetric, self-stabilizing rule. The green dots represent the same conditions shown in Fig. 1F. D. Results for the antisymmetric, self-stabilizing rule. The green dots represent the same conditions shown in Fig. 1G. E. Results for the symmetric rule in a rate-dominated regime. F,G,H. Corresponding plots showing the rate of the excitatory neuron after convergence.\", \"page\": 6, \"index\": 1, \"width\": 969, \"height\": 799}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-002.webp\", \"caption\": \"Table 1: Numerical parameters used for Fig. 1. The parameters in Fig. 2 match those of Fig. 1 unless otherwise indicated in the figure caption.\", \"page\": 15, \"index\": 2, \"width\": 608, \"height\": 775}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-003.webp\", \"caption\": \"Figure 5: Response properties of the one-dimensional ring network. A. Representation of the stimuli (black) and of the network’s response (green), as a function of the neuron’s location relative to the stimulus center, averaged over 100 trials. B. Response to the center neuron only as a function of stimulus size. C. Schematics of the iso-contra stimulation protocol. The iso direction corresponds to excitatory inputs to excitatory neurons with matching receptive field. The contra direction generates instead an inhibitory input on the SST population. D. Profiles of the center, full iso and contra stimuli to the network. E. Mean response of the center neuron, averaged over 100 trials, for the three stimuli.\", \"page\": 10, \"index\": 3, \"width\": 990, \"height\": 340}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-004.webp\", \"caption\": \"Figure 1: Effects of plasticity on E/I connectivity motifs in a two-neuron circuit. A. Schematics of the two-neuron circuit model. Two time-varying coupled Poisson units, one excitatory and one inhibitory, are connected by a fixed excitatory weight 𝑤exc and a plastic inhibitory weight 𝑤inh. The instantaneous rates are computed as the convolution between each incoming spike and an exponential synaptic kernel that either increases (exc) or decreases (inh) the instantaneous firing probability. The input to the excitatory neuron ℎexc is fixed, whereas the inhibitory input changes dynamically, keeping the inhibitory neuron at a fixed rate 𝑟inh. Only the inhibitory synapse (dashed line) is plastic. The circuit is simulated in two configurations: unidirectional (U), with 𝑤exc = 0 and mutual (M), with 𝑤exc = 0.5. B,C,D. Pairwise interaction kernels of the three iSTDP rules tested (Eq. 1). We used the following numerical parameters. B. 𝐵 = 1, 𝛼pre = −25, 𝛼post = 0, 𝜏+ = 50 ms. C. 𝐵 = 0, 𝛼pre = −0.12, 𝛼post = 1.45, 𝜏+ = 50 ms, 𝜏− = 500 ms. D. 𝐵 = 0, 𝛼pre = −0.14, 𝛼post = 7.95, 𝜏+ = 30 ms, 𝜏− = 30 ms. E,F,G. Change in inhibitory synaptic weight over time for the M (brown) and U (light orange) circuit configurations, under the rules above each column. Dashed lines are analytic predictions for the fixed point (Methods, Eq. 11). H,I,J. Change in excitatory firing rate over time for the M (dark blue) and U (dark green) configurations, under the rules above. Dashed horizontal lines are the analytic predictions for the fixed-point (Methods, Eq. 11).\", \"page\": 3, \"index\": 4, \"width\": 984, \"height\": 546}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-005.webp\", \"caption\": \"Table 3: Numerical parameters for the one-dimensional ring model. The parameters that regulate neural dynamics are the same as in Table 2.\", \"page\": 18, \"index\": 5, \"width\": 762, \"height\": 924}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-006.webp\", \"caption\": \"Figure 3: RNNs of conductance-based LIF neurons self-organize into specific E/I motifs under different iSTDP rules. A left. Representation of the random network with (𝑁exc = 900, 𝑁inh = 100) spiking neurons. The inh-toexc weights form all-to-all connections and are plastic, all other weights are fixed. Exc-to-exc and exc-to-inh connections are sparse. A middle. Kernel of the symmetric, covariance-dominated iSTDP rule used in network 1 (panels B-F). A right. Kernel of the asymmetric, covariance-dominated iSTDP rule used in network 2 (panels G-K). Parameters in Table 2. B. Evolution of population mean firing rates over time, with final distribution of rates over the full populations. C. Evolution of inh-to-exc synaptic weights over time and final distribution. The weights are split into a “mutual” (brown) and a “unidirectional” (light orange) group. Only few weights reach the saturating value, set to 80. D. Example of incoming (blue) and outgoing (red) weights from a single inhibitory neuron, with correlation between them, and distribution of correlations for the full inhibitory populations across 10 random network realizations. E. Random portion of the fixed and sparse exc-to-inh weights (the full matrix, of size 900×100 is shown in SI, Fig. S4). F. Portion of the all-to-all and plastic inh-to-exc connections after learning, with indices matching panel E. For clarity the matrix has been binarized, with threshold-value 𝑤small defined as 0.1 times the 0.9-quantile of the full weight distribution. See SI, Fig. S4, for a continuous representation of synaptic weights. G-K. Equivalent plots in a second network with identical network dynamics and initial conditions, but using the asymmetric iSTDP (see also SI, Fig. S6)\", \"page\": 8, \"index\": 6, \"width\": 998, \"height\": 985}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-007.webp\", \"caption\": \"Table 2: Numerical parameters for the random RNN in Fig. 3.\", \"page\": 17, \"index\": 7, \"width\": 667, \"height\": 1100}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2024-10-12-618014-v4/fig-008.webp\", \"caption\": \"Figure 4: Inhibitory self-organization in a spiking RNN topologically organized as a one-dimensional ring. A. Representation of the model. 800 excitatory neurons are arranged in a one-dimensional ring topology, connected to each other and to their inhibitory counterparts with weights that depend on their distance in tuning space (Methods, Eq. 15). 100 “PV” inhibitory neurons connect all-to-all to the excitatory neurons with plasticity following a symmetric iSTDP rule, 100 “SST” neurons connect all-to-all to excitatory neurons with plasticity following an antisymmetric iSTDP. For both rules 𝐵 = 0, 𝛼pre = −0.1, 𝛼post = 0. B. Full weight matrix after weight convergence. The excitatory weights (blue) are fixed, the inh-to-exc weights (red, lower right) are determined by plasticity. See SI, Fig. S4 for full weight matrix. C. Profile of the average outgoing weights as a function of tuning distance. For convenience, the profiles are normalized so that the maximum is either 1 or −1. D. Average effective interaction profile between the excitatory neurons, as a function of tuning (see Methods). E. Evolution of mean firing rate over time. F. Pearson correlation during spontaneous activity between an excitatory neuron and its neighbors, ordered by tuning distance and averaged over the entire population.\", \"page\": 9, \"index\": 8, \"width\": 987, \"height\": 351}]"
motivation: 旨在解决抑制性神经元如何在维持网络活动稳定的同时，通过自组织形成支持复杂计算的结构化连接基元。
method: 提出并分析了一类成对抑制性脉冲时间依赖可塑性（iSTDP）规则，并在小型电路和大型脉冲循环神经网络中验证其效果。
result: 发现不同的iSTDP规则可诱导产生互惠E/I对或侧向抑制结构，并在环形网络中自发形成墨西哥帽状连接及背景调制等功能性响应。
conclusion: 该研究证明了iSTDP规则在稳定网络活动与促进特定计算基元形成中的双重作用，为理解神经回路的自组织提供了新视角。
---

## 摘要
在皮层环路中，抑制性中间神经元发挥着双重作用：它们调节整体活动水平以防止失控的兴奋，并参与多种计算。虽然非结构化的抑制性突触连接通过稳态调节放电率来实现前者的作用，但计算任务通常需要结构化的兴奋-抑制（E/I）连接。在此，我们考虑了一类广泛的成对抑制性脉冲时间依赖可塑性（iSTDP）规则，展示了抑制性连接如何自组织以同时稳定兴奋并产生功能相关的连接基序——我们将这一过程称为“结构化稳定化”。我们表明，在小型 E/I 环路和大型脉冲循环神经网络中，iSTDP 规则的选择可以导致相互连接的 E/I 对，或者导致侧向抑制（即抑制性神经元连接到并不直接反向连接它的兴奋性神经元）。在一个具有两个遵循这些不同 iSTDP 规则的抑制性亚群的一维环形网络中，兴奋性单元内的有效连接自组织成类似墨西哥帽的轮廓，中心为兴奋性影响，远离中心为抑制性影响。这导致了涌现的网络响应，例如视觉皮层中的上下文调制效应，以及发育期自发活动特征的空间模块化活动。我们的理论工作引入了一系列规则，这些规则保留了基于脉冲时间的可塑性的广泛适用性和简单性，同时稳定了活动并促进了支持涌现网络计算的特定连接基序。

## Abstract
In cortical circuits, inhibitory interneurons play a dual role: they regulate overall activity levels to prevent runaway excitation, and contribute to diverse computations. While unstructured inhibitory synaptic connections achieve the first role by homeostatically regulating firing rates, computational tasks often require structured excitatory-inhibitory (E/I) connectivity. Here, we consider a broad class of pairwise inhibitory spike-timing dependent plasticity (iSTDP) rules, demonstrating how inhibitory connections can self-organize to both stabilize excitation and generate functionally relevant connectivity motifs--a process we call "structured stabilization". We show that in both small E/I circuits and large spiking recurrent neural networks the choice of iSTDP rule can lead to either mutually connected E/I pairs, or to lateral inhibition, where an inhibitory neuron connects to an excitatory neuron that does not directly connect back to it. In a one-dimensional ring network with two inhibitory subpopulations following these distinct iSTDP rules, the effective connectivity within the excitatory units self-organizes into a Mexican-hat-like profile, with excitatory influence in the center and inhibitory influence away from the center. This leads to emergent network responses such as contextual modulation effects as in the visual cortex and spatially modular activity characteristic of developmental spontaneous activity. Our theoretical work introduces a family of rules that retains the broad applicability and simplicity of spike-timing-based plasticity, while stabilizing activity and promoting specific connectivity motifs which support emergent network computations.

---

## 论文详细总结（自动生成）

这是一份关于论文《Structured stabilization in recurrent neural circuits through inhibitory synaptic plasticity》的结构化深入总结：

### 1. 核心问题与整体含义（研究动机和背景）
*   **核心问题**：在皮层神经环路中，抑制性神经元如何同时实现两个看似矛盾的目标：一是作为“刹车”维持全局活动的稳态（防止兴奋失控），二是形成精细的结构化连接（如特定基元）以支持复杂的计算任务。
*   **研究背景**：传统的抑制性可塑性模型（如经典的 Vogels 等人的 iSTDP 规则）通常只关注放电率的稳态调节，导致连接趋向于均匀的“毯状抑制（blanket inhibition）”，忽略了实验中观察到的多样化 E/I 连接基元。

### 2. 方法论：核心思想与关键技术
*   **核心思想**：提出一种通用的成对 iSTDP 框架，通过调整可塑性规则的“形状”（对称性、积分面积等），使网络在自发活动中通过“结构化稳定化（Structured Stabilization）”过程自组织出特定的连接模式。
*   **关键技术细节**：
    *   **通用均值场方程**：将突触权重变化分解为放电率相关项（由参数 $\alpha_{pre}, \alpha_{post}, B$ 控制）和协方差相关项（由内核 $L(\tau)$ 与脉冲协方差 $C(\tau)$ 的积分 $Q$ 控制）。
    *   **规则分类**：
        *   **放电率主导型（Rate-dominated）**：$B$ 值较大，主要调节放电率达到目标值，对连接结构不敏感。
        *   **协方差主导型（Covariance-dominated）**：$B \approx 0$，权重变化主要由神经元间的脉冲时间相关性驱动。
    *   **内核形状设计**：分析了对称内核（促进互惠连接，即相互连接的 E/I 对）和反对称内核（促进侧向抑制，即抑制性神经元连接到不反向连接它的兴奋性神经元）。
    *   **解析推导**：在双神经元（一静一动）的 Hawkes 过程模型下，推导出了抑制性权重的闭式解（Fixed-point solution）。

### 3. 实验设计与对比
*   **实验场景**：
    1.  **双神经元基元模型**：用于解析验证不同 iSTDP 规则对“单向”和“互惠”连接的选择偏好。
    2.  **随机连接的脉冲神经网络（RNN）**：包含 900 个兴奋性和 100 个抑制性 LIF 神经元，验证在大规模网络中规则的稳定性。
    3.  **一维环形拓扑网络（Ring Network）**：模拟具有空间调谐特性的皮层（如视觉皮层 V1），包含 PV（对称规则）和 SST（反对称规则）两类抑制性亚群。
*   **对比基准（Benchmark）**：
    *   对比了经典的放电率稳态 iSTDP 规则。
    *   对比了单一抑制性群体（仅 PV 或仅 SST）与混合群体的表现。
    *   对比了不同输入强度下的鲁棒性。

### 4. 资源与算力
*   **软件实现**：使用了 Julia 语言进行数值模拟和解析计算，使用 Brian2 仿真器进行大规模脉冲神经网络模拟。
*   **算力说明**：论文**未明确说明**具体的 GPU/CPU 型号、数量或总训练时长。考虑到 1000 节点规模的 LIF 网络模拟，通常单台高性能工作站即可在数小时内完成。

### 5. 实验数量与充分性
*   **实验规模**：
    *   进行了参数空间扫描（如改变 $B$ 和 $\alpha$），验证了规则的稳定性边界。
    *   在随机网络中进行了 10 次独立随机实现的重复实验，并给出了统计分布。
    *   针对环形网络，测试了不同刺激尺寸（Surround Suppression）和上下文调制（Iso-contra stimulation）等多种功能性场景。
*   **充分性评价**：实验设计非常充分且具有逻辑链条，从简单的解析模型过渡到复杂的生物物理模型，并最终关联到已知的生理现象（如视觉皮层的侧向抑制和发育期的自发活动相关性），客观性较强。

### 6. 主要结论与发现
*   **结构决定功能**：iSTDP 内核的对称性决定了最终形成的基元：对称内核强化互惠连接，反对称内核强化侧向抑制。
*   **自组织墨西哥帽**：在环形网络中，PV 和 SST 神经元通过不同的可塑性规则，共同使有效连接自组织成“中心兴奋、周围抑制”的墨西哥帽轮廓。
*   **涌现计算特性**：这种自组织的结构自然产生了视觉系统中的“周围抑制（Surround Suppression）”和“上下文易化”效应，并能解释发育早期皮层中观察到的长程空间相关性。

### 7. 优点（亮点）
*   **理论深度**：不仅有数值模拟，还提供了严谨的数学解析框架，建立了 iSTDP 参数与网络拓扑特征之间的直接联系。
*   **生物一致性**：模型成功整合了 PV 和 SST 神经元在可塑性规则上的已知实验差异，并解释了它们在环路功能中的协同作用。
*   **功能导向**：证明了简单的局部学习规则（iSTDP）足以产生复杂的全局计算特性，无需预设复杂的连接模板。

### 8. 不足与局限
*   **参数敏感性**：协方差主导型规则（$B \approx 0$）在大型网络中对参数调节较为敏感，有时需要引入微小的放电率补偿项才能稳定。
*   **突触类型限制**：主要关注抑制性到兴奋性的可塑性，未深入探讨兴奋性可塑性（E-to-E, E-to-I）与抑制性可塑性在长时间尺度上的交互演化。
*   **应用范围**：目前主要在静态或简单的时空输入下测试，对于高度动态、非平稳环境下的学习能力尚待验证。

（完）
