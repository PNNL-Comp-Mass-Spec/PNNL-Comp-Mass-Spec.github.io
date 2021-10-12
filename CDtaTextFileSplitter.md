# __<span style="color:#D57500">Concatenated Text File Splitter</span>__
The Concatenated Text File Splitter can be used to split apart the concatenated file to re-create the individual text files (creating one file per spectrum). This is necessary if you wish to re-search the data with SEQUEST (which reads individual .Dta files).

### Description
When analyzing tandem mass spectral data files with SEQUEST or X!Tandem, we concatenate together separate spectra files (.Dta files) into a single file, whose name ends in _Dta.txt.

The result files produced by sequest are called .Out files. We also concatenate them together to form a single _Out.txt file. Again, the Concatenated Text File Splitter can be used to split apart the _Out.txt file to re-recreate the separate .Out files.

When creating the .dta or .out files, you can use the /F switch to filter the spectra and only extract spectra of interest. Alternatively, you can use the /T switch to create a new, filtered _dta.txt or _out.txt file, again, only containing the spectra of interest.

Note that this software is a command line application; it does not have a graphical user interface. Please see the [Command Line Application Help](CmdLineHelp) page for additional information on running this program at the Windows command prompt.

### Downloads
* [Installer](https://panomics.pnnl.gov/downloads/installers/ConcatenatedTextFileSplitter_Installer.zip)
* [Source Code](https://panomics.pnnl.gov/downloads/installers/ConcatenatedTextFileSplitter_SourceAndSupportingDLLs.zip)

#### Software Instructions
The following is an excerpt from an example _dta.txt file, which was created from a series of .Dta files. The Concatenated Text File Splitter program can parse this file, looking for the header lines, and create separate .Dta files for each section in the concatenated file. Note that the "scan=5563 cs=2" portion of the parent ion info line is a PNNL-specific add-on to .Dta files (see Matrix Science's [Data File Format](http://www.matrixscience.com/help/data_file_help.html#DTA) page for additional information). The Concatenated Text File Splitter will remove the "scan=5563 cs=2" text when creating individual .Dta files.

```
=================================== "QC_File_30Aug07_Owl_07-08-03.5563.5563.2.dta" ==================================
998.62505 2   scan=5563 cs=2
227.045 7973.5
303.314 1632.7
***********.8
386.744 2049
455.543 1544.5
467.954 1080.8
477.865 1176.2
480.34 997.3
481.377 1102.3
489.778 1502.3
544.336 1376.8
673.386 5770.5
772.459 45675.8
773.538 5369.5
852.318 2238.1

>=================================== "QC_File_30Aug07_Owl_07-08-03.5564.5564.1.dta" ==================================
1057.584 1   scan=5564 cs=1
509.314 816.6
527.214 831.2
640.366 1643.2
741.457 758.5
759.412 8421.5
790.407 656.2
807.373 1387.5
808.428 1746.3
825.351 3142.8
872.401 829.8
903.447 1003.2
904.444 653.1
920.483 1054.7
921.478 3488.3
938.483 4280
1039.495 2698.9

=================================== "QC_File_30Aug07_Owl_07-08-03.5565.5565.2.dta" ==================================
.
```

### Acknowledgment

All publications that utilize this software should provide appropriate acknowledgement to PNNL. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

### Disclaimer

These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
