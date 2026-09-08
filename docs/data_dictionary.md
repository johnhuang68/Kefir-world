# Data Dictionary

This document defines the core fields used in `data/fermented_milk.csv` and the evidence standard for Kefir World.

## Core fields

- `name`: Primary English product/culture name.
- `alternate_names`: Common alternate spellings or regional names.
- `region_or_origin`: Geographic association. This does not always imply a single proven point of origin.
- `temp_min_c`: Lower bound of the selected source-backed fermentation description in °C; see `fermentation_scope`.
- `temp_max_c`: Upper bound of that description. Equal bounds can encode an approximate published process point, not exact biological limits.
- `typical_time_h`: Human-readable fermentation duration in hours where numerical, or qualified descriptions such as `overnight`, `varies` or `not established`. This is not a numeric-only column; preserve process-specific labels.
- `starter_ecology`: Broad starter system such as grain consortium, mesophilic starter, thermophilic starter, natural mixed culture, or LAB–yeast mixed culture.
- `main_microbes_or_features`: Representative organisms or microbiological/texture features. This is not intended to imply an exhaustive species list.
- `propagation_type`: Typical continuation method such as grains, backslopping, or defined commercial starter.
- `notes`: Important technical context.
- `evidence_status`: Current confidence/verification state.
- `profile_path`: Repository-relative Markdown profile path; blank when no link was attached in this review.
- `reference_ids`: Semicolon-separated foreign keys into `data/references.csv`; sources attached to the whole profile, not a claim that each supports every cell.
- `fermentation_scope`: Mandatory interpretation for reviewed numerical process fields: source type, paired temperature/time conditions, approximate points and excluded contexts.

The first eleven columns are preserved from the original catalog. The final three are appended; consumers that assume a fixed column count must use the updated header. Blank traceability fields in unreviewed rows mean not yet attached, not absence of literature.

## Evidence levels

Recommended future statuses:

1. `primary-source verified` — supported by peer-reviewed primary research with directly relevant fermentation conditions or microbial analysis.
2. `review verified` — supported by a high-quality review.
3. `authoritative reference` — supported by FAO, Codex, government, university, or recognized technical standards.
4. `traditional-source supported` — credible documentation exists but the product varies strongly by locality or household practice.
5. `working draft` — plausible structured entry awaiting formal source attachment.

All 46 rows reviewed through 2026-09-08 use `literature-backed; claim-specific scope`: a composite status with citations and explicit limitations, not a claim that every field is primary-source verified. Source quality is assessed per claim in the linked profile. An authoritative standard can establish a definition without supporting a historical origin or a strain's phenotype.

## Reference registry

`data/references.csv` retains its original seven columns:

- `reference_id`: Unique stable identifier. Existing `MK` IDs are preserved; new product prefixes and shared `GEN` IDs are used. A shared source has one ID across profiles.
- `topic`: Product/topic slug; semicolons separate multiple linked topics.
- `title`: Traceable publication or institutional-document title.
- `year`: Issue/publication year; blank when undated. A standard's original year is retained with amendment scope in its title. Online-first versus issue-year differences are explained in profile bibliographies.
- `source`: Journal, publisher or issuing institution.
- `url`: DOI, PubMed/PMC, publisher or institutional URL. A DOI not indexed by Crossref may still be valid, for example a J-STAGE/JaLC record.
- `evidence_use`: Claim scope, study type and material access/interpretation limits.

Full author citations, useful sections/tables and alternative full-text links are in each profile. An abstract-only source supports only information actually present in the abstract or inspected excerpts. Publication years are not inferred from the date a web page was crawled.

## Manufacturer process observations

`data/manufacturer_processes.csv` stores instructions for a named commercial starter separately from the core product catalog. One source may have multiple records when activation, routine fermentation, cold fermentation, reculturing or post-fermentation drainage have different conditions.

