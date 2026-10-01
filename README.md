# GGSL in SLICE

Supporting data for a scientific report on a systematic search of galaxy–galaxy strong lensing (GGSL) candidates in dense environments among SLICE galaxy clusters ($z \sim 0.20$ -- $0.83$), using JWST and HST imaging.

Across 50 cluster lines-of-sight, 172 candidates were catalogued and 29 GGSL systems (spanning 21 clusters) were modeled with Lenstool. This repository holds the working files underlying that report and mirrors the layout used during the analysis; the actual imaging data are gitignored and remain local.

## Layout

| Path | Description |
|------|-------------|
| `JWST_SLICE_data/` | Directory tree matching the JWST mosaic folders for inspected clusters. DS9 region (`.reg`) and backup (`.bck`) files are stored inside each cluster’s mosaic folder alongside the local data. Also includes "scan manifests" (used for a helper script that automatically pans the view in DS9) and curated candidate thumbnails (`Good_lensing/`). |
| `Models/` | Per-cluster Lenstool working directories for the modeled systems (parameter files, image constraints, outputs), including the models used for compiling the Results in the associated report under `Finished/`. Modeling stages include no-external-shear (isolated lenses), external-shear, and (where applicable) inclusion of cluster potentials. |

**DS9 regions:** the `.reg` files mark the observed multiple images / arcs used as positional constraints. They do not mark the lensing galaxy (or galaxies).

## Context

SLICE (Strong LensIng and Cluster Evolution; PI: G. Mahler; Cerny et al. 2026, ApJ, 1001, 60) focuses on 124 clusters observed with JWST. This work is restricted to the subset of clusters in the redshift range $0.20 < z < 0.83$ and focuses on GGSL events embedded within and in the line-of-sight of cluster environments. From the models we extract effective Einstein radii and enclosed masses within the external critical curve, and compare them with literature values across three mass scales: isolated galaxies, galaxy groups, and galaxy clusters.
