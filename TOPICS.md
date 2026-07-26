# Repo metadata worksheet (console actions)

Everything below is applied per repo via **Settings → General** (description /
website) and the **About gear → Topics** on the repo home page. Equivalent `gh`
commands at the bottom if you'd rather script it.

## prolly-core

**Description (About):**
> The prolly tree in Java — a content-addressed, history-independent B-tree with
> durable stores, pack sync, and a live write-path explorer. Independent port of
> Dolt's storage primitive.

**Topics:**
`prolly-tree` `merkle-tree` `content-addressable-storage` `version-control`
`git-for-data` `database` `storage-engine` `rocksdb` `dolt` `java`

## prolly-rdf

**Description (About):**
> Versioned SPARQL as a standard Eclipse RDF4J Sail — commits, branches, three-way
> merge, and time-travel reads on content-addressed prolly trees, with a
> worst-case-optimal triejoin.

**Website:** `https://prollygraph.github.io/prolly-rdf/` *(after the Pages toggle:
Settings → Pages → Source: "GitHub Actions")*

**Topics:**
`rdf` `sparql` `rdf4j` `triplestore` `graph-database` `knowledge-graph`
`semantic-web` `version-control` `prolly-tree` `java`

## prolly-json

**Description (About):**
> A versioned JSON document substrate on prolly trees — shared structure shares
> storage, diffs are O(changed). Development parked; embeddable substrate only.

**Topics:**
`json` `document-database` `document-store` `version-control` `prolly-tree`
`content-addressable-storage` `java`

## Org page

- **Pinned repositories** (org home → "Pinned" customize): `prolly-core`,
  `prolly-rdf`, `prolly-json` — in that order (engine first, the story reads
  downward).
- **Org profile → Website**: the Pages URL above once live.

## The `gh` equivalents (if authenticated)

```bash
gh repo edit prollygraph/prolly-core \
  --description "The prolly tree in Java — a content-addressed, history-independent B-tree with durable stores, pack sync, and a live write-path explorer. Independent port of Dolt's storage primitive." \
  --add-topic prolly-tree --add-topic merkle-tree --add-topic content-addressable-storage \
  --add-topic version-control --add-topic git-for-data --add-topic database \
  --add-topic storage-engine --add-topic rocksdb --add-topic dolt --add-topic java

gh repo edit prollygraph/prolly-rdf \
  --description "Versioned SPARQL as a standard Eclipse RDF4J Sail — commits, branches, three-way merge, and time-travel reads on content-addressed prolly trees, with a worst-case-optimal triejoin." \
  --homepage "https://prollygraph.github.io/prolly-rdf/" \
  --add-topic rdf --add-topic sparql --add-topic rdf4j --add-topic triplestore \
  --add-topic graph-database --add-topic knowledge-graph --add-topic semantic-web \
  --add-topic version-control --add-topic prolly-tree --add-topic java

gh repo edit prollygraph/prolly-json \
  --description "A versioned JSON document substrate on prolly trees — shared structure shares storage, diffs are O(changed). Development parked; embeddable substrate only." \
  --add-topic json --add-topic document-database --add-topic document-store \
  --add-topic version-control --add-topic prolly-tree \
  --add-topic content-addressable-storage --add-topic java

# Enable Pages (the item-1 gate) without the console:
gh api repos/prollygraph/prolly-rdf/pages -X POST -f build_type=workflow
```
