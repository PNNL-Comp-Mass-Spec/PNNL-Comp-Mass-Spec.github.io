# __<span style="color:#D57500">MZRefinery</span>__
MZRefinery is a software tool for correcting systematic mass error biases in mass spectrometry data files. The software uses confident peptide spectrum matches from MSGF+ to evaluate three different calibration methods, then chooses the optimal transform function to remove systematic bias, typically resulting in a mass measurement error histogram centered at 0 ppm. MzRefinery is part of the ProteoWizard package (in the msconvert.exe tool) and it thus can read and write a wide variety of file formats.

Download ProteoWizard from [http://proteowizard.sourceforge.net/downloads.shtml](http://proteowizard.sourceforge.net/downloads.shtml)

See below for a command line utility for generating plots of the mass measurement errors before and after correction.

For more information on the algorithms employed by mzRefinery, see also [http://www.ncbi.nlm.nih.gov/pubmed/26243018](http://www.ncbi.nlm.nih.gov/pubmed/26243018)

### Downloads
* [PPM Error Charter Program](https://github.com/PNNL-Comp-Mass-Spec/PPMErrorCharter/releases/latest)
* [PPM Error Charter Source code on GitHub](https://github.com/PNNL-Comp-Mass-Spec/PPMErrorCharter)

#### Software Instructions
The following is a typical workflow for using mzRefinery

1. Create a centroided .mzML file
  * `MSConvert.exe C:\WorkDir\DatasetName_2016-09-28.raw --filter "peakPicking true 1-" --mzML --32  -o C:\WorkDir`

2. Search the .mzML file using MSGF+ and a fully tryptic search and no dynamic mods (do include alkylation of cysteine if applicable):
  * `java.exe  -Xmx1500M -jar MSGFPlus.jar -s DatasetName_2016-09-28.mzML -o DatasetName_2016-09-28_msgfplus.mzid -d C:\FASTA\ID_003456_9B916A8B.fasta  -t 50ppm -m 0 -inst 3 -e 1 -ti -1,2 -ntt 2 -tda 1 -minLength 6 -maxLength 50 -n 1 -thread 7 -mod MSGFDB_Mods.txt -minNumPeaks 5 -addFeatures 1`

3. Run mzRefinery
  * `msconvert.exe C:\WorkDir\DatasetName_2016-09-28.mzML --outfile DatasetName_2016-09-28_FIXED.mzML --filter "mzRefiner C:\WorkDir\DatasetName_2016-09-28_msgfplus.mzid thresholdValue=-1e-10 thresholdStep=10 maxSteps=2" --32 --mzML`

4. Visualize the results from MzRefinery:
  * `PPMErrorCharter.exe C:\WorkDir\DatasetName_2016-09-28_msgfplus.mzid 1E-10`

5. Run MSGF+ again, this time using your longer search, for example partially tryptic or non-tryptic, plus any dynamic mods.
  * `java.exe  -Xmx4000M -jar MSGFPlus.jar -s DatasetName_2016-09-28.mzML -o DatasetName_2016-09-28_msgfplus.mzid -d C:\FASTA\ID_003456_9B916A8B.fasta  -t 10ppm -m 0 -inst 3 -e 1 -ti -1,1 -ntt 1 -tda 1 -minLength 6 -maxLength 50 -minCharge 2 -maxCharge 5 -n 1 -thread 8 -mod MSGFDB_Mods.txt -minNumPeaks 5 -addFeatures 1`
  * `java.exe  -Xmx2000M -XX:+UseConcMarkSweepGC -cp MSGFPlus.jar edu.ucsd.msjava.ui.MzIDToTsv -i C:\WorkDir\DatasetName_2016-09-28_msgfplus.mzid -o C:\WorkDir\DatasetName_2016-09-28_msgfdb.tsv -showQValue 1 -showDecoy 1 -unroll 1`

### Acknowledgment

All publications that utilize this software should provide appropriate acknowledgement to PNNL and the appropriate publication. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

### Disclaimer

These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