- `observation_id`: Unique stable observation ID.
- `product`: Product label used for linking and human review; candidate products may appear here before they qualify for the core catalog.
- `source_id`: Foreign key into `data/references.csv`.
- `starter_form`: Form and state of the inoculum, such as fresh grains, freeze-dried grains or previous-batch culture.
- `stage`: Process stage described by this record.
- `milk_or_substrate`: Milk, cream or mixture explicitly stated by the source.
- `batch_volume_ml`: Stated working volume in millilitres; blank when not specified.
- `inoculum`: Source wording or normalized quantity without inferring viable-cell count.
- `temp_min_c`, `temp_max_c`: Numeric bounds only when the page supplies them. A single set point is repeated in both fields.
- `temperature_qualifier`: Context such as `room temperature`, `ideal range` or `refrigerator set point`.
- `time_min_h`, `time_max_h`: Stated numerical time bounds in hours; blank when the stage is not separately quantified.
- `time_qualifier`: Endpoint, first-batch exception or total revival period that controls interpretation.
- `endpoint_aftercare_and_scope`: Observable endpoint, chilling/draining step and evidence limitation.

These observations do not change `temp_min_c`, `temp_max_c` or `typical_time_h` in the core catalog unless independent product-level evidence supports that change. A supplier's product name does not establish organism identity, strain provenance, traditionality, indefinite backslopping stability or a health effect.

## Important interpretation rules

### Temperature

A product should not be assigned a single exact temperature unless the source actually specifies one. Prefer a representative practical range, and preserve source-specific ranges when lineages differ.

Do not interpret a pair of minimum/maximum fields as a tested continuous operating envelope. For example, Dahi's 22 °C / 12–14 h and 37 °C / 5–8 h are separate process examples. Långfil's approximate 18 °C point has no verified duration in this review. Missing time is not zero hours. Laboratory growth, EPS extraction and industrial bioconversion conditions must not be substituted for milk fermentation.

### Microbial ecology

Traditional fermented milks are dynamic microbial communities. Avoid presenting one isolate reported in one study as the universal composition of the entire product category.

Distinguish cultured viable isolates, marker-gene detections, relative sequence abundance and genome-resolved identification. Negative or missing fungal evidence is not proof that every batch is fungus-free. Organisms found in pooled studies of several products must not be reassigned to one product without sample-level support.

### Taxonomic names and identifiers

Keep the name used by the original paper alongside current nomenclature where useful. For example, historical *Lactococcus lactis* subsp. *cremoris* is a synonym of *Lactococcus cremoris* in [LPSN (GEN002)](https://lpsn.dsmz.de/species/lactococcus-cremoris), accessed 2026-09-06. A nomenclatural update does not reidentify an old phenotypically classified isolate.

Record these separately:

| Identification level | Example | Meaning |
|---|---|---|
| Species/subspecies | *L. delbrueckii* subsp. *bulgaricus* | A taxon, not a unique strain |
| Published isolate/strain code | FC; LAPT 3001 | A publication-specific identifier; a collection deposit is not assumed |
| Sequence accession | CP000156 | A sequence record, not an additional strain |
| Mixture/batch label | Matsoni B.1 | A combination of organisms, not one isolate |
| Chemical fraction | Filmjölk CNP1/CNP2 | Purified material, not a bacterium |

Do not invent IDs, substitute a comparator for a product isolate, or silently merge similar spellings. Later reidentification must be explicit: Matsoni st265 was reported as *S. thermophilus* in MAT004 and reidentified as *E. faecium* in MAT005. The profile retains the history rather than presenting the earlier identification as current.

### EPS, acidification and storage

Separate observed ropiness, measured EPS yield, polymer chemistry and gene-cluster potential. Cell-wall polysaccharides are not automatically secreted milk thickeners. Do not use kefiran as a generic name for microbial EPS.

pH observations, pH change per unit time, titratable acidity and measured organic-acid concentrations are different variables. A table headed “acidification rate” that gives only pH at 3 h and 6 h is retained as endpoint observations.

Storage records must preserve milk, starter, package, temperature, duration and outcome. Sensory shelf life, viable-cell survival and revival as an inoculum are not interchangeable. Manufacturer instructions are labelled with product and access date; they do not establish universal performance of household lineages.

### Origin

Many fermented milks have long cross-border histories. Prefer terms such as `associated with`, `traditional in`, or a regional designation when a single-country origin cannot be demonstrated.

### Yogurt vs fermented milk

Not every item in this repository is yogurt in the strict Codex sense. Kefir, viili, kumis, dadih, amasi and many others are better categorized under the broader term `fermented milk`.

### Derived products

Greek yogurt and labneh are strongly defined by post-fermentation concentration/straining. They should not automatically be treated as unique starter ecosystems.
