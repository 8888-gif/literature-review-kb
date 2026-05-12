# Literature Review KB Workflow

## 1. Clarify

Collect only the details needed to search and rank well:

- Topic, core keywords, and any exclusions.
- Mode: general, resin/polymer + ML, AI frontier, or cross-domain inspiration.
- Source mode: open sources or specified databases.
- Output location for the Markdown knowledge base.
- For resin/polymer + ML: resin system, target property, descriptor preference, validation requirement, and whether wet-lab evidence is required.

If the user does not specify an output location, create a topic-named Markdown folder in the current workspace or the user-provided knowledge-base root.

## 2. Search

Use source mode to guide discovery:

- Open scholarly sources: Semantic Scholar, Crossref, arXiv, PubMed where relevant, publisher pages, and institution/lab pages.
- AI frontier additions: OpenReview for ICLR/NeurIPS/ICML-style work, Hugging Face Papers for code-active papers, and AI4S/DeepMind/materials-intelligence lab pages.
- Specified databases: follow the user's requested databases and record access limits.

Prefer primary metadata pages and papers with DOI, abstract, keywords, venue, and author/year data. Deduplicate preprint and published versions; keep the stronger canonical version unless the preprint has essential open metadata.

## 3. Screen and Rank

Build a candidate pool larger than 10 when possible. Score with `ranking_rubric.md`, then select the 10 highest-value papers with enough topical coverage. For resin/polymer + ML, include domain-specific evidence in the ranking reason.

Each ranked item must include:

- Rank.
- Title.
- Authors/year.
- Venue.
- CAS journal quartile (中科院分区), including year/source when available.
- Impact factor, including JCR year/source when available.
- DOI/URL.
- Abstract.
- Keywords.
- Scores or concise score rationale.
- Reason for inclusion.
- Metadata gaps marked as `unavailable`.

## 4. Build the Knowledge Base

Create a Markdown index from `index_template.md` with the ranked 10-paper table. Then create detailed notes from `top3_note_template.md` only for ranks 1-3.

Top 3 notes must distinguish:

- Paper facts.
- Domain interpretation.
- AI frontier inspiration.
- Surrogate Modeling analogy.
- Transferable research idea.

## 5. Quality Checks

Before finalizing:

- Confirm there are 10 ranked papers or explain why fewer valid papers exist.
- Confirm only top 3 papers have deep notes.
- Confirm journal quartiles and impact factors are verified or marked `unavailable`.
- Confirm all generated claims are grounded in available metadata or clearly labeled as interpretation.
- Confirm unavailable fields are marked instead of invented.
