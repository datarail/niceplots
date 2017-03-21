# niceplots: A collection of visualization tools

## Prerequisites

The `R` portion of the code uses a number of libraries, which can be installed via the following `R` command: `install.packages( c("optparse", "dplyr", "igraph", "sna", "network", "ggplot2", "ggrepel", "ggnetwork" ) )`

## Projecting a model onto its network context

Given a model encapsulated by a weight vector (such as that produced by a linear model), we can visualize its network context. To do so, you will need the following:

1. A network specified as a .sif file.
2. A tab-delimited two-column file that maps genes to their weights.
3. A list of "seed" genes to initialize the plot. This can be, for example, a subset of genes with the largest weights (in absolute value).

The script operates by finding a collection of shortest paths that links the seed genes and plots the corresponding subnetwork, colored by node weight and edge type.

For more infomation on how to run the script, use `Rscript netcontext.R -h` on the command line.
