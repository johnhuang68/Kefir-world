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

Milk Kefir, Viili, Långfil, Filmjölk, Piimä, Tätemjölk/Tettmelk, Caspian Sea Yogurt, Dadih, Ergo, Lben/Leben, Nunu/Nono, Mabisi, Dhanaan, Rayeb/Raib, Amasi/Maas, Suusac, Chal/Shubat, Kumis/Airag, Matsoni/Matzoon, Dahi/Curd, Mishti Doi, Laban, Zabadi, Skyr, Acidophilus Milk, Bifidus Milk, AB Yogurt, ABT Yogurt, Traditional Yogurt, Greek Yogurt, Bulgarian Yogurt, and Labneh.

## Repository structure

- `data/fermented_milk.csv` — core catalog
- `data/references.csv` — shared reference registry
- `profiles/` — detailed product profiles with claim-level citations
- `docs/data_dictionary.md` — field definitions and evidence rules
- `research/roadmap.md` — research backlog and validation plan

## Detailed profiles

| Product | Profile focus |
|---|---|
| [Milk Kefir](profiles/milk-kefir.md) | Existing first profile; grain consortium and kefiran |
| [Caspian Sea Yogurt](profiles/caspian-sea-yogurt.md) | Japanese lineage; FC/FA and KYG22; powder activation versus transfers |
| [Viili](profiles/viili.md) | Finnish versus Taiwanese cultures; EPS; traditional fungal surface |
| [Långfil](profiles/langfil.md) | LAPT 3001; ropiness and trait retention; unresolved fermentation duration |
| [Filmjölk](profiles/filmjolk.md) | Mesophilic aromatic milk; species evidence without invented strain codes |
| [Matsoni / Matzoon](profiles/matsoni.md) | Regional ecology; traditional and pilot production; later genomic identification corrections |
| [Dahi](profiles/dahi.md) | Regional communities; defined starter strains; EPS and storage experiments |
| [Bulgarian Yogurt](profiles/bulgarian-yogurt.md) | Yogurt species versus strains; PDO identity; microbial cooperation |

The seven profiles added on **2026-09-06** cover history, milk and process, temperature/time, sensory properties, microbial ecology, published isolate designations, EPS, acidification, propagation, storage and evidence gaps. A missing strain ID or storage duration remains explicitly unknown.

## Evidence policy

Temperature, microorganism, origin, and fermentation-time fields should be treated as reference-backed data. Traditional products often vary by household, region, milk type, and starter lineage. Preserve each source's conditions rather than turning unrelated experiments into a universal recipe.

The reviewed catalog rows link to their profile and reference IDs. Read `fermentation_scope` before plotting: some intervals summarize distinct paired protocols; equal temperature bounds can represent an approximate published process point. These fields do not describe biological tolerance limits. Species detections, named isolates, commercial mixtures and sequence accessions are kept distinct.

## Status

The catalog contains **34 products**. Seven rows now have detailed literature-backed profiles and explicit process scope; the other 27 retain their existing working-draft status. The shared registry contains **64 references**, including the seven existing milk-kefir entries. Sources have different strengths: primary experiments, reviews, standards and one named manufacturer's practical guidance are labelled accordingly. “Literature-backed” does not mean every aspect is settled or independently replicated.
