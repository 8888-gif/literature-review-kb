# Literature Review KB

`literature-review-kb` 是一个 Codex 技能，用于学术文献检索、排名筛选和 Markdown 知识库整理。

它的核心目标是围绕用户提供的研究主题检索并排名 10 篇文献，然后只对排名前 3 的文献生成深度笔记。除非用户明确要求，否则该技能不负责撰写论文正文、综述段落或 manuscript prose。

英文版说明见 [README.en.md](README.en.md)。

## 功能概览

- 根据用户提供的主题检索和筛选学术文献。
- 支持通用文献综述、树脂高分子 + 机器学习、AI 前沿追踪、跨领域启发四种模式。
- 生成 10 篇文献的 Markdown 排名索引。
- 只为排名前 3 的文献生成深度 Markdown 笔记。
- 提取题目、作者、年份、期刊/会议、DOI/URL、摘要、关键词、评分和排名理由。
- 对期刊论文标出中科院分区和影响因子，并尽量注明指标年份或来源。
- 对缺失信息标记为 `unavailable`，不编造摘要、关键词、DOI、引用量、中科院分区、影响因子、数据集或实验验证信息。

## 专业方向

### 树脂高分子 + 机器学习

当主题涉及树脂、高分子材料和机器学习时，技能会重点关注：

- 树脂体系、固化剂、填料和加工/固化条件。
- 目标性能，如 `T_g`、模量、拉伸强度、介电常数、热稳定性等。
- 描述符类型，如 SMILES、分子指纹、GNN 拓扑表示、物理化学描述符和工艺描述符。
- 机器学习流程，如主动学习、贝叶斯优化、代理模型、图神经网络和 LLM-agent 闭环。
- 实验验证、wet-lab validation、外部测试集和可复现性。

### AI 前沿追踪

当主题涉及 AI 前沿时，技能会考虑以下开放来源：

- OpenReview。
- Hugging Face Papers。
- arXiv。
- Semantic Scholar。
- Crossref。
- DeepMind、AI4S、材料智能相关实验室公开论文页。

### 跨领域启发

对排名前 3 的文献，技能会强制生成：

- AI 前沿启发。
- Surrogate Modeling 代理模型类比。
- 可迁移科研思路。

这些内容会明确作为 Codex 的解释和启发，不会伪装成原论文事实。

## 技能结构

```text
literature-review-kb/
|-- SKILL.md
|-- README.md
|-- README.en.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- index_template.md
    |-- literature_workflow.md
    |-- polymer_descriptors.json
    |-- ranking_rubric.md
    `-- top3_note_template.md
```

## 使用示例

```text
使用 $literature-review-kb 查找 10 篇关于环氧树脂 Tg 预测与机器学习的高影响力文献，进行排名，并为前三篇生成深度 Markdown 笔记。
```

英文示例：

```text
Use $literature-review-kb to find 10 high-impact papers on epoxy resin Tg prediction with machine learning, rank them, and create deep Markdown notes for the top 3.
```

## 输出形式

默认输出为 Markdown 知识库：

- 一个 10 篇文献的排名总览索引。
- 三篇 Top 3 深度文献笔记。
- 每篇 Top 3 笔记包含文献事实、材料科学字段、AI 前沿启发、代理模型类比和可迁移科研想法。

## 校验

可以使用以下命令校验技能结构：

```powershell
python D:\AI\.codex\skills\.system\skill-creator\scripts\quick_validate.py D:\AI\.codex\skills\literature-review-kb
```
