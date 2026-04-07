---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 通过监督学习和强化学习微调基础模型
tldr: 针对传统衰老时钟模型在多模态处理和生物学解释上的局限性，本研究推出了Longevity-LLM v0.1。该模型基于Qwen3-14B，通过对DNA甲基化、蛋白质组学、临床指标及RNA表达等多种生物数据进行监督和强化学习微调，实现了跨模态的衰老预测与推理。它在Longevity Bench中表现优异，不仅在表观遗传年龄预测上超越了经典的Horvath时钟，还能生成蛋白质组图谱，证明了单一基础模型可以替代多种专用衰老时钟。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 传统的衰老时钟模型通常局限于单一数据模态且缺乏生物学解释力，难以应对复杂的长寿研究需求。
method: 基于Qwen3-14B模型，利用DNA甲基化、蛋白质组、临床生物标志物和RNA表达数据，通过监督微调和强化学习进行训练。
result: 模型在表观遗传年龄预测中达到了4.34年的平均绝对误差，超越了Horvath多组织时钟，并在蛋白质组图谱生成等任务中表现卓越。
conclusion: 研究证明了中等规模的基础模型能够跨模态匹配甚至取代专用衰老时钟，为药物研发和衰老研究提供了新的范式。
---

## 摘要
衰老时钟范式已经产生了数十种专门模型，能够从几乎任何类型的生物数据中估算生理年龄或死亡率。然而，此类模型均在固定模态内运行，依赖于预定义的特征集，且产生的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据，通过监督学习和强化学习方案进行微调的 Qwen3-14B 模型。Longevity-LLM 在最近公布的 Longevity Bench 中名列前茅，涵盖了癌症生存率以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测，Longevity-LLM 还能执行许多其他任务，包括蛋白质组图谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个规模适中的 LLM 可以在不同数据模态下匹配或取代专门构建的衰老时钟。本项工作是我们的“科学多模态 AI 健身房”（MMAI）初始阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities.

This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

这是一份关于论文《The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity》的结构化深入分析报告：

### 1. 论文的核心问题与整体含义
*   **研究动机**：传统的“衰老时钟”（Aging Clocks）虽然在预测生理年龄方面表现出色，但存在三大局限：
    1.  **模态孤立**：每个模型仅限于单一数据类型（如仅 DNA 甲基化或仅临床指标），无法处理多模态或缺失数据。
    2.  **缺乏解释性**：模型通常是黑盒，无法解释“为什么”某人的生物年龄高于实际年龄。
    3.  **功能单一**：仅能进行数值回归，无法进行复杂的生物学推理或跨领域任务。
*   **核心目标**：通过“衰老时钟蒸馏”技术，将多种生物模态的知识集成到一个通用的大语言模型（LLM）中，构建名为 **Longevity-LLM v0.1** 的基础模型，旨在终结专用衰老时钟的碎片化时代，实现“提示词即药物”（Prompt-to-Drug）的愿景。

### 2. 核心方法论
*   **基础架构**：基于 **Qwen3-14B** 模型进行全参数微调。
*   **核心思想**：将数值型的组学数据（如 CpG 位点的 beta 值、蛋白质丰度）转换为结构化的文本 Trace，让模型在自然语言空间内理解生物信号。
*   **关键技术流程**：
    1.  **监督微调 (SFT)**：使用约 76.6 万个样本（10.9 亿 token），涵盖 38 个任务。通过思维链（CoT）引导模型学习 CpG 位点的生物学意义、基因组注释及其与衰老的联系。
    2.  **强化微调 (RFT)**：采用 **GRPO（群组相对策略优化）** 算法。
        *   **奖励函数设计**：由格式奖励（检查推理标签）、思考长度奖励（鼓励深入推理）和回归准确性奖励（基于预测值与真实值的 MAE 归一化得分）组成。
        *   **思维链 (Thinking)**：强制模型在输出结果前进行内部推理（`<think>` 标签内）。

