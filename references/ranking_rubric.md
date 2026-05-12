# Ranking Rubric

Score papers on a 100-point scale. Adapt weights by mode, but preserve transparent ranking reasons.

## General Literature Review

- Topic relevance: 30
- Venue and publication quality: 20
- Citation or field influence: 15
- Recency and timeliness: 15
- Methodological representativeness: 10
- Metadata completeness: 10

Venue and publication quality should consider verified Chinese Academy of Sciences journal quartile (中科院分区), impact factor, journal/conference reputation, and peer-review status. If quartile or impact factor cannot be verified, do not guess; mark it `unavailable` and rely on other venue evidence.

## Resin/Polymer + ML

- Topic relevance to resin/polymer + ML: 20
- Data integrity and scale: 20
- Descriptor and feature engineering clarity: 15
- Model quality and validation rigor: 15
- Interpretability and physical meaning: 10
- Experimental or wet-lab validation: 10
- Venue/citation impact: 5
- Digital infrastructure and reproducibility: 5

Domain-specific ranking signals:

- Structured resin formulation, curing condition, processing, or property data.
- Clear descriptor representation: SMILES, molecular fingerprints, graph representation, physicochemical descriptors, sequence/polymer descriptors, or processing descriptors.
- Interpretable ML: SHAP, feature importance, ablation, sensitivity analysis, uncertainty quantification, or physically meaningful factors.
- Validation beyond internal cross-validation: external test set, experimental validation, prospective validation, or closed-loop optimization.
- Public data, code, supplementary tables, PolyInfo, Materials Project, Citrination, Materials Cloud, or other materials database usage.
- Verified CAS journal quartile and impact factor for journal papers, especially when comparing papers with similar technical relevance.

## AI Frontier Tracking

- Frontier relevance: 25
- Novel method or capability: 20
- Evidence quality: 15
- OpenReview/community signal or peer-review status: 10
- Code/model availability: 10
- Recency: 10
- Cross-domain transfer potential: 10

For conference-first AI papers, CAS quartile and impact factor may be not applicable. Use `not applicable` for non-journal venues instead of forcing journal metrics.

## Cross-Domain Inspiration

- Materials-domain relevance: 25
- AI frontier relevance: 20
- Transferability to formulation/design loops: 20
- Data and validation strength: 15
- Interpretability and mechanistic usefulness: 10
- Reproducibility: 10
