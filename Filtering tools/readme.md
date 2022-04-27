# DeViVa Filtering Tools

The DeViVa filtering tools can be used to filter input data based on various criteria for a DeViVa analysis. There are two versions available:

* __filtering.py__ &emsp; a simplyfied version with GUI dialogs for entering the filtering parameters
* __filtering_exp.py__ &emsp; an advanced version where all parameters are set initially

__USAGE:__

The DeViVa filtering tools are Python scripts that can be run on any operating system. Please ensure that you are using Python 3.x! To start the filtering, go to a terminal and type in:

_python filtering.py -d -m_

or 

_python filtering_exp.py -d -m_

You can add additional arguments if needed, but -d is always needed!

__DEPENDENCIES:__

DeViVa needs some additional Python packages to be installed. You can install them manually or use the DeViVa.install file when working on Linux. Here is a full list of all required Python packages:

* Bio

* matplotlib

* numpy

* pandas

* scikit-bio

* scikit-learn

* scipy

* seaborn

__OPTIONS:__

__Required:__

__ -d, --data__ &emsp; Name of the input data file.

__ -m, --metadata__ &emsp; Name of the input metadata file.

__Optional (only available for "filtering_exp.py"):__

__-af, --allele_frequency__ &emsp; Treshold for allele frequency, lower values are interpreted as 0. Use -1 if you do not want to apply a threshold for allele frequency. Input must be a number between 0 and 1, e.g. 0.05 or 0.01. [Default: -1]

__-cv, --coefficient_variant__ &emsp; Maximum coefficient of variant of a sample to be retained. Use -1 if you do not want to apply this filter. Input must be a number between 0 and 1, e.g. 0.7 or 1.3. [Default: -1]

__-e, --end__ &emsp; Last epidemiological week to be included in the analysis. Use -1 for the last week. [Default: -1]

__-h, --help__ &emsp; Show this help message and exit.

__-l, --location__ &emsp; Locations to be included in the analysis. In case of more than one location, separate each location by a comma sign. Use "all" to include all locations. [Default: all]

__-ms, --min_samples__ &emsp; Minimum number of samples in which a mutation must be present in order to be retained. Use -1 if you do not want to apply this filter. [Default: -1]

__-n, --name__ &emsp; Name of the analysis, it will be used for labelling all result files. If no name is provided, data files will be labelled with 'DATA.txt' and 'META.txt'!

__-o, --output_dir__ &emsp; Ourput directory where all result files are stored. If no output directory is provided, files are stored in the current working directory!

__-r, --region__ &emsp; Regions to be included in the analysis. In case of more than one region, separate each region by a comma. Use "all" to include all regions. [Default: all]

__-rd, --read_depth__ &emsp; Threshold for read depth, lower values are interpreted as 0. Use -1 if you do not want to apply a threshold for read depth. [Default: -1]

__-s, --start__ &emsp; First epidemiological week to be included in the analysis. [Default: 1]

__-um, --undetected_mutations__ &emsp; Maximum percentage of undetected mutations in a sample to be retained. Use -1 if you do not want to apply this filter. Input must be a number between 0 and 1, e.g. 0.05 or 0.01. [Default: -1]

__-v, --version__ &emsp; Show program's version number and exit.