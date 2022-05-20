# MicrobiomeProteins
Software and data for working with Microbiome Proteins - MicrobiomeCourse2022

## Introduction
In class on 5/24/2022, we are going to explore some of the proteins (or gene products, depending on your frame of reference ;) ) that have come out of our initial explorations of the MicroPD 16S dataset, the metabolomics dataset, [this](https://bmcbiol.biomedcentral.com/articles/10.1186/s12915-020-00876-3) paper from the El Aidy lab that looks at deamination of L-DOPA, and [this](https://www.science.org/doi/10.1126/science.aau6323) paper from the Balskus and Turnbaugh Labs that looks at the interspecies metabolism of L-DOPA to m-tyramine.

I will be introducing tools that are available as web servers, that use a commmand line, scripts, the terminal, that can communicate with R, and combinations of all options. My hope is to introduce you to the different tool options and then you can select the version of the tool that suits your specific scientific question, either a simple web tool to see the domains of a representative protein or a more computationally intensive question that requires scripts for automation.

## Software to Download and Check Prior to Class
Please go to [this](https://cytoscape.org/download.html) site and download Cytoscape 3.9.1 (274 MB for MacOSX, not sure for Windows). Double click on the installer or open the .exe file and follow the installer prompts. Feel free to open one of the example sessions to get a feel for how the software works, how to move around the network, what the node and edge tables are, and how to style the network in useful ways.

Please go to [this](https://www.cgl.ucsf.edu/chimerax/download.html) site and download UCSF ChimeraX 1.3. Chimera is used to visualize models of proteins that have been built by fitting amino acids into electron density. Similar to Cytoscape, feel free to get a feel for how to explore a protein by typing "open 1EMA" in the Command Line across the bottom of the application window followed by return or enter.

Open RStudio and run the following commands to ensure you are able to access these libraries:
```{r}
install.packages("BiocManager") # The package manager for Bioconductor
BiocManager::install("RCy3") # Talking to Cytoscape from R
library(RCy3)
```
```{r}
# If you are using a Mac, you can open Cytoscape with the following command:
system2('open', args=c('-a', 'Cytoscape.app'))

# If you are using a PC, try the command above or you can open Cytoscape like you would any other program.
```

Check that you are connected to Cytoscape
```{r}
cytoscapePing()
```


