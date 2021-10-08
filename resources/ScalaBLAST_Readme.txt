Building Scalablast.
___________________

1. Untar the scalablast tar ball into the directory you wish to install in.

2. To build the serial version  of scalablast use the following commands.
  
    First connect to the directory you unpacked the tar ball into.

    Then set the environment variable CC to be the name of your c compiler
    (e.g. icc, gcc, pathcc, etc) according to your shell ie.
	
    setenv CC icc

    Then run the configure script:

    ./configure

    Finally build the Scalablastall serial executable.

    make

3. To build the parallel version if you first built the serial version
   move the executable to a file with a different name, and then do

   make real_clean

   in the top level directory (where you unpacked the tarball to).

   Otherwise from the top level directory, set the environment variable
   CC to be "mpicc" according to your shell:

   setenv CC mpicc

   Then run the configure script.

   ./configure

   And then build the parallel executable, Scalablastall:

   make


   This will build the Scalablastall executable.


Running SCALABLAST:
___________________

Scalablast is an MPI based code so to run it you must launch an mpi job.

This usually has the flavor of


<mpi_exec> -N <number_of_nodes> -n <number_of_cores> ./Scalablastall <arguments_to_blastall>

the <mpi_exec> is the name of your command to launch an MPI executable.
Frequently it will be "mpi_run" or "mpi_exec" but may be as exotic as
"srun --mpi=none". The -N and -n arguments are dependent the flavor of
your <mpi_exec>, some may only have one or the other or some other method
of specifying the number of resources you will run with.

For the <arguments_to_blastall> part one uses the normal blastall argument 
sequence with one restriction. The input and data base file names 
(-i and -d option values) must be different. When running  a database 
against itself, you want to have a symbolic link or copy of the reference 
database to use for the query database name. 

In addition to the normal BLOWSUM62 file, the reference database file and 
the query files for blastall, Scalablastall requires an auxillary input file 
named sb_params.in. 
The BLOSUM62 file and the sb_params.in file must be present in 
the directory you run the Scalablastall executable from.
The BLOSUM62 file is found in the PAR_ncbi/ncbi/data directory in the directory
into which you untarred the tar ball. 
Also in the directory where the tarball was extracted is an example
sb_params.infile

The sb_params.infile is a list of keyword value pairs 
(1 pair per line, with the value separated by 1 or more spaces from the keyword) 
that allow for runtime control of SCALABLAST.

The keywords and their default values followed by a brief description are given below.

   Keword         Default value Description:
LOCAL_DIR           /scratch/   This is the root name of a writable directory
				local to the node. The input reference and 
	                        query files are copied to this directory.


GLOBAL_DIR          ./          This is the root name of a globally visible 
				directory where the input files (reference 
	                        and query fasta files) are expected to be 
				found.

OUTPUT_DIR          ./          The directory into which output files 
	                        (1 per client) should be placed.
	                        
	 
CORES_PER_NODE      8           This is used in the auto-sizing of
                                memory usage for fasta and seqannot buffers.
	                        Normally the same as DISK_GROUP_SIZE, unless
                                you are using globally visible input files.
	                        It should be set to the number of cores per
	                        node that you will actually run on. 
		                Default value is 8 for parallel version. 
			        Default value is 1 for serial version. 
	                        Be careful not to set > 1 when running
	                        serial code.

DISK_GROUP_SIZE     8           This value needs to be number cores per node 
				being used. For example, if your mpiexec 
				is set to run on only 7 of your eight cores 
				per node you should set this to seven (not 8). 
	                        In moving the files to a local disk, 
				only every DISK_GROUP_SIZE'th mpi rank 
				process is involved (starting at 0).
	                               

TASK_GROUP_SIZE     0           Number of tasks (including 1 for the 
				submanager) in a task group. Setting to zero 
				lets this be set at runtime based on the size
				of the reference database. Task group size is 
				taken to be 1 + number of chunks of 
				reference_data buffer size it takes to contain
				the reference data or number of processes - 2, 
				which ever is smaller).

FIRST_SUBMANAGER    8           MPI rank of the first submanager process. 
	                        This allows the master to run all by itself on 
	                        a node so as to evenly map task groups to 
	                        whole numbers of nodes.
                                It must be >= 1 as manager rank is always 0.
                                       

Termination: 
____________

Scalablast frequently ends with MPI errors in the log/error files. 
this is expected as we use exit instead of calling MPI_Finalize due to 
experiences with calls to MPI_Finalize causing communication failure at 
large scale with some MPI flavors.  Indication of a successful run is the 
"All tasks completed" message in the *.log.0 log file. 
If you see segmentation violations with out the "All tasks completed" message,
it probably is due to not enough memory per core - try running fewer cores 
per node.
