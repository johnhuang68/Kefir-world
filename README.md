# Kefir World

Kefir World is a research-oriented knowledge base for fermented milk cultures from around the world, including milk kefir, mesophilic cultured milks, thermophilic yogurts, traditional regional fermented milks, and mixed LAB–yeast fermentations.

## Goals

- Build a structured catalog of global fermented milk products and starter cultures.
- Compare fermentation temperature, time, microbial ecology, texture, acidity, aroma, and propagation behavior.
- Distinguish grain-based cultures, backslopping cultures, mesophilic starters, thermophilic starters, and mixed LAB–yeast systems.
- Keep temperature ranges and microbiological claims traceable to reliable references.
- Create data that can later power charts, posters, maps, and an interactive website.

## Initial temperature classes

- Mesophilic / room-temperature: roughly 15–30 °C
- Intermediate: roughly 25–37 °C
- Thermophilic / heated incubation: roughly 37–45 °C

These are practical grouping ranges, not strict taxonomic definitions. Individual products and strains can overlap.

## Included examples

The catalog contains the original 34 rows plus twelve source-backed additions: **Ititu, Mursik, Ayran, Doogh, Labneh Ambaris, Tarag, Ryazhenka, Varenets, Katyk, Khoormog, Pendidam, and Kindirmou**. Industrial Laban and Zabadi retain separate data rows but share profiles with their traditional counterparts so that the process comparison remains visible in one place.

## Repository structure

- `data/fermented_milk.csv` — core catalog
- `data/references.csv` — shared reference registry
- `profiles/` — detailed product profiles with claim-level citations
- `docs/data_dictionary.md` — field definitions and evidence rules
- `research/roadmap.md` — research backlog and validation plan

## Detailed profiles

All catalog rows now link to a detailed profile covering identity and history, traditional versus modern production, milk, source-paired temperature/time, sensory properties, microbial ecology, published isolate designations, EPS, acidification, propagation, storage and evidence gaps. The 44 files cover:

- Nordic and European cultures: Milk Kefir, Viili, Långfil, Filmjölk, Piimä, Tettmelk, Skyr, Ryazhenka and Varenets.
- Asian and Caucasus traditions: Caspian Sea Yogurt, Dadih, Tarag, Khoormog, Katyk, Chal/Shubat, Kumis/Airag, Matsoni, Dahi and Mishti Doi.
- African traditions: Ergo, Ititu, Dhanaan, Nunu, Mabisi, Amasi, Suusac, Mursik, Kindirmou, Pendidam, Lben and Rayeb.
- Middle Eastern products: Laban, Zabadi, Ayran, Doogh, Labneh and the distinct long-process Labneh Ambaris.
- Defined or concentrated cultured milks: Traditional Yogurt, Greek Yogurt, Bulgarian Yogurt, Acidophilus Milk, Bifidus Milk, AB Yogurt and ABT Yogurt.

A missing strain ID, process temperature or storage duration remains explicitly unknown. Shared profiles for traditional/industrial Laban and Zabadi keep their paired processes separate.

## Evidence policy

Temperature, microorganism, origin, and fermentation-time fields should be treated as reference-backed data. Traditional products often vary by household, region, milk type, and starter lineage. Preserve each source's conditions rather than turning unrelated experiments into a universal recipe.

The reviewed catalog rows link to their profile and reference IDs. Read `fermentation_scope` before plotting: some intervals summarize distinct paired protocols; equal temperature bounds can represent an approximate published process point. These fields do not describe biological tolerance limits. Species detections, named isolates, commercial mixtures and sequence accessions are kept distinct.

## Status

The catalog contains **46 products in 44 profile files**, and all rows have literature-backed status with explicit process scope. The shared registry contains **133 traceable references**. Sources have different strengths: primary experiments, reviews, standards, academic texts and limited manufacturer guidance are labelled accordingly. “Literature-backed” does not mean every aspect is settled or independently replicated.

The 2026-09-07 to 2026-09-08 review also corrected several earlier working assumptions. Blank numerical cells now mean no defensible universal value was found; ambient descriptions are not converted into invented temperatures; a blend code is not a strain; and separate processes reported under one name are preserved instead of averaged into a misleading range. Product-name collisions, such as Bulgarian versus Central Asian Katyk, are explicitly scoped.
