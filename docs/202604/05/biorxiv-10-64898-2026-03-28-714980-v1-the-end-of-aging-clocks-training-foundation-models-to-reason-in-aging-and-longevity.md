---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 使用监督学习和强化学习对基础模型进行微调
tldr: 针对传统衰老时钟模型功能单一、缺乏生物学解释力的问题，本研究推出了Longevity-LLM v0.1。该模型基于Qwen3-14B，通过监督微调和强化学习，整合了DNA甲基化、蛋白质组学、临床生物标志物及RNA表达等多模态数据。它在Longevity Bench多项任务中表现优异，不仅在表观遗传年龄预测上超越了经典的Horvath时钟，还能生成蛋白质组图谱，证明了单一基础模型可替代多种专用衰老时钟。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 传统衰老时钟受限于固定模态和特征集，难以提供深入的生物学解释，且缺乏跨领域的通用性。
method: 基于Qwen3-14B模型，利用DNA甲基化、蛋白质组、临床指标和RNA表达数据，通过监督学习与强化学习进行多模态微调。
result: 模型在表观遗传年龄预测中达到4.34年平均绝对误差，优于Horvath时钟，并在蛋白质组图谱生成等任务中显著领先于其他前沿大模型。
conclusion: 研究证明了中等规模的基础模型能够跨模态整合生物数据，在衰老研究和长寿预测中达到或超越专用模型的性能。
---

## 摘要
衰老时钟范式已产生了数十种专业模型，能够从几乎任何生物数据类型中估算实足年龄或死亡率。然而，每种此类模型都在固定的模态内运行，依赖于预定义的特征集，且产生的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 Qwen3-14B 的模型，通过监督学习和强化学习方案，在 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据上进行了微调。Longevity-LLM 在最近公布的 Longevity Bench 中名列前茅，涵盖了癌症生存预测以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测，Longevity-LLM 还能执行许多其他任务，包括蛋白质组谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个规模适中的 LLM 可以在跨数据模态的任务中匹配或取代专门构建的衰老时钟。这项工作构成了我们“科学多模态 AI 健身房”（MMAI）初始冲刺阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities.

This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

### 论文总结：衰老时钟的终结——训练基础模型在衰老与长寿领域进行推理

#### 1. 论文的核心问题与整体含义
*   **研究背景**：自 2010 年代中期以来，衰老研究领域涌现了大量基于深度学习的“衰老时钟”（Aging Clocks），用于预测生物年龄或死亡率。
*   **核心问题**：现有的衰老时钟存在三大局限：
    1.  **模态单一**：每个模型仅限于特定的生物数据（如仅 DNA 甲基化或仅蛋白质组），难以处理多模态或缺失数据。
    2.  **解释性差**：模型仅给出数值，无法解释为何某人的生物年龄高于实足年龄。
    3.  **工具碎片化**：现有的 AI 代理系统仅将 LLM 作为调度器，底层工具依然是孤立且僵化的。
*   **研究动机**：开发一个名为 **Longevity-LLM v0.1** 的通用基础模型，通过将衰老生物学知识和多模态数据“蒸馏”进模型参数中，使其能够直接理解并推理衰老过程，目标是构建“从提示词到药物”（Prompt-to-Drug）的制药超智能系统。

#### 2. 论文提出的方法论
*   **核心思想**：不依赖外部工具，而是通过大规模多模态数据微调，让 LLM 内部化衰老生物学逻辑。
*   **关键技术细节**：
    *   **基础模型**：选用 **Qwen3-14B** 作为基座模型。
    *   **监督微调 (SFT)**：使用 76.6 万个示例（约 10.9 亿 token），涵盖 38 个任务。通过将组学数据（如 CpG 位点值）转换为文本格式，并加入推理链（Reasoning Traces）来训练模型。
    *   **强化微调 (RFT)**：在 SFT 基础上，利用 **GRPO（组相对策略优化）** 算法针对 7 个回归任务进行优化。
    *   **奖励函数设计**：
        1.  **格式奖励**：确保模型正确使用 `<think>` 标签。
        2.  **思考长度奖励**：鼓励模型进行深入推理（最高 5000 字符）。
        3.  **回归准确性奖励**：根据预测值与真实值的绝对误差进行评分，并进行跨任务归一化。

