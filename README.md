# Muscle Contractility Lab — RYR1

**Name:** Obiñeta, Inah Marie  
**Date Completed:** October 27, 2026  
**Course:** Cell and Molecular Biology  
**Organism:** *Homo sapiens*  
**Tools:** R/RStudio, NCBI, UniProt, GitHub  

---

## Assignment Details
**Gene:** 21. RYR1 — NM_000540.3:c.6617C>T (p.Thr2206Met) — ClinVar 12977 [missense]  
**Protein Accession:** NP_000531.2  
**Protein Length:** 5,038 amino acids

---

## Process — R Workflow
```r
# 1. Install and load required packages
install.packages(c("rentrez", "ggplot2"))
library(rentrez)
library(ggplot2)

# 2. Define assignment values
gene_symbol       <- "RYR1"
transcript_accession <- "NM_000540.3"
variant_protein   <- "p.Thr2206Met"

# 3. Create output folders
for (d in c("data", "results", "figures")) {
  dir.create(d, showWarnings = FALSE)
}

# 4. Retrieve gene information from NCBI
hits <- entrez_search("gene", paste0(gene_symbol, "[Gene Name] AND txid9606[Organism]"))
gene_info <- entrez_summary("gene", hits$ids[1])

writeLines(c(
  paste("Gene symbol:", gene_info$name),
  paste("NCBI Gene ID:", hits$ids[1]),
  paste("Chromosome:", gene_info$chromosome)
), "results/gene_summary.txt")

# 5. Retrieve protein sequence — saved to data/RYR1_Protein.fasta
# Protein accession written to results/protein_accession.txt

# 6. Calculate amino-acid composition
fasta_lines <- readLines("data/RYR1_Protein.fasta")
sequence <- paste(fasta_lines[!startsWith(fasta_lines, ">")], collapse = "")
aa_codes <- strsplit(toupper(sequence), "")[[1]]

standard_aa <- strsplit("ACDEFGHIKLMNPQRSTVWY", "")[[1]]
count_table <- table(factor(aa_codes, levels = standard_aa))

composition_df <- data.frame(
  AminoAcid = standard_aa,
  Count = as.integer(count_table)
)

write.csv(composition_df, "results/amino_acid_composition.csv", row.names = FALSE)

# 7. Generate amino-acid composition plot
composition_plot <- ggplot(composition_df, aes(AminoAcid, Count)) +
  geom_col(fill = "gray45") +
  theme_bw() +
  labs(title = "RYR1 Amino-Acid Composition", x = "Amino acid", y = "Number of residues")

ggsave("figures/01_amino_acid_composition.png", composition_plot, width = 8, height = 5, dpi = 300)

# 8. Generate variant position plot
protein_length <- 5038
variant_position <- 2206

position_plot <- ggplot() +
  geom_segment(aes(x = 1, xend = protein_length, y = 0, yend = 0), linewidth = 2) +
  geom_point(aes(x = variant_position, y = 0), size = 5, color = "red") +
  annotate("text", x = variant_position, y = 0.3, label = variant_protein, fontface = "bold") +
  labs(title = "RYR1 Reference Protein", x = "Amino-acid position") +
  theme_void() +
  theme(axis.title.x = element_text())

ggsave("figures/02_variant_position.png", position_plot, width = 8, height = 2.5, dpi = 300)