### 3. 实验设计
*   **数据集**：
    *   **DNA 甲基化 (DNAm)**：41.6 万个训练提示词，包含 CpG beta 值。
    *   **临床指标**：来自 NHANES 数据集，涉及死亡率预测和生存时间。
    *   **转录组 (RNA)**：来自 GTEx Portal，用于组织年龄比较。
    *   **蛋白质组**：来自 Olink Explore 3072 平台，涉及血浆蛋白谱。
    *   **癌症数据**：来自 TCGA，用于生存分析。
*   **Benchmark**：主要使用 **Longevity Bench**（包含肿瘤预后、年龄和死亡率预测等 7 项任务）。
*   **对比方法**：
    *   **前沿 LLM**：对比了包括 Gemini 3 Pro 在内的 15 个商业领先模型。
    *   **专用时钟**：对比了经典的 **Horvath 多组织时钟**（表观遗传学）以及 PAC、Proteoclock（蛋白质组学）。

### 4. 资源与算力
*   **SFT 阶段**：使用 **24 块 NVIDIA B200 GPU**，训练约 3000 步，全局批次大小约为 157 万 token。
*   **RFT 阶段**：使用 **16 块 NVIDIA A100 80GB GPU**，训练 2000 步。
*   **开发周期**：该模型是在一个为期 **10 天** 的快速开发冲刺（Sprint）中完成的。

### 5. 实验数量与充分性
*   **实验规模**：涵盖了 4 大主要生物模态，总计近 100 万个训练/测试样本。
*   **充分性评价**：
    *   **多维度验证**：不仅测试了年龄回归，还测试了分类（死亡率）、排序（谁更老）和生成（蛋白质谱预测）任务。
    *   **客观性**：采用了严格的“受试者级别”拆分（Subject-level split），防止数据泄露；使用了 10,000 次迭代的自助法（Bootstrap）进行显著性检验。
    *   **对比公平性**：在 DNAm 预测中，使用了 Horvath 时钟未见过的独立测试集进行公平对决。

### 6. 主要结论与发现
*   **超越专用模型**：经过 RFT 后，Longevity-LLM 在表观遗传年龄预测上的 MAE 达到 **4.34 年**，显著优于经典的 Horvath 时钟（4.61 年）。
*   **跨模态统治力**：尽管只有 14B 参数，但在 Longevity Bench 的 7 项任务中，有 4 项排名第一，超越了参数量大得多的商业模型。
*   **涌现生成能力**：在给定年龄和性别预测蛋白质丰度图谱的任务中，其 Jaccard 指数远超其他 LLM，证明模型内部形成了连贯的生物学表征。
*   **架构通用性**：证明了标准文本 Transformer 架构无需修改（如无需专用 Tokenizer 或预测头）即可处理复杂的组学数值数据。

### 7. 优点与亮点
*   **打破碎片化**：用一个“单体模型”（Monolithic Model）取代了数十个专用工具，降低了多模态研究的门槛。
*   **推理驱动**：通过 RFT 引入了思维链，使模型能够尝试解释其预测背后的生物逻辑，而不仅仅是给出数字。
*   **高效转化**：展示了如何通过 10 天的冲刺，利用现有开源底座（Qwen3）快速构建垂直领域的“超级智能”。

### 8. 不足与局限
*   **解释性尚浅**：虽然引入了推理过程，但模型将低级分子特征转化为高级表型解释的能力仍处于初级阶段（计划在 v0.2 改进）。
*   **数据规模限制**：蛋白质组学等模态的训练数据相对较小（约 7800 个样本），可能限制了其在这些领域的泛化上限。
*   **幻觉风险**：作为生成式模型，在处理极端数值或罕见生物样本时，仍存在产生生物学错误逻辑的潜在风险。
*   **应用范围**：目前主要集中在人类数据，尚未广泛扩展到其他物种或更复杂的干预实验预测。

（完）
