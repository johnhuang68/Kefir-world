# Data Dictionary

This document defines the core fields used in `data/fermented_milk.csv` and the evidence standard for Kefir World.

## Core fields

- `name`: Primary English product/culture name.
- `alternate_names`: Common alternate spellings or regional names.
- `region_or_origin`: Geographic association. This does not always imply a single proven point of origin.
- `temp_min_c`: Lower bound of the practical fermentation range in °C.
- `temp_max_c`: Upper bound of the practical fermentation range in °C.
- `typical_time_h`: Common fermentation-time range. Traditional products may vary substantially.
- `starter_ecology`: Broad starter system such as grain consortium, mesophilic starter, thermophilic starter, natural mixed culture, or LAB–yeast mixed culture.
- `main_microbes_or_features`: Representative organisms or microbiological/texture features. This is not intended to imply an exhaustive species list.
- `propagation_type`: Typical continuation method such as grains, backslopping, or defined commercial starter.
- `notes`: Important technical context.
- `evidence_status`: Current confidence/verification state.

## Evidence levels

Recommended future statuses:

1. `primary-source verified` — supported by peer-reviewed primary research with directly relevant fermentation conditions or microbial analysis.
2. `review verified` — supported by a high-quality review.
3. `authoritative reference` — supported by FAO, Codex, government, university, or recognized technical standards.
4. `traditional-source supported` — credible documentation exists but the product varies strongly by locality or household practice.
5. `working draft` — plausible structured entry awaiting formal source attachment.

## Important interpretation rules

### Temperature

A product should not be assigned a single exact temperature unless the source actually specifies one. Prefer a representative practical range, and preserve source-specific ranges when lineages differ.

### Microbial ecology

Traditional fermented milks are dynamic microbial communities. Avoid presenting one isolate reported in one study as the universal composition of the entire product category.

### Origin

Many fermented milks have long cross-border histories. Prefer terms such as `associated with`, `traditional in`, or a regional designation when a single-country origin cannot be demonstrated.

### Yogurt vs fermented milk

Not every item in this repository is yogurt in the strict Codex sense. Kefir, viili, kumis, dadih, amasi and many others are better categorized under the broader term `fermented milk`.

### Derived products

Greek yogurt and labneh are strongly defined by post-fermentation concentration/straining. They should not automatically be treated as unique starter ecosystems.
