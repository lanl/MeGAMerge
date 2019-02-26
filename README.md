MeGAMerge
=========

MeGAMerge (A tool to merge assembled contigs, long reads from metagenomic sequencing runs)

MeGAMerge is a perl tool to accept any number of files containing assembled contigs of any length in Multi-FASTA format, and produce an improved assembly based on OLC based assembly.  All overlap parameters (Minimum Overlap Length, Identity, etc) are user-declarable at runtime. 

Requirements:

Must have the following tools installed and in PATH, or added to $binpath in the tool:

-Newbler (specifically runAssembly)

-Minimus2 (part of AMOS, requires MUMMer)

Usage:

MeGAMerge-1.0.pl [options] output_directory <list of fastas>

Options:

-overlap=NN            Parameter for minimum overlap length in minimus2/Newbler (default = 80)

-minID=NN              Minimum % identity for overlap in minimus2/Newlber (default 98)

-conserr=NN            Maximum conservation error for minimus2 (default 0.06)

-cpu=NN                Number of CPU for Newbler (default 4)

-bindir=directory      Directory containing MUMmer executables and AMOS executables

-newblerdir=direcoty   Directory for newbler executable (runAssembly)

-o=outfile             Name of final file to output in output_directory (default MergedContigs.fasta)

-minLen=NN             Minimum length to include in newbler assemblies (default 150)

-minIncludeLen=NN      Minimum length to include in minimus assembly (default, 200)

-d=1                   Turns on debug information

-single_genome=1       Runs assuming single genome, reducing auto-options
                       (one newbler run, exclude fewer contigs, overrides -minLen and minIncludeLen)
                       

-------------
COPYRIGHT 
-------------

Copyright (2013).  Triad National Security, LLC. All rights reserved.
 
This program was produced under U.S. Government contract 89233218CNA000001 for Los Alamos National 
Laboratory (LANL), which is operated by Triad National Security, LLC for the U.S. Department of Energy/National 
Nuclear Security Administration.
 
All rights in the program are reserved by Triad National Security, LLC, and the U.S. Department of Energy/National 
Nuclear Security Administration. The Government is granted for itself and others acting on its behalf a nonexclusive, 
paid-up, irrevocable worldwide license in this material to reproduce, prepare derivative works, distribute copies to 
the public, perform publicly and display publicly, and to permit others to do so.

This is open source software; you can redistribute it and/or modify it under the terms of the GPLv3 License. If software 
is modified to produce derivative works, such modified software should be clearly marked, so as not to confuse it with 
the version available from LANL. Full text of the [GPLv3 License](https://github.com/losalamos/MeGAMerge/blob/master/LICENSE) can be found in the License file in the main development 
branch of the repository.
