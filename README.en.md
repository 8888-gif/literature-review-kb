# Literature Review KB

`literature-review-kb` is a Codex skill for academic literature discovery, ranking, and Markdown knowledge-base organization.

It focuses on finding and ranking 10 papers, then creating detailed notes for the top 3. It does not draft manuscript prose unless explicitly requested.

Chinese README: [README.md](README.md).

## What It Does

- Searches and ranks academic literature for a user-provided topic.
- Supports general literature review, resin/polymer + machine learning, AI frontier tracking, and cross-domain inspiration modes.
- Produces a ranked 10-paper Markdown index.
- Produces detailed Markdown notes for the top 3 papers only.
- Extracts title, authors, venue, DOI/URL, abstract, keywords, score, and ranking rationale.
- Reports CAS journal quartile and impact factor for journal papers when verifiable, with metric year/source when available.
- Marks missing metadata as `unavailable` instead of inventing it.

## Specialized Focus

For resin/polymer + ML topics, the skill defaults to two target directions: low dielectric loss materials and thermal conductive materials. It emphasizes:

- Resin systems, curing agents, fillers, and processing conditions.
- Low dielectric loss metrics such as dielectric loss tangent, dielectric constant, frequency, temperature/humidity conditions, breakdown strength, and insulation reliability.
- Thermal conductivity metrics such as through-plane/in-plane conductivity, filler type/loading, interfacial thermal resistance, conductive networks, anisotropy, and thermal stability.
- Descriptor types such as SMILES, fingerprints, GNN topology, physicochemical descriptors, and process descriptors.
- ML workflows such as active learning, Bayesian optimization, surrogate modeling, GNNs, and LLM-agent loops.
- Experimental validation, wet-lab evidence, external tests, and reproducibility.

For AI frontier topics, the skill can consider sources such as OpenReview, Hugging Face Papers, arXiv, Semantic Scholar, Crossref, and public AI4S lab pages.

## Skill Layout

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

## Example Prompt

```text
Use $literature-review-kb to find 10 high-impact papers on epoxy resin Tg prediction with machine learning, rank them, and create deep Markdown notes for the top 3.
```

## Validation

Validate the skill with:

```powershell
python D:\AI\.codex\skills\.system\skill-creator\scripts\quick_validate.py D:\AI\.codex\skills\literature-review-kb
```
