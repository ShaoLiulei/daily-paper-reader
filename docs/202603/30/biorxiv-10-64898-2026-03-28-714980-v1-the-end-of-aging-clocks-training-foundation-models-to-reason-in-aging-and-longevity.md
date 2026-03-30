---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 针对特定生物推理任务微调大语言模型
tldr: 本研究针对传统衰老时钟模型在多模态数据处理和生物学解释方面的局限性，提出了Longevity-LLM v0.1。该模型基于Qwen3-14B，通过对DNA甲基化、蛋白质组学、临床生物标志物和RNA表达数据进行监督微调和强化学习训练。Longevity-LLM在Longevity Bench中表现优异，其表观遗传年龄预测精度超越了经典的Horvath时钟，并能执行蛋白质组谱生成等多种任务，展示了单一基础模型替代专用衰老时钟的潜力。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 传统的衰老时钟模型受限于固定模态和预设特征，难以提供跨领域的生物学解释和多任务处理能力。
method: 基于Qwen3-14B模型，利用DNA甲基化、蛋白质组、临床指标及RNA数据，通过监督微调和强化学习构建多模态基础模型。
result: 模型在表观遗传年龄预测上达到4.34年平均绝对误差，超越了Horvath多组织时钟，并在蛋白质组谱生成等任务中显著优于现有前沿大模型。
conclusion: 研究证明了中等规模的基础模型能够跨模态匹配或取代专用衰老时钟，为药物研发和衰老研究提供了全新的多模态AI范式。
---

## 摘要
衰老时钟范式已经产生了数十种专业模型，能够从几乎任何类型的生物数据中估算生理年龄或死亡率。然而，每种此类模型都在固定的模态内运行，依赖于预定义的特征集，且产生的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 Qwen3-14B 的模型，通过监督学习和强化学习方案在 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据上进行了微调。Longevity-LLM 在最近公布的 Longevity Bench 中获得了很高的排名，包括癌症生存预测以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测外，Longevity-LLM 还可以执行许多其他任务，包括蛋白质组图谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个中等规模的 LLM 可以在不同数据模态下匹配或取代专门构建的衰老时钟。这项工作构成了我们“科学多模态 AI 健身房”（MMAI）初始冲刺阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities. This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

### 论文结构化深度总结：Longevity-LLM v0.1

#### 1. 核心问题与整体含义（研究动机和背景）
传统的“衰老时钟”（Aging Clocks）虽然在生物年龄预测上表现出色，但存在三大核心局限：
*   **模态孤立**：每个模型仅针对单一数据类型（如仅 DNA 甲基化或仅蛋白质组），无法处理缺失数据或跨模态整合。
*   **解释性匮乏**：模型通常是黑盒，无法解释为何某人的生物年龄高于生理年龄。
*   **功能单一**：仅能进行数值回归，缺乏生物学推理能力。
本研究提出了 **Longevity-LLM v0.1**，旨在打破专用时钟的范式，通过将衰老知识和多模态生物数据“蒸馏”进一个大语言模型（LLM），使其成为能够理解、推理并预测衰老生物学的通用基础模型。

#### 2. 论文提出的方法论
核心思想是利用大规模生物组学数据对通用 LLM 进行**监督微调（SFT）**和**强化微调（RFT）**。
*   **模型基础**：选用 **Qwen3-14B** 作为基座模型。
*   **监督微调 (SFT)**：
    *   将组学数据（如 CpG 位点 beta 值、蛋白质丰度）转化为文本格式。
    *   构建包含推理链（Reasoning Traces）的指令对，使模型学习生物学背景和特征重要性。
*   **强化微调 (RFT)**：
    *   采用 **GRPO（组相对策略优化）** 算法。
    *   **复合奖励函数**：包含**格式奖励**（确保输出特定标签）、**思考长度奖励**（鼓励模型进行深度推理）和**回归准确性奖励**（基于预测值与真实值的归一化绝对误差）。
    *   通过 RFT 优化模型在数值预测任务上的精确度。

