**Overview**

 This directory contains scripts and datasets used for setting up the experiments in the ECAN system.
 Misgana's original experiment and documentation can be found at [Here](https://github.com/misgeatgit/opencog/tree/experiment/experiments/insect-poison).

**Objective**

 The major goals of these experiments are to validate that the ECAN system is working and determine whether implementing hebbian updating based upon past STI's (Matt's Equation) results in better performance of the system.

**Installing and Running the experiment**

**Step 1** - Create a parent directory OPENCOG (or any name you prefer) for all opencog repositories.

``` cd ~ ```

``` mkdir OPENCOG/ ```

``` cd OPENCOG ```

**Step 2** - clone cogutils ( ``` cd ~/OPENCOG && git clone https://github.com/aro-ai-robots/cogutil ``` ) and do the following:

``` cd ~/OPENCOG/cogutil ```

``` mkdir build && cd build```

``` cmake .. ```

``` make ```

``` sudo make install```

**Step 3** - Clone and build Atomspace by repeating step 2 replacing cogutil with atomspace

**Step 4** - Clone and build Opencog by repeating step 2 replacing cogutil with opencog. Then do the following:

Within the build directory enter ``` make experiments```

Next, edit start_exp.sh under opencog/experiments/insect-poison/scripts and modify the oc_dir to point to your parent OPENCOG directory.

**Step 5** - Clone relex ( ``` cd ~/OPENCOG && git clone https://github.com/opencog/relex ``` ) and do the following:
 
``` cd relex/install-scripts ```

``` sudo ./install-ubuntu-dependencies.sh ```

**Step 6** - Download wordnet and conceptnet4.scm and add it in ```opencog/experiments/insect-poison/data/kb/``` directory. The files could be downloaded from [here](https://drive.google.com/open?id=1YOhKiomJ-TkyqBTn--Wu6cEB0fDktToJ)

**Step 7** - Run the start_exp.sh file and wait for the experiments to finish.

**Step 8** Get your result which will be stored in ```opencog/experiments/insect-poison/data/kb```.
