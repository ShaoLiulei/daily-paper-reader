---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 针对衰老与长寿推理微调基础模型
tldr: 传统的衰老时钟模型通常局限于单一数据模态且缺乏生物学解释力。本研究推出了Longevity-LLM v0.1，这是一个基于Qwen3-14B的大语言模型，通过对DNA甲基化、蛋白质组学、临床生物标志物和RNA表达数据进行监督微调和强化学习训练。该模型在Longevity Bench多项任务中表现优异，不仅在表观遗传年龄预测上超越了经典的Horvath时钟，还能生成蛋白质组图谱，证明了单一基础模型可以跨模态替代专用衰老时钟。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 旨在解决传统衰老时钟模型模态固定、特征预设且生物学解释性受限的问题。
method: 基于Qwen3-14B模型，利用多模态生物数据通过监督微调和强化学习构建了Longevity-LLM。
result: 模型在年龄预测和癌症生存分析等任务中表现卓越，其表观遗传年龄预测精度超过了Horvath多组织时钟。
conclusion: 研究证明了中等规模的基础模型能够跨模态匹配甚至超越专用衰老时钟，开启了长寿研究的新范式。
---

## 摘要
衰老时钟范式已催生出数十种专门模型，能够从几乎任何类型的生物数据中估算实足年龄或死亡率。然而，此类模型均在固定模态内运行，依赖预定义的特征集，且提供的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 Qwen3-14B 的模型，通过监督学习和强化学习方案，在 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据上进行了微调。Longevity-LLM 在最近发布的 Longevity Bench 中名列前茅，涵盖了癌症生存率以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测，Longevity-LLM 还能执行多项其他任务，包括蛋白质组图谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个规模适中的 LLM 可以在跨数据模态的任务中匹配或取代专门构建的衰老时钟。本项工作是我们的科学多模态人工智能实验室（MMAI）初始阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities.

This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

### 论文总结：Longevity-LLM v0.1 —— 衰老时钟的终结

#### 1. 核心问题与研究动机
*   **核心问题**：传统的“衰老时钟”（Aging Clocks）模型存在三大局限：
    1.  **模态孤立**：每个模型仅限于单一生物数据类型（如仅 DNA 甲基化或仅蛋白质组），无法处理缺失数据或跨模态整合。
    2.  **解释性差**：模型仅输出年龄数值，无法解释生物学背后的“为什么”。
    3.  **维护成本高**：增加新模态需要重新构建、验证和部署完全不同的模型。
*   **研究背景**：作者提出将大语言模型（LLM）作为生物学基础模型，通过“衰老时钟蒸馏”技术，将多种生物模态的知识内化到单一模型中，旨在构建一个能理解衰老生物学、跨模态推理的“医药超级智能”。

#### 2. 方法论：核心思想与技术细节
*   **核心思想**：不将 LLM 仅作为调用工具的代理（Agent），而是通过大规模生物数据微调，让模型直接理解组学数据。
*   **关键技术流程**：
    1.  **数据转化**：将 DNA 甲基化（CpG 位点 beta 值）、蛋白质丰度、基因表达和临床指标转化为结构化的文本 Prompt。
    2.  **监督微调（SFT）**：在 76.6 万个样本（10.9 亿 Token）上进行全参数微调，包含 38 个任务，引入推理链（CoT）以增强逻辑。
    3.  **强化微调（RFT）**：使用 **GRPO（组相对策略优化）** 算法。
        *   **奖励函数**：由格式奖励（检查思考标签）、思考长度奖励（鼓励深入推理）和回归准确性奖励（基于预测值与真实值的绝对误差归一化）组成。
        *   **目标**：针对 7 个可验证的回归任务（如年龄预测）进一步优化精度。

#### 3. 实验设计与 Benchmark
*   **数据集**：
    *   **DNA 甲基化**：41.6 万个样本，包含 CpG 位点数据及功能注释。
    *   **临床数据**：来自 NHANES，涵盖年龄预测、死亡率分类及生存时间。
    *   **转录组**：来自 GTEx，用于组织年龄比较和预测。
    *   **蛋白质组**：来自 Olink Explore 3072 平台，用于年龄回归和图谱生成。
*   **对比基准（Benchmark）**：
    *   **Longevity Bench**：与 15 个前沿商业模型（如 Gemini 1.5 Pro, GPT-4 等）对比。
    *   **专用时钟**：在 DNA 甲基化任务上对比经典的 **Horvath 多组织时钟**；在蛋白质组任务上对比 **PAC** 和 **Proteoclock**。

#### 4. 资源与算力
*   **SFT 阶段**：使用 **24 台 NVIDIA B200 GPU**。训练消耗约 45 亿 Token，经历 3000 个优化步骤。
*   **RFT 阶段**：使用 **16 台 NVIDIA A100 (80GB) GPU**。训练 2000 个步骤，有效 Batch Size 为 16。
*   **模型基础**：基于 Qwen3-14B 开源模型。

#### 5. 实验数量与充分性
*   **实验规模**：涵盖了 4 大主要生物模态，共 38 个子任务。
*   **充分性评价**：
    *   **客观性**：采用了严格的“受试者级别”拆分（Subject-level split），确保训练集和测试集无重叠，防止数据泄露。
    *   **对比公平性**：在与 Horvath 时钟对比时，使用了该时钟未见过的 1436 个独立样本。
    *   **多样性**：不仅做了回归（预测年龄），还做了分类（死亡预测）和生成（蛋白质图谱预测）实验。
    *   **局限**：由于是“十天冲刺”的初步报告，消融实验细节较少，且蛋白质组样本量（约 7800 个）相对较小。

#### 6. 主要结论与发现
*   **超越专用模型**：经过 RFT 后，Longevity-LLM 在表观遗传年龄预测上的 MAE 达到 **4.34 年**，显著优于 Horvath 时钟（4.61 年）。
*   **跨模态全能**：在 Longevity Bench 的 7 项任务中，14B 规模的模型在 4 项中排名第一，超越了参数量大得多的前沿商业模型。
*   **生成能力**：在根据年龄和性别生成蛋白质组图谱的任务中，其 Jaccard 指数远超其他 LLM，显示出模型内化了生物学规律而非简单的数值映射。
*   **架构通用性**：证明了标准的文本 Transformer 架构无需修改（如无需专门的数值编码头）即可处理复杂的组学数据。

#### 7. 优点与亮点
*   **范式突破**：提出了“单体模型（Monolithic Model）”优于“工具集成代理（Agent）”的观点，强调了内部生物学表征的一致性。
*   **高效蒸馏**：成功将过去十年积累的多种衰老时钟知识“压缩”进一个 14B 模型中。
*   **强化学习应用**：展示了 RFT（特别是 GRPO）在提升生物学数值预测精度方面的巨大潜力。

#### 8. 不足与局限
*   **解释性尚未完全释放**：虽然模型具备推理链，但本文尚未详细展示其如何从分子特征推导出表型解释的具体案例。
*   **数据偏差风险**：训练数据主要来自公开数据库（如 NHANES, GTEx），可能存在人群分布偏差（如种族、地域）。
*   **小样本模态限制**：蛋白质组数据量远小于甲基化数据，可能限制了模型在该领域的泛化上限。
*   **实时性与成本**：全参数微调和强化学习对算力要求极高，普通实验室难以复现或持续更新。

（完）
