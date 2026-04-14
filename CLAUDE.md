# Claudevault — LLM Wiki Schema

This file governs how the LLM (Claude Code) operates on this Obsidian vault. Read it at the start of every session. It defines the directory structure, page conventions, and workflows for ingesting sources, answering queries, and maintaining the wiki.

---

## Directory Layout

```
Claudevault/
├── CLAUDE.md               ← this file (schema & instructions)
├── wiki/
│   ├── index.md            ← content catalog (update on every ingest)
│   ├── log.md              ← append-only operation log
│   ├── overview.md         ← high-level synthesis of the whole knowledge base
│   ├── sources/            ← one summary page per ingested source
│   ├── concepts/           ← topic and idea pages
│   ├── entities/           ← people, organizations, products, tools
│   └── analyses/           ← query answers, comparisons, tables filed back in
├── raw/
│   ├── sources/            ← immutable raw source files (markdown, txt, pdf)
│   └── assets/             ← downloaded images referenced by sources
└── templates/
    ├── source-summary.md
    ├── concept.md
    ├── entity.md
    └── analysis.md
```

**Rule:** Never modify files under `raw/`. They are the source of truth. The LLM only writes to `wiki/`.

---

## Page Conventions

### Frontmatter
Every wiki page must have YAML frontmatter:

```yaml
---
title: "Page Title"
type: source | concept | entity | analysis | overview
tags: [tag1, tag2]
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [source-slug, ...]   # which raw sources informed this page
---
```

### Internal Links
Use Obsidian wikilink syntax: `[[Page Title]]`. Always link on first mention of any entity, concept, or source that has (or should have) its own page. This populates the graph view.

### Cross-References Section
Every page ends with a `## See Also` section listing related pages as wikilinks with a one-line note on the relationship.

### Confidence Markers
Use inline markers for uncertain claims:
- `[low confidence]` — speculation or single-source claim
- `[contradicted by [[Page]]]` — another page disputes this

---

## Workflows

### 1. Ingest a New Source

**Trigger:** User says "ingest [source]" or drops a file in `raw/sources/` and asks you to process it.

**Steps:**
1. Read the source file (or URL content).
2. Discuss key takeaways with the user — ask what to emphasize.
3. Create `wiki/sources/<slug>.md` using the source-summary template.
4. Identify all entities and concepts mentioned. For each:
   - If the page exists → update it with new information, noting the new source.
   - If it doesn't exist → create it from the appropriate template.
5. Update `wiki/overview.md` if the source shifts the big picture.
6. Update `wiki/index.md` — add the new source page and any new concept/entity pages.
7. Append an entry to `wiki/log.md`:
   ```
   ## [YYYY-MM-DD] ingest | Source Title
   - Summary page: [[sources/slug]]
   - Pages created: [[concepts/x]], [[entities/y]]
   - Pages updated: [[concepts/a]], [[entities/b]]
   - Key takeaway: one sentence.
   ```

**Aim:** a single ingest should touch 5–15 wiki pages.

### 2. Answer a Query

**Trigger:** User asks a question.

**Steps:**
1. Read `wiki/index.md` to find relevant pages.
2. Read those pages.
3. Synthesize an answer with citations as `[[wikilinks]]`.
4. **Decide:** is this answer valuable enough to file back into the wiki?
   - If yes → save it as `wiki/analyses/<slug>.md` using the analysis template, add it to the index, and log it.
   - If no → answer in chat only.

### 3. Lint the Wiki

**Trigger:** User says "lint" or "health check".

**Steps:**
1. Scan all pages for: orphans (no inbound links), contradictions, stale claims, missing cross-references, concepts mentioned but lacking a page.
2. Produce a report listing issues by severity.
3. Ask the user which issues to fix.
4. Fix approved issues and log the lint pass:
   ```
   ## [YYYY-MM-DD] lint
   - Issues found: N
   - Issues fixed: M
   - Outstanding: list
   ```

### 4. Session Start

At the start of every session:
1. Read `CLAUDE.md` (this file).
2. Read `wiki/log.md` — last 10 entries — to understand recent activity.
3. Read `wiki/index.md` to know what's in the wiki.
4. Then proceed with the user's request.

---

## Naming Conventions

| Type | Slug format | Example |
|------|-------------|---------|
| Source summary | `sources/author-short-title` | `sources/karpathy-llm-wiki-pattern` |
| Concept | `concepts/kebab-case-name` | `concepts/retrieval-augmented-generation` |
| Entity (person) | `entities/firstname-lastname` | `entities/andrej-karpathy` |
| Entity (tool/org) | `entities/kebab-name` | `entities/obsidian` |
| Analysis | `analyses/YYYY-MM-DD-short-desc` | `analyses/2026-04-14-rag-vs-wiki` |

File names use the slug (no directory prefix in the filename itself).

---

## Index Format

`wiki/index.md` is organized into sections by type. Each entry:
```
- [[Page Title]] — one-line description (N sources)
```

## Log Format

`wiki/log.md` is append-only. New entries go at the **top** (most recent first). Each entry header must start with `## [YYYY-MM-DD]` so it can be grepped:
```bash
grep "^## \[" wiki/log.md | head -10
```

---

## Style Guidelines

- Write wiki pages in **third person**, neutral tone — as if writing for a reader who will consult this later.
- Summaries should be **dense and opinionated** — extract the thesis, not just facts.
- Flag contradictions explicitly rather than silently overwriting.
- Prefer short pages with good links over long monolithic pages.
- The overview should always reflect the current synthesis — revise it aggressively.

---

## This Wiki's Domain

*[To be filled in as the knowledge base develops. Describe what this wiki is for, its central topic, and any domain-specific conventions.]*

---

*Schema version: 1.0 | Created: 2026-04-14*
