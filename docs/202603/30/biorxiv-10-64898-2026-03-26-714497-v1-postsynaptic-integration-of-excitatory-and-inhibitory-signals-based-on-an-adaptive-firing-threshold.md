---
title: Postsynaptic integration of excitatory and inhibitory signals based on an adaptive firing threshold
title_zh: 基于自适应发放阈值的兴奋性和抑制性信号的突触后整合
authors: "Gambrell, O., Singh, A."
date: 2026-03-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.26.714497v1.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 整合发放模型与脉冲间隔统计
tldr: 本研究探讨了突触后神经元如何整合兴奋性和抑制性信号，重点分析了脉冲间期（ISI）的统计特性。研究首先基于经典整合发放模型推导了兴奋性突触的ISI矩解析解，随后扩展至包含抑制性输入及自适应阈值的复杂模型。研究发现，自适应阈值机制可能导致抑制性输入频率增加反而提升发放频率的现象，并界定了ISI噪声在不同参数下的分布特征，为理解神经信息处理提供了理论基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-26-714497-v1/fig-001.webp\", \"caption\": \"Fig. 1. A schematic of synaptic transmission and a sample trajectory of the membrane potential from the associated synaptic model. A: Synaptic vesicles docked at docking sites at the active zone of the presynaptic axon terminal fuse with the membrane and release their neurotransmitter content into the synaptic cleft. These neurotransmitters then bind to receptors on the postsynaptic neuron, which facilitates the movement of positive ions between the inside and the outside of the postsynaptic neuron, changing its membrane potential. B: A simulated trajectory of the postsynaptic neuron’s membrane potential as modeled in equations (1) and (2). The membrane potential (blue line) depolarizes upon the arrival of presynaptic action potentials (red lines), which arrive via a Poisson process with rate fe. The number of synaptic vesicles (SVs) that fuse upon the arrival of an action potential (AP) follows a Poisson distribution with mean ⟨be⟩. Between presynaptic APs, the membrane potential exponentially decays, with time constant τv , to a resting potential, here 0. Once the membrane potential exceeds a threshold potential vth, the postsynaptic neuron fires an action potential (red circles). The ISI is the time between postsynaptic APs. Parameters: fe = 10 Hz, ⟨be⟩ = 15, τv = 100 ms, vth = 20 mV .\", \"page\": 2, \"index\": 1, \"width\": 1054, \"height\": 379}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-26-714497-v1/fig-002.webp\", \"caption\": \"Fig. 2. Characterizing the statistics of postsynaptic firing times as a function of both presynaptic and postsynaptic parameters. The synaptic model used for these figures is from equations (1) and (2), and the results of this figure are the solutions to equation (14). A: ISI mean (top) and ISI noise (bottom) as a function of the input frequency. Parameter values: vth = 20 mV , ⟨be⟩ = 5, v0 = 0 mV . B: ISI mean (top) and noise (bottom) as a function of the mean QC. Parameter values: fe = 50 Hz, vth = 20 mV , v0 = 0 mV . C: ISI mean (top) and noise (bottom) as a function of the threshold potential. Parameter values: fe = 50 Hz, ⟨be⟩ = 5, v0 = 0 mV .\", \"page\": 3, \"index\": 2, \"width\": 894, \"height\": 468}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-26-714497-v1/fig-003.webp\", \"caption\": \"Fig. 3. Inhibitory presynaptic APs can increase the mean postsynaptic firing frequency when the threshold potential adapts with recent firing history. The simulations in B and C come from the model in equation (15) and the simulations in E and F come from the adaptive threshold model in (16) and (17). In B,C,E, and F, excitatory and inhibitory QC follow gamma distributions with means ⟨be⟩, ⟨bi⟩ and noise CV 2 be , CV 2 bi , respectively. A: Excitatory-Inhibitory (EI) model schematic. The axon terminals of an excitatory and an inhibitory presynaptic neuron both terminate on the dendrites of a postsynaptic neuron. B: The mean postsynaptic firing frequency as a function of excitatory and inhibitory input frequency for the fixed threshold model. C: Noise in ISI for the fixed threshold model. D: Sample membrane potential and threshold potential trajectories for the adaptive threshold model. Presynaptic excitatory and inhibitory APs arrive via Poisson processes with rates fe and fi and either depolarize or polarize the membrane potential (blue line). When the membrane potential is driven below its resting potential by an inhibitory presynaptic AP (purple dotted line), the threshold potential (black line) evolves via equation (16) and (17). This facilitates postsynaptic AP firing (red circle) upon the arrival of excitatory presynaptic APs (red dotted line). E: Mean postsynaptic firing frequency for the adaptive threshold model. The white dashed line is the mean postsynaptic firing frequency at 53 Hz for a varying inhibitory input frequency. The white circle shows that the maximum postsynaptic firing frequency occurs at an inhibitory input frequency of 55 Hz. F: Noise in ISI for the adaptive threshold model. Parameters: vth = 20 mV , ⟨be⟩ = 20 mV , CV 2 be = 0.01, ⟨bi⟩ = 20 mV , CV 2 bi = 0.01, τv = 10 ms, vb = 20 mV , vlow = 10 mV , v1 = −1 mV .\", \"page\": 5, \"index\": 3, \"width\": 1054, \"height\": 608}]"
motivation: 旨在通过数学建模深入理解突触后神经元在随机递质释放影响下的脉冲发放频率调制及其统计规律。
method: 采用首时（First-passage time）分析框架，针对包含兴奋/抑制输入及自适应阈值的整合发放模型推导ISI统计矩的精确解析结果。
result: 发现自适应阈值会导致抑制性输入频率增加反而提升突触后发放频率的异常现象，并明确了ISI噪声的变异系数分布区间。
conclusion: 研究揭示了自适应阈值在神经信号整合中的关键作用，证明了其对神经元发放精确度和频率调控的显著影响。
---

