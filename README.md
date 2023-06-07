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

A typical workflow in CBMAT can be 

- import data with 'load_foci' 
- prepare data for the main CBMA with 'remove_multiple' and/or 'filter_by_tissue' and/or 'prepare_MACM' 
- prepare data for post-hoc analyses with 'create_LOEO' and/or 'create_subsets'. 
- 'dataset_hist' can be used to inspect the obtained output at any stage of the process. 

Notably, CBMAT allows high flexibility in the workflow, as the output of each function (excluding dataset_hist) is a .txt file ready to be analysed with third party software or to be passed to another function.

