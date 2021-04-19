(currently under development, run at your own risk)

[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.452-blue.svg)](https://doi.org/10.25663/brainlife.app.452)

# app-abcd-hcp-pipeline
This App is a Brainlife wrapper for the [Developmental Cognition and Neuroimaging (DCAN) Labs' modified HCP pipeline](https://github.com/DCAN-Labs/abcd-hcp-pipeline). This BIDS application initiates a functional MRI processing pipeline built upon the Human Connectome Project's minimal processing pipelines, which is robust to scanner, acquisition and age variability.

#### References and resources to consider
* ABCD-HCP Pipelines main repository: https://github.com/DCAN-Labs/abcd-hcp-pipeline
* ABCD-HCP Pipelines BIDS-app wrapper: https://hub.docker.com/r/dcanlabs/abcd-hcp-pipeline
* HCP Pipelines main repository: https://github.com/Washington-University/HCPpipelines
* HCP Pipelines BIDS-app wrapper: https://github.com/BIDS-Apps/HCPPipelines

### Authors
- Giulia Bertò ([@giulia-berto](https://github.com/giulia-berto))

### Project director
- Franco Pestilli ([@francopestilli](https://github.com/francopestilli))

### Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your code and publications. Copy and past the following lines into your repository when using this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)

### Citations
We ask that you cite the following articles when publishing papers that used data, code or other resources created by the brainlife.io community.

1. Sturgeon, D., Perrone, A., Earl, E., & Snider, K. DCAN_Labs/abcd-hcp-pipeline. DOI: 10.5281/zenodo.2587209. (check on zenodo.org for a version-specific DOI/citation)

2. Glasser MF, Sotiropoulos SN, Wilson JA, Coalson TS, Fischl B, Andersson JL, Xu J, Jbabdi S, Webster M, Polimeni JR, Van Essen DC, Jenkinson M; WU-Minn HCP Consortium. The minimal preprocessing pipelines for the Human Connectome Project. Neuroimage. 2013 Oct 15;80:105-24. doi: 10.1016/j.neuroimage.2013.04.127. Epub 2013 May 11. PMID: 23668970; PMCID: PMC3720813. https://pubmed.ncbi.nlm.nih.gov/23668970/

3. Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

For the full list of references, please see https://github.com/DCAN-Labs/abcd-hcp-pipeline.

## Running the App 

### On Brainlife.io

Check out the brainlife app [here](https://doi.org/10.25663/brainlife.app.452)

### Running Locally

Information on how to run ABCD-HCP Pipelines locally can be found here:
https://github.com/DCAN-Labs/abcd-hcp-pipeline.

### Inputs

This App requires at least one T1w scan, and optionally one (or more) functional data. If only the T1w is provided, only the structural preprocessing will be run. As in the original pipeline, you can select the step of the analysis (stage) to begin with; possible options are: PreFreeSurfer, FreeSurfer, PostFreeSurfer, FMRIVolume, FMRISurface, DCANBOLDProcessing, ExecutiveSummary, CustomClean. (fieldmap input coming soon)

### Outputs

A folder containing all the outputs. (at the moment just raw datatype, different datatypes under development)

### Dependencies

This App requires [singularity](https://www.sylabs.io/singularity/) to run. If you don't have singularity, you will need to install following dependencies. It also requires [jq](https://stedolan.github.io/jq/).

#### MIT Copyright (c) 2020 brainlife.io The University of Texas at Austin and Indiana University
