# Tutorial: Preparing Sample Tables for Bioinformatics Processing

This tutorial is designed to help lab personnel create sample tables in the correct format for bioinformatics processing and subsequent submission to the European Nucleotide Archive (ENA). By following these guidelines, you can ensure that your data is prepared correctly and minimize delays during the analysis process.

---

## 1. Introduction to ENA Submissions
The European Nucleotide Archive (ENA) is a comprehensive resource for nucleotide sequence data. Submitting accurate and well-formatted sample metadata is crucial to ensure the data's usability and compliance with ENA requirements.

---

## 2. Required Fields for Sample Tables
Below are the mandatory fields you must include in the sample table, along with a brief description of each field:

| Field Name            | Description                                                                                   |
|-----------------------|-----------------------------------------------------------------------------------------------|
| **tax_id**          | The NCBI taxonomy ID for the organism (e.g., `9606` for Homo sapiens).                        |
| **scientific_name**          | Scientific name of the organism as in the NCBI Taxonomy database. Scientific names typically follow the binomial nomenclature. For example, the scientific name for humans is Homo sapiens. (e.g., `Homo sapiens`, `human skin metagenome`)                       |
| **sample_alias**          | **Unique** name of the sample. If not selected system will auto generate an unique alias. It must start with a letter and can only contain letters, numbers or underscores (e.g., `run108_PH3902`)                       |
| **sample_title**          | Title of the sample. (e.g., `NC01`, `AD014_6M_SK_R`)                        |
| **sample_description**       | A brief description of the sample (e.g., `Human blood sample for miRNA sequencing`).         |
| **collection date**   | The date the sample was collected with the intention of sequencing, either as an instance (single point in time) or interval. In case no exact time is available, the date/time can be right truncated i.e. all of these are valid ISO8601 compliant times: 2008-01-23T19:23:10+00:00; 2008-01-23T19:23:10; 2008-01-23; 2008-01; 2008. (e.g., `2024-12-12`).                                 |
| **gegeographic location (country and/or sea)** | The geographical origin of where the sample was collected from, with the intention of sequencing, as defined by the country or sea name (e.g., `Czechia`).  
| **instrument_model**          | The sequencing instrument model used in the experiment (e.g., `Illumina MiSeq`). Leave empty if not sure. See Chapter 4: Permitted Values.           |
| **library_name**          | The name for the library if any (e.g., `S24_016_01`).           |
| **library_source**          | The type of source material that is being sequenced (e.g., `METAGENOMIC`). See Chapter 4: Permitted Values.           |
| **library_selection**          | The method used to select for or against, enrich, or screen the material being sequenced (e.g., `PCR`). See Chapter 4: Permitted Values.          |
| **library_strategy**          | The sequencing technique intended for this library (e.g., `AMPLICON`, `WGS`). See Chapter 4: Permitted Values.          |
| **library_layout**          | The library layout specifies whether to expect single or paired configuration of reads (e.g., `SINGLE`, `PAIRED`). See Chapter 4: Permitted Values.           |
| **project_id**          | The project ID data belongs to (e.g., `IM065`).                        |                
| **run_id**          | The run ID data belongs to (e.g., `run109`).           |
| **pool**          | The Pool ID sample belongs to (e.g., `pool1`).           |
| **primer**          | The primer ID sample belongs to (e.g., `IL09`, `EMP07`).           |
| **lims_id**          | The LIMS ID sample belongs to (e.g., `2348`).           |
| **additional fields** | Include fields specific to your project, such as `treatment`, `replicate`, or `tissue_type`. |

---

