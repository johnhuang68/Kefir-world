[English](freshly-fermented-instructions-audit.md) | [繁體中文](freshly-fermented-instructions-audit.zh-Hant.md)

# Freshly Fermented instruction-page audit

**Reviewed:** 2026-09-08

**Scope:** all 79 sitemap entries under `/instructions/` screened; 15 dairy product protocols extracted and additional dairy-topic guides evaluated

**Evidence class:** commercial, product-specific manufacturer/retailer guidance; not peer reviewed

## Why this source is useful

The pages give unusually concrete handling details that academic product descriptions often omit: starter form, first-batch activation, milk volume, inoculum amount, incubation window, visible endpoint, whey-draining step and the age of product recommended for backslopping. Those observations are stored in [`data/manufacturer_processes.csv`](../data/manufacturer_processes.csv), where activation, routine fermentation, cold fermentation and reculturing are separate records.

They are not used to redefine a traditional product's normal temperature range or microbial identity. The pages describe the supplier's current products and do not disclose lot-specific organism lists, strain designations, certificates of analysis or genomic accessions.

## Broader library screening

The full sitemap also contains articles about [reusing yogurt culture](https://freshlyfermented.co.uk/instructions/how-many-times-can-i-reuse-a-yogurt-culture-practical-guide-from-freshly-fermented/), [thermophilic yogurt without a machine](https://freshlyfermented.co.uk/instructions/how-to-make-thermophilic-yoghurt-without-a-yoghurt-maker/), milk choice, kefir shipping and storage, troubleshooting, second fermentation, plant substrates and health reactions. These pages were screened for new evidence rather than treated as independent support merely because the same time or temperature appeared again.

One linked 2026 primary paper supplied usable new data and was registered as **MK008**. It compared a commercial freeze-dried kefir starter in 0.1% and 3.1% fat UHT cow milk at 25 °C for 20 or 26 h. The full-fat product showed higher water-holding capacity and viscosity under that study's conditions. The Milk Kefir profile records the process, endpoint measurements and its limitation: this was a small defined-starter experiment, not natural kefir-grain evidence.

The remaining general guides did not add independently supported species, strain or traditional-process evidence. Some citations did not support the nearby claim: for example, the yogurt-reuse article links a qPCR study that monitored four named commercial strains at 41 and 43 °C, but that experiment does not demonstrate that an unspecified “heirloom” culture can be recultured indefinitely. Repeated generic advice was therefore left out of the structured table when a more direct product instruction page already covered the same operation.

## Integrated existing products

| Product | Source IDs | Useful supplier-specific observations | Integration decision |
|---|---|---|---|
| Milk Kefir | FF001–FF003 | Fresh-grain recovery, freeze-dried-grain activation, routine grain ratio and a separate 5 °C method | Added to the profile and process table; the 5 °C method does not alter the catalog's traditional 20–25 °C range |
| Viili | FF004 | 150 mL activation batch; 24–72 h activation; 12–48 h later batches; previous product younger than seven days | Added as a marketed freeze-dried starter protocol; no organism or EPS claim imported |
| Piimä | FF005 | Activation and routine backslopping quantities and times | Added as a commercial protocol; no Finnish lineage identity inferred |
| Filmjölk | FF006 | 1 L batch, 20–25 °C and 24–48 h; about one tablespoon per litre for later batches | Stored separately from the narrower academic process example |
| Caspian Sea Yogurt | FF007 | 1 L batch, 20–25 °C and 24–48 h; backslopping quantity | Added as a second supplier protocol; not evidence for the published FC/FA strain pair |
| Amasi | FF008 | 1 L batch, 20–25 °C and 24–48 h; backslopping quantity | Added as a marketed-starter process distinct from Southern African household surveys |
| Bulgarian Yogurt | FF009 | 42 °C, about 8 h, up to 18 h for the first batch, then chilling | Added as product handling; not evidence of strain composition or Bulgarian protected-origin status |
| Skyr | FF010 | 42 °C, about 10 h, then 8–12 h refrigerated whey drainage | Added without replacing historical Skyr process evidence or implying rennet use |
| Greek Yogurt | FF011 | 42 °C, about 10 h, then 8–12 h refrigerated whey drainage | Added as one starter's workflow; straining remains a processing step, not a unique microbial identity |

## Candidate products retained outside the core catalog

| Candidate | Source ID | Potentially useful data | Why it is not yet a core product row |
|---|---|---|---|
| Russian Thickset Yogurt | FF012 | 42 °C; about 8 h, with up to 24 h for the first set | The page gives no regional definition, organism list or strain identity, so the product name cannot yet be linked to a documented tradition |
| Cultured Buttermilk | FF013 | 20–25 °C; activation and routine backslopping process | This is a useful modern category, but an authoritative identity/process source and microbial evidence should be attached before catalog inclusion |
| Crème Fraîche | FF014 | 20–25 °C cream fermentation and backslopping process | A supplier page alone is insufficient to define a traditional or standardized profile and its organisms |
| Sour Cream | FF015 | 20–25 °C cream-and-milk fermentation and backslopping process | The supplied recipe is product specific; standards and primary starter-culture evidence are still needed |

These candidates remain queryable in the manufacturer process table. They should move into `data/fermented_milk.csv` only after an authoritative definition and product-linked microbiology are found.

## Claims deliberately excluded

- No species or strain was inferred from a product name. The instruction pages do not establish the contents of the sachets.
- “Reculture weekly” was recorded as handling advice, not proof that community composition or performance stays stable indefinitely.
- Supplier success rates, unspecified “laboratory tests,” health benefits and storage claims were not promoted to scientific facts without a traceable study.
- The cold-kefir page's statements about greater kefiran, microbial diversity and health effects were excluded because the page gives no checkable supporting source.
- Several pages contained unresolved `contentReference`/`oaicite` text in the rendered copy. This lowers editorial confidence and is another reason to use only directly stated process instructions.
- Similar or repeated times across pages were not treated as evidence that the products share the same organisms or traditional method.

## Source register

Full titles, URLs and claim scopes are registered as **FF001–FF015** in [`data/references.csv`](../data/references.csv). Modification dates for the 15 registered product pages, as reported by the site's XML sitemap, ranged from 2026-05-28 to 2026-06-05; all pages were accessed on 2026-09-08. Because web instructions can change, future updates should preserve the access date and compare the source text before overwriting observations.
