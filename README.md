# scannot-reference

Reference datasets for **scannot**, a reference-based single-cell RNA-seq cell-type annotation tool.

This repository provides curated Seurat reference objects that can be used for cell-type annotation with scannot.

Large reference RDS files are distributed through GitHub Releases rather than stored directly in the Git repository.

---

## Available references

| Reference | Species | Tissue / stage | Cells | Version | Annotation column |
|---|---|---|---:|---|---|
| Rice seedling aerial | *Oryza sativa* | Seedling aerial tissue | 30,300 | v1.0.0 | `cluster_annotation` |

---

## Rice seedling aerial reference

### Basic information

- Reference name: `rice_seedling_aerial`
- Species: *Oryza sativa*
- Tissue / stage: Seedling aerial tissue
- Cells: 30,300
- Object type: Seurat
- Default assay: `SCT`
- Annotation column: `cluster_annotation`
- PCA reduction: `pca`
- UMAP reduction: `umap`
- UMAP model: available
- Reference version: v1.0.0

### Cell types

The current reference contains six annotated cell types:

- Mesophyll
- Epidermis
- Mestome_sheath
- Xylem
- Preprocambium
- Phloem

### Reference file

The reference object is distributed through the Releases section of this repository.

File:

`rice_seedling_aerial_ref.rds`

Checksum:

`rice_seedling_aerial_ref.rds.sha256`

---

## Use with scannot

After downloading the reference RDS, it can be used directly:

```bash
scannot anno \
--query=/path/to/query.rds \
--outdir=/path/to/output \
--ref=/path/to/rice_seedling_aerial_ref.rds \
--label_col=cluster_annotation
