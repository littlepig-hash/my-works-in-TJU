# Genome-scale CRISPRi（pcnB 抑制）对 E. coli 转录组的影响——差异表达与富集分析
生信的小小尝试，感谢房老师的数据集：GEO 系列 GSE267710（6 个样本：对照 A×3、工程株 AP×3）。页面含 Series Matrix 与核心基因表，以及 SRA 原始测序数据。from国家生物技术信息中心
Nature Communications 2025-03-29。文中声明转录组数据已存入 GEO：GSE267710；相关 NGS 筛选数据 GSE267827；蛋白组学 PXD052390

# GSE267710 • RNA-seq Differential Expression (AP vs A in *E. coli* K-12)

**Goal.** Reproduce a concise RNA-seq DE analysis for pcnB repression (AP) vs control (A), then visualize and (optionally) run GO/KEGG enrichment.

**Data.**
- GEO: [GSE267710](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE267710) (6 samples; A: GSM8273564–66, AP: GSM8273567–69). Series Matrix + core gene table + SRA links.  
- Paper: Fang *et al.*, *Nat Commun* (2025). DOI: 10.1038/s41467-025-58368-3. Transcriptomics: GSE267710; screen: GSE267827; proteomics: PXD052390.

## Quick start
```bash
bash scripts/00_download.sh
Rscript scripts/10_deseq2_DE.R
Rscript scripts/20_plots.R
# optional:
Rscript scripts/30_enrichment.R
