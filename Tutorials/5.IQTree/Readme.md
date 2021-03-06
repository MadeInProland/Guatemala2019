# Maximum-Likelihood Phylogenetic Inference

## **IQTREE** 

In this tutorial, we will analyse the butterfly dataset with one of the fastest maximum-likelihood based phylogenetic programs [IQ-TREE](http://www.iqtree.org) ([Nguyen et al. 2015](https://academic.oup.com/mbe/article/32/1/268/2925592)). IQ-TREE for Windows, MacOSX and Linux can be downloaded [here](http://www.iqtree.org/#download), you can install it on your personal computer (optional).

The quickest is to try out the IQ-TREE [web server](http://iqtree.cibiv.univie.ac.at/), where you only need to upload an alignment, choose the options and start the analysis.

**Command line instructions in case you want to run the analysis in the terminal**

iqtree -s file.phy -spp Partitions.txt -m MFP+MERGE -bb 1000 -arlt 1000

Notes:

`iqtree` funtion will call the executable.

`-s` will call the alignment.

`-spp` is your patition file.

`-m` MFP+MERGE: will search for the best evolutionary model and partitionning scheme for your partitions.

`-bb` will perfom Ultrafast Boostrap.

`-arlt` will perform the SH-aLRT test.

**Tree inference**

Tree Inference is one of the most frequently used features of IQ-TREE and allows users to carry out phylogenetic analysis on a multiple sequence alignment (MSA). In the most basic case, only a MSA file is required to submit the job. Without further input, IQ-TREE will run with the default parameters and auto-detect the sequence type as well as the best-fitting substitution model. Additionally, Ultrafast Bootstrap ([Hoang et al., 2018](https://academic.oup.com/mbe/article/35/2/518/4565479)) and the SH-aLRT branch test ([Guindon et al., 2010](https://academic.oup.com/sysbio/article/59/3/307/1702850)) will be performed.
You can either try out the web server with an example alignment by ticking the corresponding box or upload your own alignment file. By clicking on ‘Browse’ a dialog will open where you can select your MSA; the file formats Phylip, Fasta, Nexus, Clustal and MSF are supported.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut1.png" alt="IQTREE" width="600"></p>

For this practice upload your `3_ConCATenated.phy` alignment file as explained above, reduce the `#replicates:` to `100`, add your email address and click on **SUBMIT JOB** button. This will take some time! Go for a coffee :)

**Analysis Results**

In the tab Analysis Results you can monitor your jobs. With our example file, a run will only take a few seconds, depending on the server load. For your own alignments the CPU time limit is 24 hours. If you provided an email address when submitting the job, you will get an email once it is finished.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut3.png" alt="IQTREE" width="600"></p>

Once a job is finished, you can select it by checking the corresponding box and then downloading the selected jobs as a zip file. This zip file will contain the results of your run, including the Run Log and the Full Result which are also accessible in the webserver.

   Suffix	     Output File Explanation
- .iqtree	     Full result of the run, this is the main report file
- .log	       Run log
- .treefile	   Maximum likelihood tree in NEWICK format, can be visualized with treeviewer programs
- .svg	       Graphical tree representation in SVG format, done with ete view
- .pdf	       Graphical tree representation in PDF format, done with ete view
- .contree	   Consensus tree with assigned branch supports where branch lengths are optimized on the original alignment; printed if Ultrafast Bootstrap is selected
- .ckp.gz	    Checkpoint file; included if a job was stopped because of RAM/CPU limits.



## Extra!

**Model Selection**

IQ-TREE supports a wide range of substitution models for DNA, protein, codon, binary and morphological alignments. In case you do not know which model is appropriate for your data, IQ-TREE can automatically determine the best-fit model for your alignment. Use the Model Selection tab if you only want to find the best-fit model without doing tree reconstruction.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut2.png" alt="IQTREE" width="600"></p>

Like with Tree Inference, the only obligatory input is a multiple sequence alignment. You can either upload your own alignment file or use the example alignment to try out the web server and then submit the job.

This tutorial was retrieved from the [IQTREE Web-Server](http://www.iqtree.org/doc/Web-Server-Tutorial)
