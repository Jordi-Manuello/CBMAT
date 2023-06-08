# CBMAT
CBMAT is a MATLAB® suite of user-friendly and automated functions assisting researchers through data preparation for coordinate-based meta-analysis and post-hoc analyses

CBMAT consists of the following seven functions:
1)	load_foci: To import foci into MATLAB®
2)	remove_multiple: To remove multiple experiments included in a same paper
3)	filter_by_tissue: To select foci in gray matter or white matter only 
4)	prepare_MACM: To prepare data for Meta-Analytic Connectivity Modelling
5)	create_LOEO: To prepare data for Leave One Experiment Out analysis 
6)	create_subsets: To prepare data for split-half or sub-sets analysis
7)	dataset_hist: To create histograms allowing to visualize features of the dataset

A typical workflow in CBMAT can be: 

- import data with 'load_foci' 
- prepare data for the main CBMA with 'remove_multiple' and/or 'filter_by_tissue' and/or 'prepare_MACM' 
- prepare data for post-hoc analyses with 'create_LOEO' and/or 'create_subsets'. 
- 'dataset_hist' can be used to inspect the obtained output at any stage of the process. 

Notably, CBMAT allows high flexibility in the workflow, as the output of each function (excluding dataset_hist) is a .txt file ready to be analysed with third party software or to be passed to another function.

A general description of each function is provided below:

'load_foci' allows to load the .txt input into MATLAB. The output .txt will contain both coordinates and meta-data of the experiments originally included in the input file, after removal of possible duplicates. Experiments are treated as duplicates based on identical meta-data and identical reported coordinates.

'remove_multiple' allows to retain only one experiment among those which came from a same paper, i.e. having same first author and year of publication. The argument 'mode' allows to control the way the sampling is made (1 = greater sample size; 2 = at random). 

'filter_by_tissue' allows to specify a tissue of interest and to retain in each experiment only foci located in it. The tissue is specified as a 2x2x2 mm .nii binary mask in Talairach standard space through the argument 'ROI'.

'prepare_MACM' allows to prepare data to run Meta-Analytic Connectivity Modeling (MACM). In doing so, experiments are retained only if they report at least one coordinate of effect in a given region of interest specified as user defined as a 2x2x2 mm .nii mask in Talairach standard space through the argument 'ROI'.

'create_LOEO' allows to prepare data to run a Leave One Experiment Out validation. Given an original dataset of n experiments it generates n subset with n-1 experiments each. If the argument 'add' is set to 1 the procedure becomes incremental, so to exclude one more experiment at each iteration.

'create_subsets' allows to prepare data to run a sub-sample validation. The argument 'ns' sets the number of sub-samples to be created, while the argument 'nexp' specifies the size of each sub-sample. Finaly, the argument 'rep' controls replacement. Different combinations of these parameters allows to prepare data for either a split-half analysis or a boot-strap analysis.

'dataset_hist' allows to visualize the distributions of the sample size and year of pubblication of the experiments included. The number of bins to be shown in the histogram of sample sizes can be controlled through the argument 'sbins'. Both the average sample size and the median year of publication are also computed and shown over the histograms.










