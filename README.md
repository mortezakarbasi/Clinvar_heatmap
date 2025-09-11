# ClinVar Heatmap Visualization

This repository provides a simple workflow to extract, clean, and visualize ClinVar data (gene-level) as a heatmap.  
We use the [clinvar-perl](https://github.com/dlal-group/clinvar-perl) tool for preprocessing and then generate heatmaps in Jupyter Notebook.

---

## 1. Installation

First, install the required Perl dependencies:

```bash
sudo apt-get update
sudo apt-get install liblist-moreutils-perl
sudo apt-get install libsort-fields-perl
```
Clone the clinvar-perl repository:
```bash
git clone https://github.com/dlal-group/clinvar-perl.git
cd clinvar-perl
```
2. Download ClinVar Data
Get the latest ClinVar variant summary file from the NCBI FTP:

```bash
wget https://ftp.ncbi.nlm.nih.gov/pub/clinvar/tab_delimited/variant_summary.txt.gz
gzip -d variant_summary.txt.gz
```
3. Generate a Clean Data File for a Gene
Use the clinvar-viewer.pl script to extract summary data for your gene of interest.

Example for IGHMBP2:

```bash
perl clinvar-viewer.pl summary gene IGHMBP2
# This will create a clean tab-delimited file for the selected gene. In this example gene name is IGHMBP2.
```
📺 Tutorial video: How to use [clinvar-perl](https://www.youtube.com/watch?v=ivuM2d9B4yI)

4. Visualize in Jupyter Notebook
Open the provided Jupyter Notebook (example: IGHMBP2_heatmap.ipynb), replace the gene filename if needed, and run the notebook to generate your heatmap.

📺 Tutorial video: Draw ClinVar [heatmaps](https://www.youtube.com/watch?v=0U9cs2V-Mqc)

Example Workflow
```bash
# Extract gene-specific file
perl clinvar-viewer.pl summary gene IGHMBP2

# Launch Jupyter Notebook
jupyter notebook IGHMBP2_heatmap.ipynb
The notebook will generate a heatmap of ClinVar variants for the gene.
```
References
[clinvar-perl GitHub](https://github.com/dlal-group/clinvar-perl)
[ClinVar FTP (NCBI)](https://ftp.ncbi.nlm.nih.gov/pub/clinvar/tab_delimited/)
