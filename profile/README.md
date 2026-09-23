# prollygraph

**Git semantics for structured data, on the JVM.** A [prolly tree](https://github.com/prollygraph/prolly-core/blob/main/docs/foundations/the-prolly-tree.md)
is a B-tree whose shape is a pure function of its content — every node stored under
the hash of its own bytes — which buys commits, branches, three-way merge, O(changed)
diff, and time-travel reads as *structural properties*, not bolted-on features. These
repos are that idea as working software: an engine, and data models built on it.

| Ring | What it is |
|---|---|
| [**prolly-core**](https://github.com/prollygraph/prolly-core) | The engine: the prolly tree (a faithful Java port of [Dolt](https://github.com/dolthub/dolt)'s, independently maintained), durable RocksDB/file stores, pack-based sync, the many-repos primitive — with a **live write-path explorer** you can run to *watch* a write mint exactly its spine |
| [**prolly-rdf**](https://github.com/prollygraph/prolly-rdf) | Versioned SPARQL: a standard Eclipse RDF4J Sail with git-like history, a worst-case-optimal triejoin, W3C conformance run in every build, and 13 CI-locked runnable demos |
| [**prolly-json**](https://github.com/prollygraph/prolly-json) | A versioned JSON document substrate — documents shredded into content-addressed rows so shared structure shares storage (development currently parked; the repo is the embeddable substrate) |

**Start here:** the [two-minute landing page](https://github.com/prollygraph/prolly-rdf/blob/main/landing-page/index.html)
(benefits *and* honest limits, with a time-travel demo built from a real run) · the
[embedded quickstart](https://github.com/prollygraph/prolly-rdf/blob/main/prolly-rdf4j/docs/getting-started.md)
(a versioned Sail in ~20 lines) · the
[docs](https://github.com/prollygraph/prolly-rdf/blob/main/docs/README.md)
(foundations + anatomy walkthroughs, bugs left in).

**Evaluate it:** the
[on-disk format specification](https://github.com/prollygraph/prolly-core/blob/main/docs/spec/on-disk-format.md)
and [sync protocol specification](https://github.com/prollygraph/prolly-core/blob/main/docs/spec/sync-protocol.md)
(normative — every constant cited to the defining code, each with a
verification map) · the
[SPARQL 1.1 conformance report](https://github.com/prollygraph/prolly-rdf/blob/main/CONFORMANCE.md)
(174/176 query, 90/90 update, the two failures named and classified, with
reproduction steps and the build-enforced ratchet).

## Maintainers

Maintained by **Manny Rivera** under **Earasoft**. Contact routes are GitHub-native:
issues on the relevant repo for bugs and questions, and each repo's `SECURITY.md`
private-advisory channel for vulnerability or conduct reports — one family, one
process. Per-repo `MAINTAINERS.md` files carry the same information beside the code.

Everything is Apache-2.0, pre-1.0 (each repository's `pom.xml` names its version; formats evolve freely), and written
in a calibrated-honesty register: numbers are dated and traceable, limits are stated
next to benefits, and retractions stay visible. Vulnerability reports: any repo's
`SECURITY.md` — one family, one private channel. Not affiliated with DoltHub, Inc.
