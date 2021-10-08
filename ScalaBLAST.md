# __<span style="color:#D57500">ScalaBLAST</span>__
A high-performance multiprocessor implementation of the NCBI BLAST library.

### Description
ScalaBLAST supports all 5 primary program types (blastn, blastp, tblastn, tblastx, and blastx) and several output formats (pairwise, tabular, or XML). ScalaBLAST will run on most multiprocessor systems that have MPI installed, and can run over a wide variety of interconnects including infiniband, quadrics, and ethernet. ScalaBLAST is designed to run a large number of queries against either large or small databases. ScalaBLAST parallelizes the BLAST calculations by dynamically scheduling them across processors using a fault-resilient scheme.

### Publications
[ScalaBLAST 2.0: rapid and robust BLAST calculations on multiprocessor systems](https://pubmed.ncbi.nlm.nih.gov/23361326/) [PMCID PMC3597145](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3597145/)

### Downloads
* [ScalaBLAST source](resources/scalablast_source.tar.gz)
* [ScalaBLAST Readme](resources/ScalaBLAST_Readme.txt)

#### Software Instructions
After downloading, untar the scalablast_source.tar.gz file, then follow the directions in the README for compiling and running ScalaBLAST.

### Acknowledgment

All publications that utilize this software should provide appropriate acknowledgement to PNNL and the publication. However, if the software is extended or modified, then any subsequent publications should include a more extensive statement, as shown in the Readme file for the given application or on the website that more fully describes the application.

### Disclaimer

These programs are primarily designed to run on Windows machines. Please use them at your own risk. This material was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor the United States Department of Energy, nor Battelle, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness or any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights.

Portions of this research were supported by the NIH National Center for Research Resources (Grant RR018522), the W.R. Wiley Environmental Molecular Science Laboratory (a national scientific user facility sponsored by the U.S. Department of Energy's Office of Biological and Environmental Research and located at PNNL), and the National Institute of Allergy and Infectious Diseases (NIH/DHHS through interagency agreement Y1-AI-4894-01). PNNL is operated by Battelle Memorial Institute for the U.S. Department of Energy under contract DE-AC05-76RL0 1830.

We would like your feedback about the usefulness of the tools and information provided by the Resource. Your suggestions on how to increase their value to you will be appreciated. Please e-mail any comments to proteomics@pnl.gov