## 摘要
神经元内通信的一个关键组成部分是突触前神经元随机释放递质对突触后发放频率的调节。连续突触后发放之间的时间间隔被称为脉冲间期（ISI），理解其统计特性对于神经信息处理至关重要。我们首先建立了一个兴奋性化学突触模型，其中突触后神经元的发放遵循经典的整合-发放（integrate-and-fire）模型。利用首通时间（first-passage time）框架，我们推导出了 ISI 统计矩的精确解析结果，揭示了驱动突触后动作电位定时精确性的参数范围。随后，我们将该分析扩展到包含连接至同一突触后神经元的兴奋性和抑制性突触前连接。我们同时考虑了固定的突触后发放阈值以及基于突触后膜电位历史进行调整的自适应阈值。我们的分析表明，后者的自适应阈值可能导致增加抑制性输入频率反而增加突触后发放频率的情况。此外，我们根据变异系数（coefficient of variation）小于或大于 1，分别刻画了 ISI 噪声呈亚指数（hypo-exponential）或超指数（hyperexponential）分布的参数范围。

## Abstract
A key component of intraneuronal communication is the modulation of postsynaptic firing frequencies by stochastic transmitter release from presynaptic neurons. The time interval between successive postsynaptic firings is called the inter-spike interval (ISI), and understanding its statistics is integral to neural information processing. We start with a model of an excitatory chemical synapse with postsynaptic neuron firing governed as per a classical integrate-and-fire model. Using a first-passage time framework, we derive exact analytical results for the ISI statistical moments, revealing parameter regimes driving precision in postsynaptic action potential timing. Next, we extended this analysis to include both an excitatory and an inhibitory presynaptic connection onto the same postsynaptic neuron. We consider both a fixed postsynaptic-firing threshold and a threshold that adapts based on the postsynaptic membrane potential history. Our analysis shows that the latter adaptive threshold can result in scenarios where increasing the inhibitory input frequency increases the postsynaptic firing frequency. Moreover, we characterize parameter regimes where ISI noise is hypo-exponential or hyperexponential based on its coefficient of variation being less than or higher than one, respectively.

---

## 论文详细总结（自动生成）

这篇论文题目为《基于自适应发放阈值的兴奋性和抑制性信号的突触后整合》，由特拉华大学和科美纽斯大学的研究人员合作完成。以下是对该论文的结构化总结：

### 1. 核心问题与整体含义（研究动机和背景）
*   **核心问题**：研究突触后神经元如何整合来自突触前的随机兴奋性（E）和抑制性（I）信号，并重点分析**脉冲间隔（ISI）**的统计特性（均值与噪声）。
*   **研究背景**：神经元间的通信依赖于神经递质的随机释放。传统的整合-发放（LIF）模型多采用固定阈值，但生物神经元的离子通道特性决定了其发放阈值是动态变化的。
*   **研究动机**：探索自适应阈值如何影响神经元发放的精确度，以及在抑制性信号存在时，神经元发放频率表现出的非直觉行为。

