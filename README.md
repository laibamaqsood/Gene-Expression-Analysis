# 🧬 Gene Expression Analysis (EdgeR)

### Differential expression analysis between IDH-MUT and Diffuse Astrocytoma (DA) samples

---

## 🔍 Overview
This project identifies differentially expressed genes between **IDH-mutant** and **Diffuse Astrocytoma (DA)** RNA-seq samples using **EdgeR**.  
Results include statistical summaries, volcano plots, heatmaps, and enrichment analyses.

---

## ⚙️ Workflow

1. **Data preparation**
   - Input: `combined_RNAs.csv` (samples × genes)
   - Groups: IDH-MUT = DA06, DA01, DA05, GB07

2. **EdgeR analysis**
   - Filtered genes with mean counts < 10  
   - Normalization: TMM  
   - Test: DA vs IDH-MUT  
   - Significance: p < 0.05, |log₂FC| > 1  

3. **Visualization**
   - Volcano plot of DEGs  
   - Heatmap of top 50 genes  

4. **Functional analysis (g:Profiler, GSEA)**
   - GO terms: BP, MF, CC  
   - KEGG pathways  
   - Highlighted key activated and inhibited biological processes

---

## 📊 Key Results

| Metric | Count |
|---------|--------|
| Significant DE genes | 1,544 |
| Upregulated (log₂FC > 1) | 660 |
| Downregulated (log₂FC < -1) | 884 |

**Activated pathways:** Neuroactive ligand–receptor interaction, Wnt signaling  
**Inhibited pathways:** ECM organization, PI3K–Akt signaling, Focal adhesion

---

## 🧩 Conclusion
IDH-MUT gliomas show reduced ECM and PI3K–Akt activity, indicating less invasiveness and altered metabolic regulation. Enrichment in neuronal pathways suggests compensatory signaling changes.



