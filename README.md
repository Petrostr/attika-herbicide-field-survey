# From Phone to Pixel

**Open-source field ground truth for describing cultivation practices in olive groves, vineyards and other plots in Greece**

Petros Stratis · Dr. Vassilios Andronis · Em. Prof. Demetre Argialas
Remote Sensing Laboratory, School of Rural, Surveying and Geoinformatics Engineering, National Technical University of Athens (NTUA)

> Poster presented at the **IEEE GRSS Student and Young Professionals Summit 2026**, Naples, 14–15 November 2026.

---

## Why

CAP area monitoring and organic certification rely more and more on satellite checks. Farmers need simple ways to document their cultivation practices, auditors need structured evidence, and Earth-observation models need reliable training labels from the field, not from declarations.

## Workflow

**QGIS** (project + coded form) → **Mergin Maps** (sync to phone, works offline) → **field** (GPS point, coded answers, up to 3 photos) → **back to QGIS** (quality control, ground truth for Sentinel-2 / PlanetScope).

All tools are free and open source.

## What each point records

| Field | Values |
|---|---|
| `crop_type` | vineyard, olive, pistachio, fig, uncultivated, other |
| `spray_status` | sprayed-like, not sprayed, uncertain |
| `understory_state` | green, yellow/dry, bare soil, tilled, mowed, mixed |
| `management_evidence` | herbicide-, tillage-, mowing-consistent, no suppression, uncertain |
| `confidence` | A (sure), B, C |
| `control_case` | yes, no, possible |
| `photo`, `photo1`, `photo2` | up to 3 photos per point |
| `date_time`, `notes` | automatic timestamp, free text |

*"Sprayed-like" = visual evidence consistent with herbicide use, not a confirmed application.*

## Dataset (spring 2026)

- **495** coded field points in **11 field days** (29 April – 22 June 2026), Eastern Attica (+7 on Andros)
- 246 vineyard · 132 olive · 38 uncultivated · 30 pistachio · 8 fig · 28 other
- Spray status: 210 sprayed-like · 213 not sprayed · 66 uncertain
- Management evidence: 137 herbicide · 119 no suppression · 78 tillage · 43 mowing
- Confidence: A 310 · B 64 · C 14
- Plus 101 pilot points recorded with an earlier form (same plots)

**The point data are not published yet** (analysis in preparation).

## Next steps

- PlanetScope (3 m) + object-based analysis: separate canopy from inter-row soil
- Sentinel-2 time series: can herbicide, tillage and mowing be told apart?
- Target: IGARSS 2027, Reykjavík

## Acknowledgements

This research was supported by the Hellenic Foundation for Research and Innovation (H.F.R.I.) under the 4th Call for H.F.R.I. PhD Fellowships (Fellowship Number: 011270).

## Contact

ORCID: [0009-0002-5954-1162](https://orcid.org/0009-0002-5954-1162) 
ORCID: [0009-0002-5954-1162](https://orcid.org/0000-0002-9757-3600) 
ORCID: [0009-0002-5954-1162](https://orcid.org/0000-0003-1699-6714) 
