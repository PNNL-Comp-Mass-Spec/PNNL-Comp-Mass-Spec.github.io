# __<span style="color:#D57500">DanteR</span>__
DanteR is an entirely R-based program that provides a graphical front-end for common data analysis tasks in "omics", with an emphasis on proteomics. It is the successor to DAnTE, providing all of the previous features plus new functionality, including the imputation algorithm described in "[A statistical framework for protein quantitation in bottom-up MS-based proteomics.](https://www.ncbi.nlm.nih.gov/pubmed/19535538)" by Karpievitch and Dabney (DOI 10.1093/bioinformatics/btp362).

IMPORTANT: Development of this program is frozen since it has been superseded by InfernoRDN, available on the [InfernoRDN page](https://pnnl-comp-mass-spec.github.io/InfernoRDN/) or [on GitHub](https://github.com/PNNL-Comp-Mass-Spec/InfernoRDN/releases).

This version is still made available because it implements the imputation algorithm described above (see "Model Based Filter/Impute/ANOVA" under the Statistics menu).

### Description
| <!-- empty --> | <!-- empty --> | <!-- empty --> | <!-- empty --> |
|---|---|---|---|
| __Supported file formats__ | Excel, Excel 2007, SQLite DB, Access, CSV, tab-delimited text | __Supported locales__ | US and European delimiters and decimals |
| __Data types__ | __Crosstabulated numeric data__ (peptide intensity, expression ratios, spectral counts, gene expressions) | __Metadata types__ | __Row metadata__ (proteins, pathways, biological functions) <br /> __Column metadata/Factors__ (Experiment categories) |
| __Basic data operations__ | Merge, sort, filter, apply arbitrary R commands | __Metadata operations__ | Define row/column metadata, plot metadata linkages, create/apply aliases |
| __Preprocessing__ | Normalization via eigenvalues, linear regression, LOESS, quantiles | __Imputation__ | KNN, row means, model-based ANOVA, many others |
| __Peptide-to-protein rollup__ | Via medians, means or quantiles | __Parametric statistical operations__ | N-way ANOVA and robust ANOVA, two-factor protein-level ANOVA, Fisher test, model-based imputation/ANOVA |
| __Nonparametric statistics__ | Shapiro-Wilks, Kruskal-Wallis | __Other statistical operations__ | Interactive volcano plots, significance summaries |
| __Plotting__ | Matrix/Scatterplot, 3D plots using RGL, histogram, QQ, boxplots, ellipses, Venn diagram | __Data exploration__ | K-means and hierarchical clustering, pattern search, 2D and 3D PCA plot, dynamic metadata-linked row plotting |
| __Addons__ | Users can include their own R-based addons to the program | __Addon dialogs__ | A simple markup language allows dialogs to be created with no GUI experience |

### Related Publications
* [DAnTE: a statistical tool for quantitative analysis of -omics data.](https://pubmed.ncbi.nlm.nih.gov/18453552/)
* [A statistical framework for protein quantitation in bottom-up MS-based proteomics.](https://pubmed.ncbi.nlm.nih.gov/19535538/)

### Downloads
* [Installer that includes DanteR, GTK+, and R](https://panomics.pnnl.gov/downloads/installers/DanteR_Installer.zip)

#### Software Instructions
1. Download DanteR_Installer.zip , unzip, and run DanteR_Setup.exe
  * This installs DanteR, GTK+, and R
  * This will not affect any other copy of R you might have installed
2. After the installer finishes, start DanteR using the link in the DanteR folder in the start menu, or via the desktop link
  * R Console will appear
  * After ~15 seconds, commands will appear in R Console and the DanteR window should appear
3. See the PDF files for usage tips

### Acknowledgment

All publications that utilize this software should provide appropriate acknowledgement to PNNL and the DanteR publication. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

### Disclaimer

These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
