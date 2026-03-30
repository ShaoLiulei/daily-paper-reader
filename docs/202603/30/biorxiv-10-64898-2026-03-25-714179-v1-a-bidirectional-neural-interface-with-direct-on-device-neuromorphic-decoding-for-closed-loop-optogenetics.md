---
title: A Bidirectional Neural Interface With Direct On-Device Neuromorphic Decoding for Closed-Loop Optogenetics
title_zh: 一种具有直接片上类脑解码功能的闭环光遗传学双向神经接口
authors: "Bilodeau, G., Miao, A., Gagnon-Turcotte, G., Ethier, C., Gosselin, B."
date: 2026-03-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.25.714179v1.full.pdf"
tags: ["query:snn"]
score: 9.0
evidence: 用于闭环神经接口的设备端类脑解码
tldr: 本研究针对自由活动动物闭环神经调制中无线设备计算资源受限的挑战，开发了一种集成片上类脑解码器的双向无线神经接口。该系统在Spartan-6 FPGA上实现了32通道记录、PCA降维及非线性SVM解码，通过漏积分器捕捉时间动态。实验证明，该平台在保持低功耗和低延迟的同时，解码精度媲美深度学习模型，并成功在活体大鼠中演示了实时闭环光遗传刺激，为无束缚神经科学研究提供了高效工具。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-001.webp\", \"caption\": \"Fig. 10. Neural decoding in vivo during anesthesia. a) Experimental setup with a 32-channel electrode array implanted in rat motor cortex and a fiber-optic cannula targeting the VTA. b) Packaged wireless headstage connected via a Molex-to-Omnetics adapter and coupled to the optical cannula for stimulation. c) Overlaid MUA from all 32 channels during anesthesia, showing representative waveforms. d) Raster plot with population firing rate and real-time decoder output. The decoder was trained on data from the same rat (10-ms bins, 10-ms LI decay) for fast, low-latency firing-rate prediction. e) Wireless closed-loop results using a longer accumulation model (50-ms bins, 150-ms LI decay), integrating larger temporal dynamics of the neural signal. When predicted activity exceeded the threshold (dotted line) for 50 ms, a 300-ms optical pulse was delivered, followed by a 2-s refractory period. Stimulation periods are shown in green, refractory period in grey. f) Average population firing rate across two rats before, during, and after closed-loop stimulation.\", \"page\": 11, \"index\": 1, \"width\": 1076, \"height\": 852}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-002.webp\", \"caption\": \"Fig. 1. Block diagram and overall concept of the wireless headstage and neural decoder. Left: A rat performs a lever-pull task while carrying the wireless headstage. The force applied to the lever can be predicted in real time by the onboard neural decoder using an SVM-based regressor. Right: Block diagram of the decoding pipeline, showing the neural interface, digital signal processing stages, binned spike counts, leaky-integrator filtering, PCA-based feature extraction, and the nonlinear SVM decoder. The decoder output can be used to drive closed-loop optical stimulation.\", \"page\": 2, \"index\": 2, \"width\": 1076, \"height\": 521}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-003.webp\", \"caption\": \"TABLE I COMPARISON OF ACCURACY FOR DIFFERENT FEATURES AND DECODERS, HIGHLIGHTING THE FEATURE SIZE OF EACH CASE.\", \"page\": 7, \"index\": 3, \"width\": 529, \"height\": 615}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-004.webp\", \"caption\": \"Fig. 7. Pie chart of the headstage power consumption per module and a close up on the usage of the neural decoder building blocks implemented on the FPGA.\", \"page\": 7, \"index\": 4, \"width\": 505, \"height\": 244}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-005.webp\", \"caption\": \"Fig. 9. Classification performance comparison of multiple classifiers on the rat lever-pulling dataset across four recording days. a) Accuracy of the classifiers across the four days. b) Macro F1 score over the same period. c) Macro precision over the same period. d) Macro recall over the same period.\", \"page\": 10, \"index\": 5, \"width\": 529, \"height\": 375}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-006.webp\", \"caption\": \"Fig. 2. Two-sided view of the rigid-flex PCB when not folded [33]\", \"page\": 3, \"index\": 6, \"width\": 474, \"height\": 429}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-007.webp\", \"caption\": \"TABLE III SYSTEM-LEVEL COMPARISON WITH STATE-OF-THE-ART NEURAL DECODERS AND SIGNAL PROCESSING SYSTEMS.\", \"page\": 13, \"index\": 7, \"width\": 1078, \"height\": 825}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-008.webp\", \"caption\": \"TABLE II RESOURCE USAGE AND PERFORMANCE COMPARISON OF DIFFERENT NEURAL DECODERS.\", \"page\": 8, \"index\": 8, \"width\": 1040, \"height\": 261}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-009.webp\", \"caption\": \"Fig. 3. R2 for different number of principal components kept when predicting the x and y-forces using the dataset from the center-out isometric wrist force task from [37] using an SVM decoder\", \"page\": 4, \"index\": 9, \"width\": 396, \"height\": 317}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-010.webp\", \"caption\": \"Fig. 8. Wireless neural decoder headstage: experimental results and validation with synthetic data played from an arbitrary waveform generator. a) Model training workflow. On the left, a 32-channel synthetic recording with overlaid MUA threshold crossings shows signal capture and detection. Timestamps are used to compute spike-count bins, optimize the LI decay constant, and extract PCA coefficients (gray). Features and population firing rate are clustered to reduce model size, and an SV regressor is trained to predict firing rate. Feature parameters and the trained SV model are transferred via BLE at startup. Recorded activity along with the neural decoder prediction are then transferred wirelessly to the base station in subsequent experiments. b) Wireless decoding results. Top: raster plot of detected MUA across channels. Bottom: population firing rate, on-device prediction, and computer-based prediction from logged MUA (pre-quantized model). c) Experimental setup: headstage, Molex-to-Omnetics adapter, custom signal-injection board, and signal generator replaying prerecorded activity. d) Decoder output and quantization error: VAF = 0.998 and mean RMS error = 5.54%, demonstrating high on-device fidelity.\", \"page\": 9, \"index\": 10, \"width\": 1076, \"height\": 983}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-011.webp\", \"caption\": \"Fig. 4. Training process of the proposed neural decoder and its model reduction performance with, a) the cluster based data reduction, from left to right, the monkey performs a behavioral task, while MUA is recorded in the motor cortex to form a training dataset for the SVM algorithm. This data set is clustered using k-means to reduce the size of the training dataset and thus reduce the SVM model size. The SVM is trained on this new, reduced dataset to predict the X and Y wrist forces during a center out isometric wrist force task b) its performance predicting the X and Y-axis forces applied by a monkey performing a center out task from 32 channels of MUA. Comparison of the R2 values for the X and Y predictions as a function of training size based on training dataset size w/ and w/o clustering.\", \"page\": 5, \"index\": 11, \"width\": 529, \"height\": 556}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-25-714179-v1/fig-012.webp\", \"caption\": \"Fig. 5. Detailed VHDL implementation of the feature extraction cores with the bin count core (top) that detects MUA threshold crossings, applies an artifact removal threshold and keeps track of the MUA events for each of the 32 channels during a customization time window (bin). A trigger is sent along with the MUA threshold crossing count for all 32 channels to the Leaky Integrator core (middle) when the time widow exceeds the user defined time. The leaky integrator core then calculates the new leaky integrator value for each channel using the user defined coefficients loaded and previous LI state into RAM and a multiply accumulate calculation block. When the 32 LI values are ready, a trigger is sent to the PCA inference core (bottom), where the LI values and the user defined PCA coefficients are used to calculate the coefficients of the 6 principal components at this time point. These 6 values are the features used in the SVM decoder.\", \"page\": 5, \"index\": 12, \"width\": 529, \"height\": 677}]"
motivation: 旨在解决现有闭环神经接口依赖外部处理器、难以在小型无线设备上实现复杂实时解码的问题。
method: 在资源受限的FPGA上部署了结合类脑特征提取、PCA降维与非线性SVM的硬件优化解码架构。
result: 解码器性能优于维纳滤波器且接近CNN，并在活体大鼠闭环光遗传实验中达到了0.9148的VAF。
conclusion: 该工作实现了一个全自洽、低功耗且高精度的无线双向神经接口平台，适用于实时闭环神经科学实验。
---