#### 3. 实验设计
*   **数据集**：
    *   **DNA 甲基化 (DNAm)**：最大的模态，包含 CpG 贝塔值、特征重要性比较等。
    *   **临床生物标志物**：来自 NHANES 数据集，涉及年龄预测、死亡率分类及生存时间预测。
    *   **转录组学 (RNA)**：来自 GTEx，用于组织年龄预测和比较。
    *   **蛋白质组学**：来自 Olink Explore 3072 平台，包含年龄回归和蛋白质谱生成任务。
*   **Benchmark**：**Longevity Bench**（包含肿瘤预后、年龄和死亡率预测等任务）。
*   **对比方法**：
    *   **LLM 对比**：与 GPT-4、Gemini 1.5 Pro 等 15 个前沿商用大模型对比。
    *   **专用模型对比**：在 DNAm 任务上对比经典的 **Horvath 多组织时钟**；在蛋白质组任务上对比 **PAC** 和 **Proteoclock**。

#### 4. 资源与算力
*   **SFT 阶段**：使用 **24 台 NVIDIA B200 GPU**，训练约 3000 步，消耗约 45 亿 token。
*   **RFT 阶段**：使用 **16 台 NVIDIA A100 80GB GPU**，训练 2000 步。
*   **开发周期**：该模型是在一个为期 **10 天** 的初始开发冲刺中完成的。

#### 5. 实验数量与充分性
*   **实验规模**：涵盖了 4 大主要生物模态，总训练样本接近 100 万。
*   **评估方法**：采用了严格的**受试者级别（Subject-level）**划分，防止数据泄露。使用了留出集（Holdout set）进行验证，并利用自助法（Bootstrap）计算置信区间和 p 值。
*   **客观性**：实验不仅对比了通用 LLM，还直接挑战了该领域的“金标准”专用模型（如 Horvath 时钟），对比维度较为全面且客观。

#### 6. 主要结论与发现
*   **性能卓越**：Longevity-LLM v0.1 在 Longevity Bench 的 7 项任务中有 4 项排名第一，超越了参数量更大的商用模型。
*   **超越专用时钟**：经过 RFT 后，模型在表观遗传年龄预测上的 MAE 达到 **4.34 年**，显著优于 Horvath 时钟（4.61 年）。
*   **跨模态生成能力**：在根据年龄和性别生成蛋白质组谱的任务中，其 Jaccard 指数显著高于所有其他前沿 LLM，证明模型内化了蛋白质组的动态规律。
*   **架构通用性**：证明了标准的文本 Transformer 架构无需修改（如无需专用 Tokenizer 或预测头）即可处理复杂的组学数值数据。

#### 7. 优点
*   **打破模态壁垒**：实现了单一模型处理多模态生物数据，解决了传统时钟无法处理缺失特征的问题。
*   **强化学习的应用**：成功将 RFT 引入生物回归任务，通过奖励函数显著提升了预测精度。
*   **内部一致性**：作为一个“单体模型”（Monolithic Model），它比代理系统更容易产生跨生物尺度的内在逻辑一致性。

#### 8. 不足与局限
*   **中期报告性质**：目前仅为 v0.1 版本，虽然预测精度高，但在“解释生物学逻辑”方面的叙述能力仍需在后续版本（v0.2）中加强。
*   **数据依赖**：蛋白质组学等部分模态的训练数据量相对较小，可能存在过拟合风险。
*   **计算成本**：虽然模型仅 14B，但训练过程（尤其是 RFT）对算力要求较高，且生物系统的复杂性使得定义完美的奖励函数依然具有挑战性。

（完）
