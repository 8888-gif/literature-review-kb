---
name: literature-review-kb
description: Search, rank, and organize academic literature into a Markdown knowledge base. Use when Codex needs to find 10 papers, score and rank them, extract titles/abstracts/keywords, and create detailed notes for the top 3; supports general literature review, resin/polymer + machine learning, AI frontier tracking, and cross-domain inspiration workflows. This skill does not draft manuscript prose unless separately requested.
---

# Literature Review KB

## Overview

Use this skill to build a ranked literature knowledge base rather than write paper text. Produce a 10-paper ranked overview and deep Markdown notes for only the top 3 papers.

## Workflow

1. Clarify the task before searching:
   - Research topic and required language.
   - Mode: general literature review, resin/polymer + ML, AI frontier tracking, or cross-domain inspiration.
   - Literature source mode: open sources or user-specified databases.
   - For resin/polymer + ML: default to low dielectric loss materials and thermal conductive materials unless the user specifies another property; ask whether to prioritize a resin system, target property, validation type, or descriptor family.
2. Choose sources:
   - Open sources: Semantic Scholar, Crossref, arXiv, publisher pages, OpenReview, Hugging Face Papers, and public AI4S lab pages when relevant.
   - Specified databases: use the user's requested database names and access constraints.
3. Search, verify, and deduplicate papers. Prefer primary sources and metadata pages over secondary summaries.
4. Rank exactly 10 papers when enough valid candidates exist. If fewer are available, state the reason and rank all valid candidates.
5. Extract for all ranked papers: title, authors/year, venue, CAS journal quartile, impact factor, DOI/URL, abstract, keywords, ranking score, and ranking reason. Mark unavailable fields as `unavailable`; do not invent metadata.
6. Create or update a Markdown index for all 10 papers and detailed Markdown notes only for the top 3.
7. For every top 3 note, include AI frontier inspiration, Surrogate Modeling analogy, and transferable research ideas.

## Mode Guidance

- **General literature review**: use standard relevance, impact, recency, and methodological coverage scoring.
- **Resin/polymer + ML**: load `references/polymer_descriptors.json` and emphasize low dielectric loss resins, thermal conductive resins, data integrity, descriptors, interpretability, experimental validation, and materials databases.
- **AI frontier tracking**: emphasize very recent work, OpenReview discussions, code availability, Hugging Face activity, and frontier model or agent relevance.
- **Cross-domain inspiration**: combine resin/polymer + ML extraction with AI frontier analogies, especially LLM agents, multimodal models, automated molecular or formulation design, Bayesian optimization, and closed-loop wet-lab workflows.

## References

- Load `references/literature_workflow.md` for the full search, scoring, ranking, and Markdown output procedure.
- Load `references/ranking_rubric.md` before scoring papers.
- Load `references/index_template.md` when creating the 10-paper overview.
- Load `references/top3_note_template.md` when creating deep notes.
- Load `references/polymer_descriptors.json` for resin/polymer + ML or cross-domain inspiration mode.

## Output Rules

- Keep outputs evidence-grounded and citation-aware.
- Separate verified paper facts from Codex-generated interpretation.
- For journal papers, include Chinese Academy of Sciences journal quartile (中科院分区) and impact factor when verifiable. State the year/source of the quartile and impact factor when available; otherwise write `unavailable`.
- Do not fabricate abstracts, keywords, metrics, DOI, citation counts, journal quartiles, impact factors, datasets, code links, or experimental validation.
- Do not create related-work paragraphs or manuscript sections unless the user separately requests writing.
