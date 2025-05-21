# Avian Immune Gene Expression Project

This project explores immune gene expression in barn owls (*Tyto alba*) simulated as co-infected with **Leucocytozoon** parasites and **Matryoshka virus**. It was completed as part of my Biometry final project and forms the foundation for my master’s thesis on host-parasite-virus interactions.

## Project Aim
**Research Question**  
How does immune gene expression vary between barn owls simulated as co-infected versus uninfected?

**Hypothesis**  
There is a significant difference in immune gene expression between co-infected and uninfected owls.

## Dataset
 * RNA-seq gene count data from **6 barn owl individuals**
 * Original data comes from Caroline Faircloth's project
 * For this Biometry course project, I used the existing dataset but **simulated infection status** (3 co-infected, 3 uninfected) to demonstrate statistical analysis techniques

## Statistical Approach
 * Welch's t-tests used for differential expression
 * Adjusted p-values using Benjamini-Hochberg correction
 * Genes filtered by significance (padj < 0.05) and log2FC > 1

 **Visualizations created:**
 
  * Volcano plot (primary figure)
  * Boxplots of top genes
  * Clustered heatmap

## Key Findings
While no genes reached statistical significance (likely due to small sample size), several patterns emerged:
* A1CF gene was expressed in uninfected owls but completely silenced in infected owls
* Hierarchical clustering in the heatmap showed separation between infected/uninfected samples
* Results suggest future studies should use larger sample sizes (15-20 owls per group)

## Limitations

* Infection status was simulated, not experimentally verified
* Small sample size (n = 6) limits statistical power
* No pathway or functional annotation analysis included
* Results are exploratory and require validation through qPCR or other methods

## Repository Structure
* `reads_per_gene/`: Directory containing RNA-seq gene count data
* `avian_immune_gene_expression.Rmd`: R Markdown analysis code
* `Immune Gene Expression in Barn Owls Co-infected with Leucocytozoon and Matryoshka Virus main.pdf`: Knitted output report
* `README.md`: This file

## How to Run
1. Clone this repository
2. Open `avian_immune_gene_expression.Rmd` in RStudio
3. Install required R packages if not already installed:
   ```r
   install.packages(c("pheatmap", "ggplot2", "viridis", "dplyr"))
4. Run the R Markdown document to reproduce the analysis   ```

## Author
Prathmesh Bhagwat