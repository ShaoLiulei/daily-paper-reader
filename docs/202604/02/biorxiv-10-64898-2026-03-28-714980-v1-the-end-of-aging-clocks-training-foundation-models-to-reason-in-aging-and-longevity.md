---
title: "The End of Aging Clocks: Training Foundation Models to Reason in Aging and Longevity"
title_zh: 衰老时钟的终结：训练基础模型在衰老与长寿领域进行推理
authors: "Zhavoronkov, A., Aladinskyi, V., Aliper, A., Miftakhutdinov, Z., Reymond, M., Naumov, V., Zagirova, D., Pushkov, S., Sidorenko, D., Shayakhmetov, R., Galkin, F."
date: 2026-03-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.28.714980v1.full.pdf"
tags: ["query:ai-llm"]
score: 9.0
evidence: 使用监督学习和强化学习微调的基础模型
tldr: 针对传统衰老时钟模型在多模态处理和生物学解释上的局限性，本研究推出了Longevity-LLM v0.1。该模型基于Qwen3-14B，通过对DNA甲基化、蛋白质组学、临床生物标志物及RNA表达数据进行监督和强化学习微调，实现了跨模态的衰老预测与推理。它在Longevity Bench中表现优异，在表观遗传年龄预测上超越了经典的Horvath时钟，并能生成高质量蛋白质组图谱，证明了单一基础模型可替代多种专用衰老时钟。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-001.webp\", \"caption\": \"Figure 1. Longevity-LLM shows competitive performance in a range of Longevity Bench tasks. The tested tasks span the domains of transcriptomics, proteomics, and clinical record. Base Qwen-3 14B failed to produce valid outputs on all tasks.\", \"page\": 6, \"index\": 1, \"width\": 976, \"height\": 471}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-002.webp\", \"caption\": \"Figure 2. Longevity-LLM is a language model parsing the aging signal in DNAm profiles.\", \"page\": 7, \"index\": 2, \"width\": 976, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-28-714980-v1/fig-003.webp\", \"caption\": \"Figure 3. Longevity-LLM captures age-dependent signal in proteomic data.\", \"page\": 8, \"index\": 3, \"width\": 976, \"height\": 644}]"
motivation: 传统的衰老时钟模型受限于固定模态和特征集，且缺乏足够的生物学解释能力。
method: 通过监督学习和强化学习，在多种生物组学数据上对Qwen3-14B基础模型进行微调。
result: 模型在表观遗传年龄预测中达到4.34年MAE，优于Horvath时钟，并在多项长寿基准测试中取得高分。
conclusion: 研究表明中等规模的基础模型能够跨模态匹配或取代专用衰老时钟，开启了衰老研究的新范式。
---

## 摘要
衰老时钟范式已经产生了数十种专业模型，这些模型几乎可以从任何生物数据类型中估算生理年龄或死亡率。然而，每种此类模型都在固定的模态内运行，依赖于预定义的特征集，且产生的生物学解释有限。在此，我们报告了 Longevity-LLM v0.1，这是一个基于 Qwen3-14B 的模型，通过监督学习和强化学习方案在 DNA 甲基化、蛋白质组学、临床生物标志物和 RNA 表达数据上进行了微调。Longevity-LLM 在最近公布的 Longevity Bench 中获得了很高的排名，包括癌症生存预测以及基于 RNA 或蛋白质组的年龄预测等任务。经过强化微调后，该模型在表观遗传年龄预测中实现了 4.34 年的平均绝对误差（MAE），超越了 Horvath 多组织时钟。除了年龄预测外，Longevity-LLM 还可以执行许多其他任务，包括蛋白质组图谱生成，其表现显著优于所有前沿大语言模型（LLMs）。这些结果表明，单个中等规模的 LLM 可以在不同数据模态下匹配或取代专门构建的衰老时钟。这项工作构成了我们“科学多模态人工智能健身房”（MMAI）初始冲刺阶段的中期报告，该计划致力于为药物研发和衰老研究构建基础模型。

## Abstract
The aging clock paradigm has yielded dozens of specialist models that can estimate chronological age or mortality from virtually any biodata type. Yet each such model operates within a fixed modality, relies on a predetermined feature set, and produces limited biological interpretation. Here, we report Longevity-LLM v0.1, a Qwen3-14B model fine-tuned through supervised and reinforcement learning regimes on DNA methylation, proteomics, clinical biomarker, and RNA expression data. Longevity-LLM achieves high ranks in the recently announced Longevity Bench, including such tasks as cancer survival and RNA- or proteome-based age prediction. After reinforcement fine-tuning, the model achieved a 4.34-year MAE in epigenetic age prediction, surpassing the Horvath multi-tissue clock. In addition to age prediction, Longevity-LLM can carry out numerous other tasks, including proteomic profile generation, for which it significantly outperforms all frontier LLMs. These results demonstrate that a single modestly sized LLM can match or replace purpose-built aging clocks across data modalities.

This work constitutes an interim report from the initial sprint of our Multi-Modal AI Gym for Science (MMAI), an initiative dedicated to building foundation models for drug discovery and aging research.

---

## 论文详细总结（自动生成）

### 论文总结：衰老时钟的终结——训练基础模型在衰老与长寿领域进行推理

