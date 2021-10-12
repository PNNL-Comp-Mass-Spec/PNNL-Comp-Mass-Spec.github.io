# __<span style="color:#D57500">mPE-MMR</span>__
mPE-MMR can be used to create a MGF file with refined parent ion masses and charges, which can lead to more accurate search results from MS/MS spectra. mPE-MMR (Multiplexed Post-Experiment Monoisotopic Mass Refinement) supports multiplexed MS/MS spectra, and consists of the following:

* Multiplexing of precursor masses to assign multiple monoisotopic masses of cofragmented peptides to the corresponding multiplexed MS/MS spectra
* Multiplexing of charge states to assign correct charges to the precursor ions of MS/MS spectra with no charge information
* Mass correction for inaccurate monoisotopic peak picking.

When combined with MS-GF+, a database search algorithm based on fragment mass difference, mPE-MMR effectively increases both sensitivity and accuracy in peptide identification from complex high-throughput proteomics data compared to conventional methods.

### Description
The mPE-MMR method is an integrated approach that combines three previously reported methods of treating MS/MS data for precursor mass refinement. It increases sensitivity in peptide identification and provides increased accuracy. The mPE-MMR (SA) software requires the following:

* Thermo .Raw file for your dataset of interest
* MSConvert.exe, available either as part of the [TPP](http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP) or from [ProteoWizard](http://proteowizard.sourceforge.net/)
* MzXML2Search.exe, available as part of the TPP ([http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP](http://tools.proteomecenter.org/wiki/index.php?title=Software:TPP))

Given these files, you can run mPE-MMR (SA) via the command line. The following automated steps will be performed:

* Rapid.exe will process the .Raw file to deisotope the data, creating _isos.csv and _scans.csv files
* MSConvert.exe will convert the .Raw file to a .mzXML file
* MzXML2Search.exe will convert the .mzXML file to a .mgf file
* mPE-MMR's UMCCreator will create LC-MS Features (UMCs) using the _scans.csv and _isos.csv files
* mPE-MMR will use the information from the UMCCreator result to filter the spectra in the MGF file, while also refining the parent ion mass. A new .mgf file named OriginalName_PEMMR.mgf will be created.

See the User Guide ([mPEMMR_UserGuide_EN.pdf](resources/mPEMMR_UserGuide_EN.pdf)) for detailed information on how to configure and run mPE-MMR.

Software developed at the Laboratory of Gaseous Ion Chemistry in the Department of Chemistry at Korea University.

Reference: "Multiplexed Post-Experimental Monoisotopic Mass Refinement (mPE-MMR) to Increase Sensitivity and Accuracy in Peptide Identifications from Tandem Mass Spectra of Cofragmentation." Madar IH, Ko SI, Kim H, Mun DG, Kim S, Smith RD, Lee SW. Anal Chem. 2017 Jan 17; 89(2): 1244-1253. doi: 10.1021/acs.analchem.6b03874
(PubMed ID [27966901](https://www.ncbi.nlm.nih.gov/pubmed/27966901))

### Downloads
* [mPE-MMR Program](https://panomics.pnnl.gov/downloads/installers/mPEMMR_Program.zip)
* [mPEMMR_UserGuide_EN.pdf](resources/mPEMMR_UserGuide_EN.pdf) (or [here](https://panomics.pnnl.gov/downloads/installers/mPEMMR_UserGuide_EN.pdf))

### Acknowledgment

All publications that utilize this software should provide appropriate acknowledgement to PNNL and the mPE-MMR publication. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

### Disclaimer

These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