## 摘要
双向接口结合神经解码算法对于闭环（CL）神经调节至关重要，能够实现同步神经监测和响应式光遗传刺激。然而，在用于自由活动动物的小型无线头戴式设备中实现这些功能仍然具有挑战性，因为大多数现有平台依赖有线装置和外部处理器来执行计算密集型解码器。本研究介绍了一种集成在双向无线系统中的神经解码器的设计与优化，用于啮齿动物的闭环光遗传学实验。所提出的平台结合了32通道电生理记录、类脑特征提取、降维以及在资源受限的 Spartan-6 FPGA 上实现的非线性支持向量机（NL-SVM）解码器。利用脉冲计数特征和漏积分器捕捉时间动力学，同时通过主成分分析（PCA）将特征空间降至六个分量，从而以极低的内存和功耗需求实现亚毫秒级推理。在训练过程中使用 k-means 聚类来限制支持向量的数量，从而进一步减小模型尺寸。通过非人灵长类动物和大鼠运动皮层记录的数据集验证了解码器的性能。所提出的解码器实现了与卷积神经网络相当的准确度（R2 = 0.85 对比 0.87），并优于维纳滤波器（R2 = 0.81），同时所需的计算资源显著减少。整个系统通过在大鼠体内进行的无线闭环光遗传刺激得到了进一步验证，实现了 0.9148 的方差解释度（VAF）。总之，这项工作为实时、无束缚的闭环神经科学实验提供了一个多功能、完全独立且资源高效的平台。