## 3. Using the Sample Table Template
To simplify the process, we provide a downloadable template in `.csv` format. [Download the template here](#).

### Example Template

---

## 4. Permitted Values

### Instrument_model

| **Sequencer Name**             |
|--------------------------------|
| 454 GS                         |
| 454 GS 20                      |
| 454 GS FLX                     |
| 454 GS FLX Titanium            |
| 454 GS FLX+                    |
| 454 GS Junior                  |
| AB 310 Genetic Analyzer        |
| AB 3130 Genetic Analyzer       |
| AB 3130xL Genetic Analyzer     |
| AB 3500 Genetic Analyzer       |
| AB 3500xL Genetic Analyzer     |
| AB 3730 Genetic Analyzer       |
| AB 3730xL Genetic Analyzer     |
| AB 5500 Genetic Analyzer       |
| AB 5500xl Genetic Analyzer     |
| AB 5500xl-W Genetic Analysis System |
| BGISEQ-50                      |
| BGISEQ-500                     |
| DNBSEQ-G400                    |
| DNBSEQ-G400 FAST               |
| DNBSEQ-G50                     |
| DNBSEQ-T7                      |
| Element AVITI                  |
| FASTASeq 300                   |
| GENIUS                         |
| GS111                          |
| Genapsys Sequencer             |
| GenoCare 1600                  |
| GenoLab M                      |
| GridION                        |
| Helicos HeliScope              |
| HiSeq X Five                   |
| HiSeq X Ten                    |
| Illumina Genome Analyzer       |
| Illumina Genome Analyzer II    |
| Illumina Genome Analyzer IIx   |
| Illumina HiScanSQ              |
| Illumina HiSeq 1000            |
| Illumina HiSeq 1500            |
| Illumina HiSeq 2000            |
| Illumina HiSeq 2500            |
| Illumina HiSeq 3000            |
| Illumina HiSeq 4000            |
| Illumina HiSeq X               |
| Illumina MiSeq                 |
| Illumina MiniSeq               |
| Illumina NovaSeq 6000          |
| Illumina NovaSeq X             |
| Illumina iSeq 100              |
| Ion GeneStudio S5              |
| Ion GeneStudio S5 Plus         |
| Ion GeneStudio S5 Prime        |
| Ion Torrent Genexus            |
| Ion Torrent PGM                |
| Ion Torrent Proton             |
| Ion Torrent S5                 |
| Ion Torrent S5 XL              |
| MGISEQ-2000RS                  |
| MinION                         |
| NextSeq 1000                   |
| NextSeq 2000                   |
| NextSeq 500                    |
| NextSeq 550                    |
| Onso                           |
| PacBio RS                      |
| PacBio RS II                   |
| PromethION                     |
| Revio                          |
| Sentosa SQ301                  |
| Sequel                         |
| Sequel II                      |
| Sequel IIe                     |
| Tapestri                       |
| UG 100                         |
| unspecified                    |


### library_source

| **Term** | **Description** |
|-------------|----------|
| GENOMIC | Genomic DNA (includes PCR products from genomic DNA). |
| GENOMIC SINGLE CELL | |
| TRANSCRIPTOMIC | Transcription products or non genomic DNA (EST, cDNA, RT-PCR, screened libraries). |
| TRANSCRIPTOMIC SINGLE CELL | |
| METAGENOMIC | Mixed material from metagenome. |
| METATRANSCRIPTOMIC | Transcription products from community targets |
| SYNTHETIC | Synthetic DNA. |
| VIRAL RNA | Viral RNA. |
| OTHER | Other, unspecified, or unknown library source material. |

### library_selection

| **Term**                         | **Description**                                                                                             |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| RANDOM                           | No Selection or Random selection                                                                            |
| PCR                              | Target enrichment via PCR                                                                                   |
| RANDOM PCR                       | Source material was selected by randomly generated primers.                                                 |
| RT-PCR                           | Target enrichment via RT-PCR                                                                                |
| HMPR                             | Hypo-methylated partial restriction digest                                                                  |
| MF                               | Methyl Filtrated                                                                                            |
| repeat fractionation             | Selection for less repetitive (and more gene-rich) sequence through Cot filtration (CF) or similar methods. |
| size fractionation               | Physical selection of size-appropriate targets.                                                             |
| MSLL                             | Methylation Spanning Linking Library                                                                        |
| cDNA                             | PolyA selection or enrichment for messenger RNA (mRNA); synonymize with PolyA                               |
| cDNA_randomPriming               | Random priming for cDNA library preparation.                                                                |
| cDNA_oligo_dT                    | Oligo-dT priming for cDNA library preparation.                                                              |
| PolyA                            | PolyA selection or enrichment for messenger RNA (mRNA); replaces cDNA enumeration.                          |
| Oligo-dT                         | Enrichment of messenger RNA (mRNA) by hybridization to Oligo-dT.                                            |
| Inverse rRNA                     | Depletion of ribosomal RNA by oligo hybridization.                                                          |
| Inverse rRNA selection           | Depletion of ribosomal RNA by inverse oligo hybridization.                                                  |
| ChIP                             | Chromatin immunoprecipitation                                                                               |
| ChIP-Seq                         | Chromatin immunoPrecipitation revealing binding sites of specific proteins using antibodies.                |
| MNase                            | Identifies well-positioned nucleosomes using Micrococcal Nuclease (MNase).                                 |
| DNase                            | DNase I endonuclease digestion and size selection reveals chromatin regions sensitive to DNase I.           |
| Hybrid Selection                 | Selection by hybridization in array or solution.                                                            |
| Reduced Representation           | Reproducible genomic subsets generated by restriction fragment size selection.                              |
| Restriction Digest               | DNA fractionation using restriction enzymes.                                                                |
| 5-methylcytidine antibody        | Selection of methylated DNA fragments using an antibody against 5-methylcytosine or 5-methylcytidine.       |
| MBD2 protein methyl-CpG binding domain | Enrichment by methyl-CpG binding domain.                                                              |
| CAGE                             | Cap-analysis gene expression.                                                                               |
| RACE                             | Rapid Amplification of cDNA Ends.                                                                           |
| MDA                              | Multiple Displacement Amplification, a non-PCR-based DNA amplification technique.                           |
| padlock probes capture method    | Targeted sequence capture protocol covering specific nonrepetitive genomic targets.                         |
| other                            | Other library enrichment, screening, or selection process.                                                 |
| unspecified                      | Library enrichment, screening, or selection is not specified.                                              |

### library_strategy

| **Library Strategy**           | **Description**                                                                                     |
|--------------------------------|-----------------------------------------------------------------------------------------------------|
| WGS                            | Whole Genome Sequencing - random sequencing of the whole genome (see pubmed 10731132 for details).   |
| WGA                            | Whole Genome Amplification followed by random sequencing (see pubmed 1631067, 8962113 for details). |
| WXS                            | Random sequencing of exonic regions selected from the genome (see pubmed 20111037 for details).     |
| RNA-Seq                        | Random sequencing of whole transcriptome, also known as Whole Transcriptome Shotgun Sequencing (WTSS) (see pubmed 18611170 for details). |
| ssRNA-seq                      | Strand-specific RNA sequencing.                                                                     |
| miRNA-Seq                      | Micro RNA sequencing strategy designed to capture post-transcriptional RNA elements (see pubmed 21787409 for details). |
| ncRNA-Seq                      | Capture of non-coding RNA types, including snRNA, snoRNA, siRNA, and piRNA.                        |
| FL-cDNA                        | Full-length sequencing of cDNA templates.                                                          |
| EST                            | Single-pass sequencing of cDNA templates.                                                          |
| Hi-C                           | Chromosome Conformation Capture technique with biotin-labeled nucleotide for deep sequencing.       |
| ATAC-seq                       | Assay for Transposase-Accessible Chromatin (ATAC) for studying genome-wide chromatin accessibility. |
| WCS                            | Random sequencing of a whole chromosome or other replicon isolated from a genome.                  |
| RAD-Seq                        |                                                                                                     |
| CLONE                          | Genomic clone-based (hierarchical) sequencing.                                                     |
| POOLCLONE                      | Shotgun of pooled clones (usually BACs and Fosmids).                                               |
| AMPLICON                       | Sequencing of overlapping or distinct PCR or RT-PCR products.                                       |
| CLONEEND                       | Clone end (5’, 3’, or both) sequencing.                                                            |
| FINISHING                      | Sequencing intended to finish (close) gaps in existing coverage.                                   |
| ChIP-Seq                       | Chromatin immunoPrecipitation revealing binding sites of specific proteins.                        |
| MNase-Seq                      | Identifies well-positioned nucleosomes using Micrococcal Nuclease (MNase).                        |
| Ribo-Seq                       | Ribosome profiling to determine which mRNAs are being actively translated.                         |
| DNase-Hypersensitivity         | Sequencing of hypersensitive sites, open chromatin segments more readily cleaved by DNaseI.        |
| Bisulfite-Seq                  | Sequencing following bisulfite treatment to analyze DNA methylation (MethylC-seq).                |
| CTS                            | Concatenated Tag Sequencing.                                                                       |
| MRE-Seq                        | Methylation-Sensitive Restriction Enzyme Sequencing.                                               |
| MeDIP-Seq                      | Methylated DNA Immunoprecipitation Sequencing.                                                    |
| MBD-Seq                        | Methyl CpG Binding Domain Sequencing.                                                             |
| Tn-Seq                         | Quantitatively determines bacterial gene fitness using transposon insertion sequencing.            |
| VALIDATION                     | Independent experiment to re-evaluate putative variants (CGHub special request).                  |
| FAIRE-seq                      | Formaldehyde Assisted Isolation of Regulatory Elements for open chromatin regions.                |
| SELEX                          | Systematic Evolution of Ligands by Exponential Enrichment.                                         |
| RIP-Seq                        | Direct sequencing of RNA immunoprecipitates (includes CLIP-Seq, HITS-CLIP, and PAR-CLIP).          |
| ChIA-PET                       | Direct sequencing of proximity-ligated chromatin immunoprecipitates.                              |
| Synthetic-Long-Read            | Binning and barcoding of large DNA fragments to facilitate assembly.                               |
| Targeted-Capture               | Enrichment of a targeted subset of loci.                                                          |
| Tethered Chromatin Conformation Capture |                                                                                           |
| OTHER                          | Library strategy not listed.                                                                      |



### library_layout
| **Term** | **Description** |
|-------------|----------|
| SINGLE | Single-end sequencing. |
| PAIRED | Paired-end sequencing. |

---

## 5. Common Formatting Issues
To avoid errors during submission, ensure:
- All fields are filled correctly.
- Dates are formatted as `YYYY-MM-DD`.
- Taxonomy IDs match those in the [NCBI Taxonomy Database](https://www.ncbi.nlm.nih.gov/taxonomy).

---


## 6. Frequently Asked Questions (FAQs)

### Q: What should I do if I don’t know the taxonomy ID?
A: Use the [NCBI Taxonomy Browser](https://www.ncbi.nlm.nih.gov/taxonomy) to find the correct ID.

### Q: What should I do with taxonomy ID for metagenomics studies??
A: Choose the correct ID from the list of [metagenomes](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=408169).

### Q: What should I put as taxonomy ID for negative control?
A: Empty values are not permitted. Use taxon ID `256318` and scientific name `metagenome`.

### Q: How do I handle missing collection dates?
A: If the exact date is unknown, provide an approximate year (e.g., `2024`).

### Q: Can I include additional metadata fields?
A: Yes, additional fields are welcome if they provide useful information about the sample.

---

## 7. Contact for Assistance
If you have any questions or need further assistance, please contact RCX-Bioinformatics facility at bioinformatics@recetox.muni.cz.

---

By following this tutorial, you can ensure that your sample tables meet the necessary requirements for bioinformatics processing and subsequential ENA submission. Thank you for your attention to detail!
