# __<span style="color:#D57500">Omics@PNNL Software</span>__

All of our open source software is posted at our group's [GitHub Repository](https://github.com/PNNL-Comp-Mass-Spec).

Some quick links:
* [Command Line Application Help](#cmdlineapphelp)
* [Molecular Weight Calculator](#molwtcalc)
* [PNNL PreProcessor](#pnnlpreprocessor)
* [Thermo Raw File Reader](#rawfilereader)
* [Venn Diagram Plotter](#venndiagram)

#### Software Category: Featured Tools
* __[DeconTools (Decon2LS)](https://pnnl-comp-mass-spec.github.io/DeconTools/)__ <br>
  Used to de-isotope mass spectra and to detect features from mass spectrometry data using observed isotopic signatures.

* __[DtaRefinery](https://pnnl-comp-mass-spec.github.io/DtaRefinery/)__ <br>
  Reduces mass measurement errors for parent ions of tandem MS/MS data by modeling systematic errors based on putative peptide identifications. This information is used to subtract out errors from parent ion protonated masses.

* __[InfernoRDN](https://pnnl-comp-mass-spec.github.io/InfernoRDN/)__ <br>
  InfernoRDN can perform various downstream data analysis, data reduction, and data comparison tasks including normalization, hypothesis testing, clustering, and heatmap generation.

* __[MultiAlign](https://pnnl-comp-mass-spec.github.io/MultiAlign/)__ <br>
  Aligns multiple LC-MS datasets to one another after which LC-MS features can be matched to a database of peptides (typically an AMT tag database)

* __[VIPER](https://pnnl-comp-mass-spec.github.io/VIPER/)__ <br>
  VIPER (Visual Inspection of Peak/Elution Relationships) can be used to visualize and characterize the features detected during LC-MS analyses.

#### Software Category: Data Analysis and Data Presentation Tools
* __[Active Data Canvas](https://github.com/ActiveDataBio/Adbio)__ <br>
  Active Data Canvas is a web-based visual analytic tool to visualize data matrix (expression matrix) and for users to interactively identify the structured domain knowledges (e.g., pathways and other genesets) linked to a cluster.

  Active Data Canvas was hosted at ~~`https://adbio.pnnl.gov/bioviz`~~, but that was turned off due to lack of use. The source code is available at https://github.com/ActiveDataBio/Adbio

* __[LcMsSpectator](https://pnnl-comp-mass-spec.github.io/LCMS-Spectator/)__ <br>
  Windows graphical user interface tool for viewing LC-MS data and identifications.

* __[ListPOR](https://pnnl-comp-mass-spec.github.io/ListPOR/)__ <br>
  The ListPOR program (List Parser for Outlier Removal) can be used to read a file containing columns of grouped values and remove outlier values using Grubb's test.

* __[Protein Coverage Summarizer](https://pnnl-comp-mass-spec.github.io/protein-coverage-summarizer/)__ <br>
  The Protein Coverage Summarizer can be used to determine the percent of the residues in each protein sequence that have been identified.

* __[ScalaBLAST](ScalaBLAST)__ <br>
  A high-performance multiprocessor implementation of the NCBI BLAST library.

* __[Venn Diagram Plotter](https://pnnl-comp-mass-spec.github.io/Venn-Diagram-Plotter/)__ <a id="venndiagram"></a> <br>
  Draws correctly proportioned and positioned two and three circle Venn diagrams (aka Euler diagrams) whose colors can be customized and the diagrams copied to the clipboard or saved to disk.

* __[VIBE: Visual Integration for Bayesian Evaluation](VIBE)__ <br>
  The Visual Integration for Bayesian Evaluation (VIBE) software is a visualization tool that allows the user to observe classification accuracies at the class level and evaluate classification accuracies on any subset of available data types based on the posterior probability models defined for the individual and integrated data.

#### Software Category: Fasta File, Protein Sequence, or Protein Database Related tools
* __[Fasta File Splitter](https://pnnl-comp-mass-spec.github.io/Fasta-File-Splitter/)__ <br>
Console application that reads a protein FASTA file and splits it apart into a number of sections. Although the splitting is random, each section will have a nearly identical number of residues.

* __[Population Variation](https://pnnl-comp-mass-spec.github.io/PopulationVariationPlugin/)__ <br>
  A Population Variation plug-in for the [Skyline software program](https://skyline.ms/project/home/software/Skyline/begin.view) that can assist researchers in determining whether their target peptides have known mutations in the general human population.

* __[Protein Digestion Simulator](https://pnnl-comp-mass-spec.github.io/Protein-Digestion-Simulator/)__ <br>
  The Protein Digestion Simulator can be used to read a text file containing protein or peptide sequences ([FASTA](http://en.wikipedia.org/wiki/FASTA_format) format or delimited text) then output the data to a tab-delimited file.

* __[Protein Sequence Motif Extractor](https://pnnl-comp-mass-spec.github.io/Protein-Sequence-Motif-Extractor/)__ <br>
  The Protein Sequence Motif Extractor reads a fasta file or tab delimited file containing protein sequences, then looks for the specified motif in each protein sequence.

* __[Uniprot DAT File Parser](https://pnnl-comp-mass-spec.github.io/Uniprot-DAT-File-Parser/)__ <br>
  The Uniprot DAT File Parser can read a Uniprot .Dat file and parse out the information for each entry, creating a series of tab delimited text files or creating a FASTA file.

#### Software Category: MS Analysis Tools
* __[Formultitude](https://pnnl-comp-mass-spec.github.io/Formultitude/)__ <br>
  Formultitude (previously named Formularity) is software for assignment of low weight molecular formulas to peaks in high-resolution mass spectra.

* __[MTDB Creator](https://pnnl-comp-mass-spec.github.io/MTDB-Creator/)__ <br>
  This software can be used to generate an Accurate Mass and Time tag database from local MS/MS search engine results from MSGF+, X!Tandem, or SEQUEST.  It can create the database in two formats:

  * Microsoft Access (.mdb file), compatible with VIPER
  * SQLite (.mtdb), compatible with MultiAlign

#### Software Category: MS/MS Analysis Tools
* __[DeconMSn](https://pnnl-comp-mass-spec.github.io/DeconMSn/)__ <br>
  DeconMSn creates spectrum files for tandem mass spectrometry data.

* __[GlyQ-IQ](https://pnnl-comp-mass-spec.github.io/GlyQ-IQ/)__ <br>
  GlyQ-IQ is software that performs a targeted, chromatographic centric search of mass spectral data for glycans. The software uses a list of glycan targets to search for expected features in MS1 spectra. Features are characterized by monoisotopic mass, elution time, and isotopic fit score.  Features are annotated by glycan family relationships and in-source fragmentation patterns.

* __[MASIC](https://pnnl-comp-mass-spec.github.io/MASIC/)__ <br>
MASIC (MS/MS Automated Selected Ion Chromatogram generator) Generates selected ion chromatograms (SICs) for all of the parent ions chosen for fragmentation in an LC-MS/MS analysis.

* __[MASIC Results Merger](https://pnnl-comp-mass-spec.github.io/MASIC-Results-Merger/)__ <br>
  Reads the contents of a tab-delimited peptide hit results file (e.g. from Sequest, XTandem, Inspect, or MSGF+) and merges that information with the corresponding MASIC results files, appending the relevant MASIC stats for each peptide hit result.

* __[MS-GF+](https://MSGFPlus.github.io/)__ <br>
  MS-GF+ (aka MSGF+ or MSGFPlus) performs peptide identification by scoring MS/MS spectra against peptides derived from a protein sequence database. It supports the HUPO PSI standard input file (mzML) and saves results in the mzIdentML format, though results can easily be transformed to TSV. ProteomeXchange supports Complete data submissions using MS-GF+ search results.

* __[MSGFPlus/MASIC Data Processing Toolbox](https://pnnl-comp-mass-spec.github.io/MSGFPlus_MASIC_Toolbox/)__ <br>
  DataProcessing toolbox for running MSGF+ and MASIC, then merging the results. Uses Windows batch files to automate the process for a folder of Thermo .Raw files

* __[MSPathFinder](https://pnnl-comp-mass-spec.github.io/Informed-Proteomics/)__ <br>
  MSPathFinder is a database search engine for top-down proteomics, part of the Informed Proteomics package, which includes PbfGen, ProMex, MSPathfinderT, and ProMexAlign.

* __[MZRefinery](https://pnnl-comp-mass-spec.github.io/MzRefinery)__ <br>
  MZRefinery is a software tool for correcting systematic mass error biases in mass spectrometry data files. The software uses confident peptide spectrum matches from MSGF+ to evaluate three different calibration methods, then chooses the optimal transform function to remove systematic bias, typically resulting in a mass measurement error histogram centered at 0 ppm. MzRefinery is part of the ProteoWizard package (in the msconvert.exe tool) and it thus can read and write a wide variety of file formats.

* __[Peptide Hit Results Processor (PHRP)](https://pnnl-comp-mass-spec.github.io/PHRP/)__ <br>
  Converts a MSGF+ TSV file, X!Tandem results file (XML format), or a SEQUEST Synopsis/First Hits file to a series of tab-delimited text files summarizing the results.

#### Software Category: MS Data File Utilities
* __[FlexibleFileSortUtility](https://pnnl-comp-mass-spec.github.io/FlexibleFileSortUtility/)__ <br>
  The Flexible File Sort Utility is a command line application that sorts a text file alphabetically (forward or reverse). <br>
  It supports both in-memory sorts for smaller files and use of temporary swap files for large files. <br>
  It can alternatively sort on a column in a tab-delimited or comma-separated file. <br>
  The column sort mode also supports numeric sorting.

* __[LC-IMS-MS-Feature-Finder](https://pnnl-comp-mass-spec.github.io/LC-IMS-MS-Feature-Finder/)__ <br>
  Finds LC-IMS-MS features using deisotoped features from DeconTools

* __[MS File Info Scanner](https://pnnl-comp-mass-spec.github.io/MS-File-Info-Scanner/)__ <br>
  The MS File Info Scanner can be used to scan a series of MS data files (or data folders) and extract the acquisition start and end times, number of spectra, and the total size of the data.

* __[OBO Data Converter](https://pnnl-comp-mass-spec.github.io/OBO-Data-Converter/)__ <br>
  Utility for converting ontology OBO files to a tab-delimited text file

* __[PNNL PreProcessor](https://pnnl-comp-mass-spec.github.io/PNNL-PreProcessor/)__ <a id="pnnlpreprocessor"></a> <br>
  Ion mobility-mass spectrometry (IM-MS) provides an increasingly popular platform for analyzing complex samples due to its separation power and ability to differentiate structural isomers, which are difficult to resolve using conventional LC-MS systems. Here we provide a software tool with various algorithms and utilities to improve workflows using this technology: data compression and interpolation, ion mobility demultiplexing, multidimensional smoothing, noise filtering by low intensity threshold and spike removal, saturation repair and metadata export.

* __[Thermo Raw File Reader](https://pnnl-comp-mass-spec.github.io/Thermo-Raw-File-Reader/)__ <a id="rawfilereader"></a> <br>
  The Thermo Raw File Reader is a .NET DLL that demonstrates how to read Thermo-Finnigan .Raw files using Thermo's RawFileReader.

#### Software Category: Mass Spectrometry Auxiliary Tools
* __[Molecular Weight Calculator](https://pnnl-comp-mass-spec.github.io/Molecular-Weight-Calculator-VB6/)__ <a id="molwtcalc"></a> <br>
  Calculates the molecular weight and percent composition of chemical formulas and amino acids.

* __[Molecular Weight Calculator - .NET DLL Version](https://pnnl-comp-mass-spec.github.io/Molecular-Weight-Calculator-DLL/)__ <br>
  VB.NET DLL version of the Molecular Weight Calculator, supporting a range of molecular weight calculations for both chemical formulas and amino acids.

#### Software Category: Tutorials
* __[Command Line Application Help](CmdLineHelp)__ <a id="cmdlineapphelp"></a> <br>
  This topic provides a basic introduction to using software tools that do not have a graphical user interface (GUI) and instead can only be used at the Windows Command Prompt.

#### Retired Tools:
* __[DanteR](DanteR)__ <br>
  DanteR is an entirely R-based program that provides a graphical front-end for common data analysis tasks in "omics", with an emphasis on proteomics. It is the successor to DAnTE, providing all of the previous features plus new functionality, including the imputation algorithm described in "[A statistical framework for protein quantitation in bottom-up MS-based proteomics.](https://www.ncbi.nlm.nih.gov/pubmed/19535538)" by Karpievitch and Dabney (DOI 10.1093/bioinformatics/btp362).

  IMPORTANT: Development of this program is frozen since it has been superseded by InfernoRDN, available on the [InfernoRDN page](https://pnnl-comp-mass-spec.github.io/InfernoRDN/) or [on GitHub](https://github.com/PNNL-Comp-Mass-Spec/InfernoRDN/releases).

  This version is still made available because it implements the imputation algorithm described above (see "Model Based Filter/Impute/ANOVA" under the Statistics menu).

* __[ICR-2LS](ICR-2LS)__ <br>
  Finds peaks in raw mass spectra. Capable of full waveform generation, automated mass spectra interpretation and database searching integration of FASTA or GenBank files.

* __[mPE-MMR](mPE-MMR)__ <br>
  mPE-MMR can be used to create a MGF file with refined parent ion masses and charges, which can lead to more accurate search results from MS/MS spectra. mPE-MMR (Multiplexed Post-Experiment Monoisotopic Mass Refinement) supports multiplexed MS/MS spectra, and consists of the following:

  * Multiplexing of precursor masses to assign multiple monoisotopic masses of cofragmented peptides to the corresponding multiplexed MS/MS spectra
  * Multiplexing of charge states to assign correct charges to the precursor ions of MS/MS spectra with no charge information
  * Mass correction for inaccurate monoisotopic peak picking.

  When combined with MS-GF+, a database search algorithm based on fragment mass difference, mPE-MMR effectively increases both sensitivity and accuracy in peptide identification from complex high-throughput proteomics data compared to conventional methods.

* __[PE-MMR](PE-MMR)__ <br>
  PE-MMR can be used to create a MGF file with refined parent ion masses and charges, which can lead to more accurate search results from MS/MS spectra.

* __[Concatenated DTA to Mascot Generic File (MGF) File Converter](CDtaToMgfConverter)__ <br>
    Command-line utility that reads in a _Dta.txt file and creates the equivalent Mascot Generic Format (MGF) file. _Dta.txt files are large text files that contain numerous .Dta files, all concatenated together.

* __[Concatenated Text File Splitter](CDtaTextFileSplitter)__ <br>
  The Concatenated Text File Splitter can be used to split apart the concatenated file to re-create the individual text files (creating one file per spectrum). This is necessary if you wish to re-search the data with SEQUEST (which reads individual .Dta files).

### Software Disclaimers
##### Acknowledgment
All publications that utilize this software should provide appropriate acknowledgement to PNNL and the appropriate publications and/or software repository. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

##### Disclaimer
These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