## Abstract
Bidirectional interfaces combined with neural decoding algorithms are essential for closed-loop (CL) neuromodulation, enabling simultaneous neural monitoring and responsive optogenetic stimulation. However, implementing these capabilities in compact wireless headstages for freely moving animals remains challenging, as most existing platforms rely on tethered setups and external processors to execute computationally intensive decoders. This work presents the design and optimization of a neural decoder integrated into a bidirectional wireless system for CL optogenetic experiments in rodents. The proposed platform combines 32-channel electrophysiological recording with neuromorphic feature extraction, dimensionality reduction, and a nonlinear support vector machine (NL-SVM) decoder implemented on a resource-constrained Spartan-6 FPGA. Temporal dynamics are captured using spike-count features and leaky integrators, while principal component analysis (PCA) reduces the feature space to six components, enabling sub-millisecond inference with minimal memory and power requirements. Model size is further reduced using k-means clustering during training to limit the number of support vectors. Decoder performance was validated using datasets from non-human primate and rat motor cortex recordings. The proposed decoder achieved accuracy comparable to convolutional neural networks (R2 = 0.85 vs. 0.87) and outperformed Wiener filters (R2 = 0.81) while requiring significantly fewer computational resources. The full system was further demonstrated in vivo through wireless closed-loop optogenetic stimulation in rats, achieving a variance accounted for (VAF) of 0.9148. Overall, this work introduces a versatile, fully self-contained, and resource-efficient platform for real-time untethered closed-loop neuroscience experiments

---

## 论文详细总结（自动生成）

这是一份关于论文《A Bidirectional Neural Interface With Direct On-Device Neuromorphic Decoding for Closed-Loop Optogenetics》的结构化深入总结：

### 1. 核心问题与研究动机
*   **核心问题**：如何在资源极度受限的无线头戴式设备（Headstage）上，实现高精度、低延迟的实时神经信号解码，以支持自由活动动物的闭环光遗传学实验。
*   **研究背景**：传统的闭环神经调制系统通常依赖有线连接或将数据传输至外部高性能计算机处理，这限制了动物的自然行为，且通信延迟可能破坏生物学上的因果关系（如STDP机制要求的10-20ms窗口）。现有的片上解码方案要么过于简单（如线性回归），要么功耗过高，难以集成在小型无线设备中。

### 2. 方法论：核心思想与技术细节
该论文提出了一种**混合类脑（Hybrid-Neuromorphic）解码架构**，部署在 Spartan-6 FPGA 上，核心流程如下：
*   **特征优化（类脑提取）**：
    *   **多单位活动（MUA）检测**：通过自适应阈值检测神经脉冲（Spikes）。
    *   **漏积分器（Leaky Integrator, LI）**：模仿生物神经元动力学，将脉冲计数通过公式 $Leaky(n) = Leaky(n-1) \cdot \alpha + Bin(n) \cdot (1-\alpha)$ 进行平滑。这在不存储长历史记录的情况下捕捉了时间动态，将特征维度从数百个历史窗口压缩至32个通道特征。