#### 3. 实验设计
*   **数据集**：
    *   **DNA 甲基化 (DNAm)**：41.6 万个训练样本，涵盖多个公开时钟的 CpG 位点。
    *   **临床数据 (NHANES)**：22.8 万个样本，涉及年龄预测、死亡率和生存时间。
    *   **转录组 (GTEx)**：9.8 万个样本，用于组织年龄比较。
    *   **蛋白质组 (Olink)**：约 7800 个样本，用于年龄回归和谱图生成。
*   **Benchmark**：使用 **Longevity Bench**（包含癌症生存、年龄预测等 7 项任务）。
*   **对比方法**：
    *   **通用 LLM**：与 GPT-4、Gemini 1.5 Pro、Claude 3.5 Sonnet 等 15 个前沿模型对比。
    *   **专用时钟**：与 Horvath 多组织甲基化时钟、PAC、Proteoclock 等专业模型对比。

#### 4. 资源与算力
论文明确记录了训练所需的算力资源：
*   **SFT 阶段**：使用 **24 台 NVIDIA B200 GPU**，处理约 45 亿 token，耗时未明确但属于“10天冲刺”的一部分。
*   **RFT 阶段**：使用 **16 台 NVIDIA A100 80GB GPU**，运行 2000 个 step。
*   **上下文窗口**：SFT 使用 64k 窗口，RFT 使用 16k 窗口。

#### 5. 实验数量与充分性
*   **实验规模**：训练语料包含 76.6 万个示例（10.9 亿 token），涵盖 38 个子任务。
*   **客观性与公平性**：
    *   采用了**受试者级别（Subject-level）**的数据拆分，严格防止数据泄露。
    *   使用了留出集（Holdout set）进行最终评估。
    *   通过自助法（Bootstrap）计算置信区间和显著性差异（p-value）。
*   **充分性**：实验覆盖了从分子（DNAm）到细胞（RNA/蛋白）再到表型（临床/生存）的多个维度，对比了当前最强的通用模型和最经典的专用模型，实验设计较为严谨。

#### 6. 主要结论与发现
*   **超越专用模型**：经过 RFT 后，Longevity-LLM 在表观遗传年龄预测上的 MAE 达到 **4.34 年**，显著优于经典的 **Horvath 时钟（4.61 年）**。
*   **横扫 Longevity Bench**：在 7 项任务中的 4 项排名第一，尤其在癌症生存预测和死亡率预测上大幅领先 Gemini 1.5 Pro 等巨型模型。
*   **涌现生成能力**：在给定年龄和性别的情况下，模型能生成生物学合理的蛋白质组谱图，Jaccard 指数远超其他 LLM。
*   **架构普适性**：证明了标准文本 Transformer 架构无需修改（如无需专门的数值预测头）即可处理复杂的组学回归任务。

#### 7. 优点
*   **范式创新**：提出了“衰老时钟蒸馏”概念，将碎片化的专用工具整合进统一的对话式 AI。
*   **多模态一致性**：模型不仅能做预测，还能通过自然语言解释生物逻辑，具备跨模态推理的潜力。
*   **高效性**：仅用 14B 参数的模型，通过高质量生物数据微调，在特定领域击败了参数量大得多的通用模型。

#### 8. 不足与局限
*   **中期报告性质**：目前仅为 v0.1 版本，部分跨模态泛化假设（如一种模态的知识如何辅助另一种模态）仍需更多消融实验验证。
*   **推理深度限制**：虽然引入了 RFT 鼓励思考，但模型在解释复杂生物通路时的逻辑严密性仍有提升空间。
*   **数据依赖**：模型性能高度依赖于现有衰老时钟的系数和标注数据，若原始数据存在偏差，模型可能会继承这些偏差。
*   **应用场景**：目前主要集中在预测和生成，尚未在实际的临床决策或药物靶点发现中进行端到端的验证。

（完）
