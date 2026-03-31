---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 使用监督学习和强化学习微调 Qwen3-14B 基础模型
tldr: 本研究针对传统衰老时钟模型在多模态和生物学解释上的局限性，开发了Longevity-LLM v0.1。该模型基于Qwen3-14B，通过对DNA甲基化、蛋白质组学、临床生物标志物和RNA表达数据进行监督微调和强化学习。实验表明，Longevity-LLM在衰老预测和蛋白质组生成等任务上表现卓越，甚至超越了Horvath多组织时钟，证明了单一基础模型在衰老研究中替代专用模型的潜力。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 传统的衰老时钟模型受限于固定模态和预设特征，缺乏跨领域的生物学解释能力。
method: 基于Qwen3-14B模型，利用DNA甲基化、蛋白质组、临床指标及RNA数据，通过监督微调和强化学习进行训练。
result: 模型在Longevity Bench中表现优异，表观遗传年龄预测误差仅为4.34年，且在蛋白质组生成任务上显著优于现有前沿大模型。
conclusion: 单一的中等规模大语言模型能够跨模态匹配甚至取代专用衰老时钟，为药物研发和衰老研究提供了新的基础模型范式。
---

## 摘要
衰老时钟范式已经产生了数十种专门模型，能够从几乎任何类型的生物数据中估算生理年龄或死亡率。然而，此类模型均在固定模态内运行，依赖于预定义的特征集，且产生的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 Qwen3-14B 的模型，通过监督学习和强化学习方案在 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据上进行了微调。Longevity-LLM 在最近公布的 Longevity Bench 中获得了很高的排名，涵盖了癌症生存率以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测，Longevity-LLM 还能执行许多其他任务，包括蛋白质组图谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个规模适中的 LLM 可以在不同数据模态下匹配或取代专门构建的衰老时钟。本项工作是科学多模态 AI 健身房（MMAI）初始阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities. This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

### 论文总结：Longevity-LLM v0.1 —— 衰老时钟的终结

#### 1. 核心问题与研究动机
*   **核心问题**：传统的“衰老时钟”（Aging Clocks）模型存在三大局限：
    1.  **模态孤立**：每个模型仅限于单一生物数据类型（如仅DNA甲基化或仅蛋白质组），无法处理缺失数据或跨模态整合。
    2.  **特征预设**：依赖固定的特征集，缺乏灵活性。
    3.  **解释性差**：仅给出年龄数值，无法解释“为什么”生物年龄偏高，需依赖额外的生物信息学工具。
*   **研究背景**：作者提出 Longevity-LLM，旨在打破专用模型的壁垒，通过大语言模型（LLM）内化衰老生物学知识，构建一个能够跨模态推理、预测并生成生物图谱的通用基础模型。

#### 2. 方法论：核心思想与技术细节
*   **核心思想**：采用“衰老时钟蒸馏”技术，将多种组学数据和已有的衰老时钟知识转化为结构化的文本 Traces，对基础 LLM 进行微调。
*   **关键技术流程**：
    1.  **监督微调 (SFT)**：在包含 38 个任务、约 11 亿 Token 的多模态数据集上进行全参数微调。任务涵盖年龄回归、死亡率分类、特征重要性比较及生物学推理。
    2.  **强化微调 (RFT)**：基于 SFT 模型，利用 **Group Relative Policy Optimization (GRPO)** 算法在 7 个可验证的回归任务上进一步优化。
*   **奖励函数设计**：RFT 阶段采用了复合奖励函数，包括：
    *   **格式奖励**：确保模型正确使用推理标签（`<think>`）。
    *   **思考长度奖励**：激励模型进行深入推理（最高 5000 字符）。
    *   **回归准确性奖励**：根据预测值与真实值的绝对误差进行评分，并进行跨任务归一化。

#### 3. 实验设计与 Benchmark
*   **数据集**：
    *   **DNA 甲基化 (DNAm)**：41.6 万个样本，包含 CpG 位点 beta 值。
    *   **临床指标**：来自 NHANES 数据集，涉及死亡率和生存时间预测。
    *   **转录组 (RNA)**：来自 GTEx，用于组织年龄预测。
    *   **蛋白质组**：来自 Olink 平台，用于年龄回归和图谱生成。
*   **Benchmark**：
    *   **Longevity Bench**：包含肿瘤预后、年龄和死亡预测等 7 项任务。
    *   **对比方法**：15 个前沿商用 LLM（如 Gemini 1.5 Pro、GPT-4 等）以及专业的衰老时钟（如 Horvath 多组织时钟、PAC、Proteoclock）。

#### 4. 资源与算力
*   **SFT 阶段**：使用 **24 台 NVIDIA B200 GPU**。训练消耗约 45 亿 Token，经历 3000 个优化步骤。
*   **RFT 阶段**：使用 **16 台 NVIDIA A100 (80GB) GPU**。训练经历 2000 个步骤。
*   **模型基础**：基于 Qwen3-14B 架构。

#### 5. 实验数量与充分性
*   **实验规模**：涵盖了 4 大生物模态，总训练样本量近 80 万。
*   **充分性评价**：
    *   **多维度验证**：不仅测试了预测精度（MAE、相关系数），还测试了生成能力（Jaccard 指数）和分类准确率。
    *   **严谨性**：采用了受试者级别的训练/测试集划分，防止数据泄露；使用自助法（Bootstrap）计算置信区间和显著性差异（p-value）。
    *   **对比公平性**：在相同的留出集上直接对比了经典的 Horvath 时钟，具有较强的说服力。

#### 6. 主要结论与发现
*   **超越专用模型**：Longevity-LLM 在表观遗传年龄预测上的 MAE 为 **4.34 年**，显著优于经典的 Horvath 时钟（4.61 年）。
*   **Longevity Bench 夺冠**：在 7 项任务中的 4 项排名第一，尤其在 RNA 癌症预后和 10 年死亡率预测上表现卓越。
*   **涌现生成能力**：在给定年龄和性别生成蛋白质组图谱的任务中，其表现远超所有前沿商用 LLM，显示模型内化了复杂的生物学规律。
*   **架构通用性**：证明了无需修改标准 Transformer 架构（如增加预测头或特殊 Token），仅靠文本格式的数值输入即可处理复杂的组学回归任务。

#### 7. 优点与亮点
*   **单模型多模态**：实现了“一个模型解决所有衰老预测问题”，降低了多模态研究的成本。
*   **推理能力**：通过 RFT 引入了思维链（CoT），使模型能够尝试解释分子特征与表型之间的逻辑关系。
*   **高性能**：以 14B 的适中参数量，在特定领域击败了参数量大得多的通用模型。

#### 8. 不足与局限
*   **生物逻辑解释尚浅**：虽然引入了推理标签，但模型从低级分子特征到高级表型解释的深度仍需在 v0.2 版本中进一步加强。
*   **数据依赖性**：蛋白质组学等部分模态的训练数据量相对较小（约 7800 个样本），可能限制了模型在该领域的泛化上限。
*   **黑盒风险**：尽管比传统时钟更具解释性，但 LLM 内部的决策机制依然复杂，存在产生“幻觉”生物学解释的潜在风险。

（完）