*   **维度压缩（PCA）**：在 FPGA 上实现实时主成分分析推理，将32维特征进一步压缩至6个主成分，减少了后续 SVM 的计算压力。
*   **模型优化（NL-SVM）**：
    *   使用**多项式核函数**代替高斯核，以降低硬件乘法器开销。
    *   **K-means 聚类压缩**：在训练阶段对数据进行聚类，生成合成代表向量，从而在保持精度的前提下显著减少支持向量（SV）的数量，使模型能存入 FPGA 仅有的 10.5 kB 内存中。
*   **闭环控制**：解码输出直接触发光遗传刺激模块（PWM控制），实现亚毫秒级片上反馈。

### 3. 实验设计与对比
*   **数据集**：
    1.  **猕猴数据集**：中心向外等距腕力任务（32通道 MUA，预测 X/Y 轴力）。
    2.  **大鼠数据集**：杠杆拉动任务（16通道运动皮层记录，进行二分类预测）。
    3.  **合成数据验证**：通过信号发生器回放预录信号，验证硬件量产误差。
    4.  **活体实验（In vivo）**：麻醉大鼠，记录运动皮层（M1）活动并闭环刺激腹侧被盖区（VTA）。
*   **Benchmark 与对比方法**：
    *   **算法对比**：线性回归、维纳滤波器（Wiener Filter）、卷积神经网络（CNN）、长短期记忆网络（LSTM）、前馈神经网络（FFNN）。
    *   **特征对比**：原始脉冲计数 vs. 带有历史窗口的特征 vs. 漏积分器特征。

### 4. 资源与算力占用
*   **硬件平台**：Xilinx Spartan-6 FPGA。
*   **算力资源**：
    *   仅使用 **3个 MAC（乘法累加）单元**。
    *   内存占用：**10.5 kB**（用于存储支持向量和模型参数）。
    *   逻辑资源：1822个 LUT，2401个寄存器。
*   **延迟与功耗**：
    *   推理延迟：**0.254 ms**（远低于生物响应窗口）。
    *   整机功耗：解码模块仅占总功耗的一小部分（约 2 mA 电流贡献）。

### 5. 实验数量与充分性
*   **实验覆盖面**：涵盖了离线数据验证（跨物种：猴、鼠）、硬件仿真验证以及最终的活体闭环验证。
*   **充分性评价**：实验设计较为充分。作者不仅对比了不同算法的准确率（$R^2$），还详细分析了 PCA 维数选择的“拐点”、聚类压缩对模型大小与精度的权衡（消融研究）。活体实验展示了系统在真实电生理环境下的鲁棒性。

### 6. 主要结论与发现
*   **性能卓越**：提出的 NL-SVM + LI 方案在猕猴力预测任务中达到 $R^2=0.85$，性能接近计算量巨大的 CNN（0.87），显著优于维纳滤波器（0.81）。
*   **资源极省**：通过类脑特征提取，特征维度降低了 50 倍以上，使得在极低功耗的 FPGA 上运行非线性解码成为可能。
*   **闭环有效性**：活体实验中，系统能准确识别高频神经活动并实时触发 VTA 刺激，方差解释度（VAF）达 0.9148。

### 7. 优点与亮点
*   **端到端集成**：在单一无线设备上集成了记录、压缩、解码和刺激，无需外部 PC 参与决策。
*   **硬件感知优化**：通过 K-means 减少支持向量和使用多项式核，精准解决了嵌入式设备内存不足的痛点。
*   **极低延迟**：亚毫秒级的处理速度为研究神经可塑性（如 STDP）提供了理想工具。
*   **无线重构**：支持通过蓝牙实时更改解码参数和刺激逻辑，灵活性高。

### 8. 不足与局限
*   **通道数限制**：目前仅支持 32 通道，对于现代高密度探针（如 Neuropixels，数百上千通道）的片上实时处理仍有距离。
*   **训练依赖离线**：虽然推理在片上，但 PCA 系数和 SVM 支持向量仍需预先在外部计算机上训练好再上传，无法实现完全的片上自主学习。
*   **应用场景单一**：主要验证了运动解码和简单的阈值触发，对于更复杂的认知任务或多目标解码的适用性有待验证。
*   **麻醉限制**：活体闭环实验是在麻醉状态下进行的，尚未展示自由活动状态下运动伪影对解码稳定性的具体影响。

（完）
