# Counting candidate terpene and terpenoid identities in Terpedia

**Study status:** source-audited aggregate result; full molecule-level execution is not bundled.

## Abstract

A chemical diversity census depends on the definition of “terpene,” the source universe, and the structure identity rule. The upstream census reports 199,234 distinct identities from a COCONUT terpenoid source set and 145,354 from a source-classified TeroKit set, with 75,664 shared identities. Their union is 268,924 candidate identities. The result is a two-source, source-declared candidate census, not a validated count of natural terpene hydrocarbons or a complete Terpedia-wide total.

## Methods and provenance

The upstream analysis deduplicated the two source sets by typed standard InChI, falling back to InChIKey and then structure representation where necessary. The reported execution used standard InChI for all 344,588 source-set memberships. The set relation is `199,234 + 145,354 − 75,664 = 268,924`. The frozen report is in `data/reports/coconut-terokit-union-20260903.json`; source flow is in `data/reports/source-flow-20260904.json`.

## Results and interpretation

The 268,924 total is a union of source-labeled candidates. A source classification or resolved structure identity does not establish chemical class, natural occurrence, independent characterization, or biosynthesis. The result does not include all Terpedia BigQuery/RDF sources. The upstream project separately documents identity-policy sensitivity, ChEBI ontology checks, and reaction evidence; those must not be silently collapsed into this union.

## Reproducibility status

The included notebook validates the arithmetic and displays report caveats. It does not rerun molecular standardization or the BigQuery query. Full reproduction requires the upstream source tables and scripts in `census/`, plus access to the stated cloud data.

## Source

Terpedia `census` project, `paper.md`, `README.md`, and dated reports. The current paper is a working research artifact, not a peer-reviewed estimate.
