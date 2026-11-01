[README.md](https://github.com/user-attachments/files/34234437/README.md)
# Single-cell analyses identify perivascular remodeling in SSc skin

This folder is the GitHub browser-upload set for the study's derived computational analyses and figure source files. Upload **every file in this folder** to the repository root: <https://github.com/byby131/Single-cell-analyses-identify-perivascular-remodeling-in-SSc-skin>. Each file is below 25 MB, and the upload set contains fewer than 100 files and no nested folders. `MANIFEST.csv` provides sizes and SHA-256 checksums.

## Contents

| File | Contents |
| --- | --- |
| `01_regression_and_pseudobulk.zip` | Participant-level regression inputs, diagnostics, aggregated pseudobulk counts and metadata, gene-set membership, thresholds, session information, and R scripts for the primary association and ECM sensitivity analyses. |
| `02_ligand_immune_composition.zip` | Frozen NicheNet inputs and weights, matched-null and ligand-program results, equivalent myeloid/T/NK models, composition and cell-flow outputs, source tables, session information, and self-contained R reproduction scripts. |
| `03_reviewer_figures_vector.zip` | Vector PDF and SVG versions of the revised computational review figures and Supplementary Figures 7–9. |
| `04a_discovery_selection_summary.zip` | Reconstructed GSE195452 cell-selection flow, per-participant summaries, input provenance, and reconstruction scripts. |
| `04b_discovery_cell_audits.zip` | Detailed per-cell GSE195452 selection and quality-control CSVs. The large CSVs are compressed **inside** the ZIP. |
| `05_original_panel_sources.zip` | Original panel-level CSV source data and plotting scripts, including earlier plot variants. File names identify those variants. |
| `06_cellchat_and_liana.zip` | CellChat and LIANA-compatible outputs plus the associated analysis scripts. |
| `07_SupplementaryMaterials_11.1.docx` | Current supplementary material, including Supplementary Tables 1–5 and figure legends. |

## Reproduction

Extract `01_regression_and_pseudobulk.zip` into its own directory and run its `scripts/regression.R`, `scripts/pseudobulk.R`, then `scripts/threshold_figure.R` from that directory. Extract `02_ligand_immune_composition.zip` into a different directory and run `scripts/reproduce_ligands.R`, `scripts/reproduce_immune_models.R`, `scripts/reproduce_composition.R`, and `scripts/reproduce_supplementary_figures.R` from its root. Package versions are recorded in the `sessionInfo` files. The two archives contain their own inputs and intentionally duplicate a few small shared reference tables.

The primary discovery and independent validation data are public under GEO accessions [GSE195452](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE195452) and [GSE138669](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE138669). The packages contain derived inputs for the review analyses, not the full raw single-cell objects. The `04a`, `04b`, and `05` archives preserve source and reconstruction scripts, but some scripts were developed with local data paths and require the downloaded GEO objects and path configuration to rerun from raw cells. `06` likewise requires the public single-cell object and the relevant R packages for a full rerun.

This release does not contain the original mouse-level microscopy measurements or raw immunofluorescence images. Figure 6's original experimental data should be deposited from the laboratory records if they are to be shared publicly; the computational files here cannot reconstruct those measurements. The supplementary DOCX is supplied for cross-reference and is also a separate journal submission file.

The ZIP files preserve editable scripts and tabular data while keeping the GitHub browser upload within the user's per-file and item-count limits. Download and extract them to inspect or run the analyses.
