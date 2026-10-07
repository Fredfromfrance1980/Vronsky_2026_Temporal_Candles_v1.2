# Temporal candles · Chandelles temporelles

**A calibration map for locating gravitational anomalies in dimensionless clock coordinates**
**Un calque d'étalonnage pour situer les anomalies gravitationnelles en coordonnées d'horloges sans dimension**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23193464.svg)](https://doi.org/10.5281/zenodo.23193464)

**Frédérick Vronsky** — Independent researcher / Chercheur indépendant, Toulouse, France
ORCID: [0009-0003-5719-9604](https://orcid.org/0009-0003-5719-9604) · Version 1.2 · 6 October / octobre 2026 · CC BY-NC-SA 4.0

[English](#english) · [Français](#français)

---

## English

### What it is

Tests of general relativity (GR) are published in heterogeneous parameters, and anomalies such as the dynamics of disc galaxies are usually stated relative to a model. This paper builds a single map showing where gravity has been calibrated, where it has not, and where a given anomaly sits.

By analogy with the standard candles of the distance ladder, a **temporal candle** is a system whose mass is known independently of the measured effect, and for which the ratio ℛ = observed effect / GR prediction is published with an uncertainty. Each candle is placed in dimensionless clock coordinates: compactness X = GM/(Rc²), Y = M_P/M, and acceleration in Planck units g/a_P = X²Y. Five rules (C1–C5) make a candle usable; the workflow is calibrate, overlay, read, forecast.

**This is a methods paper**, carried out within classical general relativity. MOND with the external-field effect appears only as the alternative that the wide-binary test is designed to discriminate.

### Main results

1. **Calibration map.** Eight tests, from Gravity Probe A to GW150914, give ℛ = 1 over nine decades of compactness, but only at high acceleration.
2. **Disc galaxies.** 2,511 rotation-curve points from 155 SPARC galaxies lie about eight decades lower in acceleration than the candles. Their departure from ℛ = 1 is organised by acceleration (ρ = −0.87), not compactness (−0.72) or mass (+0.36); once the radial acceleration relation is removed, no dependence on X or Y remains. A known result recovered blindly: a test of the tool, not a discovery.
3. **Wide binaries.** The map singles them out as the only accessible non-galactic systems in the galactic acceleration band.
   - **Gaia EDR3** (11,678 pairs): γ = G_eff/G = 0.98 ± 0.005, 1.00 ± 0.015, 1.01 ± 0.035 in three acceleration bins; χ² = 1.2 for GR, 67.6 for MOND.
   - **Gaia DR3 rehearsal** (new in v1.2): sample rebuilt from the Gaia archive with the published EDR3 selection (72,728 pairs); γ = 0.968 ± 0.018, 0.986 ± 0.013, 1.004 ± 0.038; χ² = 0.9 for GR, 101 for MOND. Same stars as EDR3: not an independent test.
   - **Gaia DR4** (2 December 2026): the full analysis and a numerical decision rule are **frozen and pre-registered**; the result will be published whatever it is.

### Repository contents

This repository holds one archive, `Vronsky_2026_Temporal_Candles_v1.2_complet.zip`, identical to the Zenodo deposit. Unzipped, it gives a folder `V1.2/` with:

| File | Contents |
|---|---|
| `Vronsky_2026_Temporal_Candles_v1.2_EN.pdf` | paper in English (16 pages) |
| `Vronsky_2026_Chandelles_Temporelles_v1.2_FR.pdf` | paper in French (17 pages) |
| `calque_systemes.csv` | the 8 calibration candles |
| `sparc_chandelles.csv` | SPARC overlay: 2,511 points, 155 galaxies |
| `Vronsky_2026_Temporal_Candles_v1.2.zip` | code, LaTeX sources, figures, data, Gaia EDR3 and DR3 results, extraction queries |
| `ZENODO_texte_depot.txt`, `_FR.txt` | Zenodo deposit description (EN, FR) |

### Reproduce

Python 3 with numpy, scipy, pandas, matplotlib and astropy.

```bash
unzip Vronsky_2026_Temporal_Candles_v1.2_complet.zip
cd V1.2
unzip Vronsky_2026_Temporal_Candles_v1.2.zip
cd code
python chandelles_calque.py   # calibration map, SPARC overlay, RAR, residual tests
python figs.py                # Figures 2-4
python fig_gaia.py            # Figure 5
```

These scripts regenerate `data/resultats.json`, `data/calque_systemes.csv` and `data/sparc_chandelles.csv` identically. The wide-binary chain (Gaia DR3 rehearsal and DR4) is described in the README inside the code archive.

### Versions

- **1.0** (5 Oct 2026): first deposit.
- **1.1** (6 Oct 2026): Gravity Probe A value, Mercury as indicative candle, EDR3 selection made explicit.
- **1.2** (6 Oct 2026, before Gaia DR4): full rehearsal on Gaia DR3; new sample construction reproducing the EDR3 selection; measurement averaged over five frozen seeds. No cut, threshold or EDR3 number changed.

---

## Français

### De quoi s'agit-il

Les tests de la relativité générale (RG) sont publiés dans des paramètres hétérogènes, et les anomalies comme la dynamique des galaxies à disque sont le plus souvent énoncées par rapport à un modèle. Cet article construit une carte unique montrant où la gravitation a été étalonnée, où elle ne l'a pas été, et où se situe une anomalie donnée.

Par analogie avec les chandelles standard de l'échelle des distances, une **chandelle temporelle** est un système dont la masse est connue indépendamment de l'effet mesuré, et pour lequel le rapport ℛ = effet observé / prédiction de la RG est publié avec une incertitude. Chaque chandelle est placée en coordonnées d'horloges sans dimension : compacité X = GM/(Rc²), Y = M_P/M et accélération en unités de Planck g/a_P = X²Y. Cinq règles (C1 à C5) rendent une chandelle utilisable ; le mode opératoire est : étalonner, superposer, lire, prévoir.

**C'est un article de méthode**, mené dans le cadre classique de la relativité générale. MOND avec effet de champ extérieur n'y figure que comme l'alternative que le test des binaires larges doit départager.

### Principaux résultats

1. **Le calque.** Huit tests, de Gravity Probe A à GW150914, donnent ℛ = 1 sur neuf décades de compacité, mais seulement aux fortes accélérations.
2. **Les galaxies à disque.** 2 511 points de 155 galaxies SPARC se situent environ huit décades sous les chandelles en accélération. Leur écart à ℛ = 1 est organisé par l'accélération (ρ = −0,87), pas par la compacité (−0,72) ni la masse (+0,36) ; une fois la relation d'accélération radiale retirée, il ne reste aucune dépendance en X ou en Y. Un résultat connu retrouvé à l'aveugle : un test de l'outil, pas une découverte.
3. **Les binaires larges.** Le calque les désigne comme les seuls systèmes non galactiques accessibles dans la bande d'accélération galactique.
   - **Gaia EDR3** (11 678 paires) : γ = G_eff/G = 0,98 ± 0,005, 1,00 ± 0,015, 1,01 ± 0,035 ; χ² = 1,2 pour la RG, 67,6 pour MOND.
   - **Répétition Gaia DR3** (nouveau en v1.2) : échantillon reconstruit depuis l'archive Gaia selon la sélection publiée d'EDR3 (72 728 paires) ; γ = 0,968 ± 0,018, 0,986 ± 0,013, 1,004 ± 0,038 ; χ² = 0,9 pour la RG, 101 pour MOND. Mêmes étoiles qu'EDR3 : pas un test indépendant.
   - **Gaia DR4** (2 décembre 2026) : toute l'analyse et une règle de décision chiffrée sont **figées et pré-enregistrées** ; le résultat sera publié quel qu'il soit.

### Contenu et reproduction

Le dépôt contient une archive, `Vronsky_2026_Temporal_Candles_v1.2_complet.zip`, identique au dépôt Zenodo : articles FR et EN, tables des chandelles et de la superposition SPARC, et paquet de code (voir le tableau et les commandes de la partie anglaise). Les scripts régénèrent à l'identique les résultats et les tables de l'article.

---

## Citation

Vronsky, F. (2026). *Temporal candles: a calibration map for locating gravitational anomalies in dimensionless clock coordinates* (v1.2). Zenodo. https://doi.org/10.5281/zenodo.23193464

Companion paper / article compagnon : Vronsky, F. (2026). *Temporal fingerprints: a logarithmic reference frame of time scales for gravitational and quantum systems* (v2.0). Zenodo. https://doi.org/10.5281/zenodo.23116283

Data: SPARC (Lelli, McGaugh & Schombert 2016); Gaia EDR3 wide binaries (Pittordis & Sutherland 2023, Zenodo 7629240); ESA Gaia mission (DPAC).

Licence: CC BY-NC-SA 4.0 (see `LICENSE`).

The analysis code, figures and part of the text were prepared with the assistance of an AI model (Claude, Anthropic); the author defined the questions, checked the results and takes responsibility for the content. Le code d'analyse, les figures et une partie du texte ont été préparés avec l'aide d'un modèle d'IA (Claude, Anthropic) ; l'auteur a défini les questions, vérifié les résultats et assume la responsabilité du contenu.