### 2. 方法论：核心思想与技术细节
*   **核心思想**：利用**首通时间（First-Passage Time, FPT）**框架，将神经元达到发放阈值的过程建模为随机过程越过边界的问题，从而推导出 ISI 统计矩的精确解析表达式。
*   **关键技术细节**：
    *   **突触模型**：兴奋性输入按速率为 $f_e$ 的泊松过程到达，每次引起膜电位 $v(t)$ 增加一个随机量 $b_e$（量子含量，QC）；抑制性输入则引起减少 $b_i$。
    *   **动力学方程**：采用漏电整合-发放模型，膜电位在两次输入间按时间常数 $\tau_v$ 指数衰减至静息电位。
    *   **自适应阈值模型**：阈值 $v_{th}$ 不再固定，而是随膜电位历史演化。当膜电位因抑制信号而超极化时，阈值会降低（模拟“后抑制易化”现象），其演化遵循一个线性分段函数和时间常数 $\tau_{th}$。
    *   **数学推导**：通过后向方程（Backward Equation）推导出关于 ISI 矩的**非齐次线性延迟微分方程（DDE）**，并证明了该方程在特定边界条件下解的存在性与唯一性。

### 3. 实验设计
*   **场景设定**：
    1.  **单兴奋性输入场景**：分析 $f_e$、平均 QC 和固定阈值对 ISI 均值和噪声的影响。
    2.  **兴奋-抑制（EI）网络场景**：对比“固定阈值”与“自适应阈值”两种模式。
*   **Benchmark 与对比**：
    *   以经典的固定阈值 LIF 模型作为基准。
    *   对比不同输入频率（$f_e, f_i$）组合下的突触后发放频率和 ISI 变异系数（$CV^2$）。
*   **评估指标**：ISI 均值、ISI 噪声（$CV^2$）。根据 $CV^2$ 与 1 的关系，将噪声分为亚指数（<1）、指数（=1）和超指数（>1）三类。

### 4. 资源与算力
*   **算力说明**：论文中**未明确说明**具体的硬件配置（如 GPU 型号、数量）或训练时长。
*   **性质分析**：由于该研究侧重于数学解析推导和数值仿真（基于微分方程求解和随机模拟），而非深度学习大模型训练，因此对高性能 GPU 算力的需求较低，通常在标准工作站或个人电脑上即可完成。

### 5. 实验数量与充分性
*   **实验规模**：论文展示了多组参数扫描实验，包括输入频率（0-100Hz）、平均 QC（0-25）、阈值电位（0-40mV）等维度的全空间覆盖。
*   **充分性评价**：
    *   **理论充分性**：提供了严谨的数学证明（见附录），确保了解析解的可靠性。
    *   **仿真充分性**：通过热图和曲线图展示了参数变化对结果的影响，逻辑链条完整。
    *   **局限性**：实验主要基于理想化的随机模型，缺乏与真实生物电生理记录数据的直接大规模拟合对比（虽然引用了前作中关于 MNTB-LSO 突触的观察）。

### 6. 主要结论与发现
*   **反直觉现象**：在自适应阈值模型中，**增加抑制性输入频率在某些区间内反而会提高突触后神经元的发放频率**。这是因为抑制导致的阈值降低幅度超过了其对膜电位的压制作用。
*   **噪声分区**：识别出了一个临界抑制频率，将参数空间划分为“始终为亚指数噪声”区域和“可随兴奋频率增加转变为超指数噪声”区域。
*   **最优参数区间**：发现 ISI 噪声在中间阈值水平和中间 QC 水平时达到最小，这意味着神经元在特定生化参数下具有最高的定时精确度。

### 7. 优点（亮点）
*   **数学严谨性**：不依赖于小噪声近似，而是推导出了 ISI 矩的**精确解析解**，这在随机神经动力学研究中具有较高价值。
*   **生物合理性**：引入自适应阈值来模拟后抑制易化（Post-inhibitory facilitation），比传统的固定阈值模型更贴近真实的神经生理特性。
*   **预测性**：模型成功预测了抑制信号对发放频率的正向调节作用，为理解复杂的神经环路计算提供了新视角。

### 8. 不足与局限
*   **模型简化**：假设量子含量（QC）为独立同分布（i.i.d.），忽略了突触囊泡释放的短时程可塑性（如耗尽或易化导致的连续相关性）。
*   **维度限制**：目前仅分析了单对 EI 输入，未考虑大规模神经元网络中的群体效应和突触电导的非线性整合。
*   **缺乏实测验证**：论文结论主要源于数学模型和仿真，尚未在活体（in vivo）实验中得到直接验证。

（完）