#### 1. 核心问题与整体含义（研究动机和背景）
*   **核心问题**：传统的“衰老时钟”（Aging Clocks）虽然在预测生理年龄和死亡率方面表现出色，但存在三大局限：
    1.  **模态孤立**：每个模型仅限于单一数据类型（如仅 DNA 甲基化或仅临床指标），无法处理缺失数据或跨模态整合。
    2.  **解释性差**：模型通常是黑盒，无法解释“为什么”生物年龄高于生理年龄。
    3.  **工具碎片化**：现有的 AI 代理系统仅将 LLM 作为调度器，而非真正理解生物学逻辑。
*   **整体含义**：本研究提出了 **Longevity-LLM v0.1**，旨在通过“衰老时钟蒸馏”技术，将多种组学知识内化到单一的 14B 参数基础模型中，使其能够跨模态推理并替代专用工具，迈向“从提示词到药物”（Prompt-to-Drug）的全流程自动化。

#### 2. 论文提出的方法论
*   **核心思想**：不改变模型架构，将生物组学数据（数值、特征重要性、基因注释）转化为结构化的文本推理链（Reasoning Traces），通过两阶段微调使通用 LLM 具备处理复杂生物数据的能力。
*   **关键技术细节**：
    *   **监督微调 (SFT)**：在 76.6 万个样本（10.9 亿 Token）上进行全参数微调。任务涵盖年龄回归、死亡率分类、生存对比及蛋白质组生成。
    *   **强化微调 (RFT)**：基于 SFT 检查点，使用 **GRPO（组相对策略优化）** 算法。
    *   **奖励函数设计**：
        1.  **格式奖励**：确保模型正确使用 `<think>` 标签。
        2.  **思考长度奖励**：鼓励模型进行深度推理（最高 5000 字符）。
        3.  **回归准确性奖励**：根据预测值与真实值的绝对误差进行评分，并通过任务全量程进行归一化，使不同单位（年、月）的任务具有可比性。

#### 3. 实验设计
*   **数据集**：
    *   **DNA 甲基化 (DNAm)**：来自多个公开时钟的 CpG 位点数据。
    *   **临床生物标志物**：NHANES 数据集（死亡率、生存时间）。
    *   **转录组学 (RNA)**：GTEx 门户数据（组织年龄对比）。
    *   **蛋白质组学**：Olink Explore 3072 平台数据。
    *   **癌症生存**：TCGA 数据。
*   **Benchmark 与对比方法**：
    *   **Longevity Bench**：与 15 个前沿商用模型（如 Gemini 3 Pro, GPT 系列等）对比。
    *   **专用时钟对比**：在 DNAm 预测上对比 **Horvath 多组织时钟**；在蛋白质组上对比 **PAC** 和 **Proteoclock**。

#### 4. 资源与算力
*   **SFT 阶段**：使用 **24 张 NVIDIA B200 GPU**，训练约 3000 个优化步数，消耗约 45 亿 Token。
*   **RFT 阶段**：使用 **16 张 NVIDIA A100 80GB GPU**，训练 2000 个步数。
*   **开发周期**：该模型是“10 天开发冲刺”的产物。

#### 5. 实验数量与充分性
*   **实验规模**：涵盖了 38 个任务，跨越 4 大主要生物模态。
*   **充分性评价**：
    *   **客观性**：采用了严格的受试者级（Subject-level）划分，防止数据泄露。
    *   **对比维度**：不仅对比了通用 LLM，还挑战了该领域的“金标准”专用模型（Horvath Clock），实验设计较为严谨。
    *   **局限性**：蛋白质组学样本量（约 7800 个）相对较小，可能影响该模态下的泛化上限。

#### 6. 主要结论与发现
*   **超越专用模型**：经过 RFT 后，Longevity-LLM 在表观遗传年龄预测上的 MAE 达到 **4.34 年**，显著优于经典的 Horvath 时钟（4.61 年）。
*   **跨模态霸榜**：在 Longevity Bench 的 7 项任务中，该 14B 模型在 4 项中排名第一，尤其在癌症预后和死亡率预测上超过了参数量更大的前沿模型。
*   **生成能力**：模型能够根据年龄和性别生成生物学上合理的蛋白质组图谱，Jaccard 指数远超其他 LLM，证明其内化了蛋白质组动力学规律。

#### 7. 优点
*   **架构简洁性**：证明了无需修改 Transformer 架构或添加专用预测头，仅靠高质量数据工程即可处理复杂的组学数值任务。
*   **多功能性**：单一模型集成了预测、分类、推理和生成多种功能，打破了“一病一时钟”的碎片化局面。
*   **强化学习的应用**：成功将 RFT 引入生物数值回归任务，通过奖励机制显著提升了预测精度。

#### 8. 不足与局限
*   **数据依赖**：模型性能高度依赖于现有时钟系数的“蒸馏”，对于完全未知的生物信号发现能力尚待验证。
*   **推理深度**：虽然模型能生成推理链，但文中未详细展示其推理过程在生物学上的“洞察力”是否真正超越了统计相关性。
*   **模态不平衡**：蛋白质组学数据量远少于 DNA 甲基化，模型在不同模态间的知识迁移机制仍需进一步研究。
*   **初步报告**：作为 v0.1 版本和 10 天冲刺的产物，其长期稳定性和在临床决策中的可靠性仍需大规模验证。

（完）
