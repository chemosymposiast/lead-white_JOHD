# Lead White in Context Across Greco-Roman Sources — *TheSu* XML Annotation Dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19614479.svg)](https://doi.org/10.5281/zenodo.19614479)

The first public dataset encoded with the *TheSu* XML stand-off annotation schema, covering Greco-Roman passages on lead white (ψιμύθιον / *cerussa*).

**[https://thesu.io/](https://thesu.io/)**

## At a glance

- **Creator:** Daniele Morrone — KU Leuven, Institute of Philosophy
- **Languages:** English, Ancient Greek, Latin
- **Formats:** XML, XSD, CSS, XHTML, DOT, SVG
- **License:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- **Related paper:** *Lead White in Context Across Greco-Roman Sources: The First TheSu XML Annotation Dataset of Arguments and Recipes, with Graph Visualisations and Discussion of their Design* — invited full submission for peer review (June 2025) following abstract selection (June 2024); **preprint**.
- **Schema documentation:** [https://thesu.io/documentation/](https://thesu.io/documentation/)
- **Visualisation tool:** [chemosymposiast/TheSu-to-DOT](https://github.com/chemosymposiast/TheSu-to-DOT) — archived on Zenodo: [10.5281/zenodo.19613192](https://doi.org/10.5281/zenodo.19613192)

## What this dataset is

The dataset contains *TheSu* XML annotations of six sources discussing lead white: four ancient Greek texts (Plato, Theophrastus, Dioscorides, Plutarch) and two modern scientific studies (Caley & Richards 1956; Katsaros, Liritzis & Laskaris 2010). It also includes the Graphviz and Gephi graphs derived from those annotations and used as figures in the companion paper.

All annotations are collected in [ancient-lead-white_JOHD.xml](ancient-lead-white_JOHD.xml), which uses stand-off references: `THESIS`, `SUPPORT`, `PROPOSITION`, `sequence`, and `phase` elements point to tokenised `xml:id`s inside the files under [sources-segmented/](sources-segmented/), rather than containing the source text themselves.

## Sources

| Source                                                           | File                                                                                                                     |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Plato, *Lysis*                                                   | [sources-segmented/tlg0059.tlg020.perseus-grc2.xml](sources-segmented/tlg0059.tlg020.perseus-grc2.xml)                 |
| Theophrastus, *De lapidibus*                                     | [sources-segmented/tlg0093.tlg004.1st1K-grc1.xml](sources-segmented/tlg0093.tlg004.1st1K-grc1.xml)                     |
| Dioscorides, *De materia medica*                                 | [sources-segmented/tlg0656.tlg001.1st1K-grc1.xml](sources-segmented/tlg0656.tlg001.1st1K-grc1.xml)                     |
| Plutarch, *Quaestiones convivales*                               | [sources-segmented/tlg0007.tlg112.perseus-grc2.xml](sources-segmented/tlg0007.tlg112.perseus-grc2.xml)                 |
| Caley & Richards, 1956 (copyrighted, therefore largely redacted) | [sources-segmented/today_caley,richards_1956_copyrighted.xhtml](sources-segmented/today_caley,richards_1956_copyrighted.xhtml) |
| Katsaros, Liritzis & Laskaris, 2010                              | [sources-segmented/today_katsaros,liritzis,laskaris_2010.xhtml](sources-segmented/today_katsaros,liritzis,laskaris_2010.xhtml) |

## Repository structure

- [ancient-lead-white_JOHD.xml](ancient-lead-white_JOHD.xml) — main *TheSu* annotation document
- [ancient-lead-white_JOHD_new-propositions.xml](ancient-lead-white_JOHD_new-propositions.xml) — cross-source proposition models (included via XInclude)
- [meta/](meta/) — authority records (indexing tags, relationship tags, people, bibliography)
- [schema/](schema/) — TheSu.xsd and TheSu_tags.xsd
- [css/](css/) — Oxygen Author-mode stylesheets for the schema and its tag vocabularies
- [sources-original/](sources-original/) — unsegmented base editions of the open-licence sources
- [sources-segmented/](sources-segmented/) — tokenised editions used as stand-off link targets
- [visualisations/](visualisations/) — per-figure folders (figures 1–8 of the paper) with Graphviz and Gephi .dot files and .svg outputs

## How to explore the annotations

- Recommended: open [ancient-lead-white_JOHD.xml](ancient-lead-white_JOHD.xml) in [Oxygen XML Editor](https://www.oxygenxml.com/) in **Author mode**. The CSS in [css/TheSu/](css/TheSu/) is applied automatically via the `xml-stylesheet` processing instruction at the top of the file.
- Any standard XML editor or web browser also works for structural inspection.
- For the meaning of elements, attributes, and tag vocabularies, see the schema documentation at [https://alchemeast.eu/thesu/ns/1.0/documentation/TheSu.html](https://alchemeast.eu/thesu/ns/1.0/documentation/TheSu.html).

## Reproducing the visualisations

The `.dot` and `.svg` files under [visualisations/](visualisations/) can be regenerated from the annotation using the companion tool **TheSu-to-DOT**:

- Repository: [https://github.com/chemosymposiast/TheSu-to-DOT](https://github.com/chemosymposiast/TheSu-to-DOT)
- Archived release: [10.5281/zenodo.19613192](https://doi.org/10.5281/zenodo.19613192)

The tool ships per-figure presets (one subfolder per figure under `_config_presets/`, e.g. `1.Plutarch`, `2.Plato`, …, `8.everything`) and step-by-step reproduction instructions in its `JOHD_dataset_reproduction.md`.

The Gephi layouts used in the paper (ForceAtlas 2, Fruchterman–Reingold) are applied manually inside Gephi after importing the generated `*_gephi.dot` files, as documented by the tool.

## Citation

* **Data paper (preprint)**
  Morrone, Daniele. 2025. "Lead White in Context Across Greco-Roman Sources: The First *TheSu* XML Annotation Dataset of Arguments and Recipes, with Graph Visualisations and Discussion of their Design". Preprint (first submitted June 2025).

  ```
  Morrone, Daniele. 2025. "Lead White in Context Across Greco-Roman Sources: The First TheSu XML Annotation Dataset of Arguments and Recipes, with Graph Visualisations and Discussion of their Design". Preprint (first submitted June 2025).
  ```

* **Dataset**
  Morrone, Daniele. 2026. "chemosymposiast/lead-white_JOHD: v1.0.0 – First Public Release (v1.0.0)". *Zenodo*. [https://doi.org/10.5281/zenodo.19614479](https://doi.org/10.5281/zenodo.19614479)

  ```
  Morrone, Daniele. 2026. "chemosymposiast/lead-white_JOHD: v1.0.0 – First Public Release (v1.0.0)". Zenodo. https://doi.org/10.5281/zenodo.19614479
  ```

* **Visualisation tool**
  Morrone, Daniele. 2026. "chemosymposiast/*TheSu*-to-DOT: v1.0.0 – First release (v1.0.0)". *Zenodo*. [https://doi.org/10.5281/zenodo.19613192](https://doi.org/10.5281/zenodo.19613192)

  ```
  Morrone, Daniele. 2026. "chemosymposiast/TheSu-to-DOT: v1.0.0 – First release (v1.0.0)". Zenodo. https://doi.org/10.5281/zenodo.19613192
  ```

## License

- Full license text: [LICENSE](LICENSE) (CC BY-SA 4.0).
- Annotations, schema, stylesheets, and derived visualisations in this repository: **CC BY-SA 4.0**.
- Third-party source texts retain their original licences:
  - Perseus / PerseusDL *canonical-greekLit* and OpenGreekAndLatin *First1KGreek* editions — CC BY-SA 4.0.
  - Katsaros, Liritzis & Laskaris, 2010 — CC BY-NC-ND 4.0.
  - Caley & Richards, 1956 — copyrighted; the segmented XHTML is intentionally redacted, keeping only the boundary words of referenced spans for annotation verification (see section 3.1 of the paper).
