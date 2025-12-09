## Data measurement and collection
This dataset contains demographic and clinical characteristics from the 
electronic health records of patients who were referred to and scheduled 
at the CU Functional Neurological Disorders Clinic between April 1, 2020 and
April 1, 2025. All patients have been de-identified in excel prior to import,
and the study team has approved the use of this data for this activity. 

There are data on 485 patients who completed the Brief Illness Perceptions 
Questionnaire (BIPQ). The primary outcome of this dataset are each patients' 
BIPQ score, which is categorized by 1. total sum score and 
2. a 2-level factor variable (Low/Moderate, and High). The BIPQ and its cutoff 
points have been validated and shown to have good test-retest reliability across
multiple diseases
[Broadbent et al. 2006](https://pubmed.ncbi.nlm.nih.gov/16731240/). 

**Note, the categorization of patient scores according to Low/Moderate versus High 
has not been tested within an FS population. This categorization was made 
for exploratory purposes, and other cutoff values may be a better representation
of a "High" score for this populations' illness perceptions**


The BIPQ was administered virtually after the neurology intake session. 
The other variables were obtained through 1. chart review and/or
2. questions asked of the patient during their neurology intake and psychology 
intake (if available).   

## Data format 

The data are stored in multiple .csv files within the `/data` folder, 
which are merged in the Data Cleaning document "DataCleaning.rmd", contained 
within the `/Writing` folder. To conduct the entire analysis, beginning with 
data cleaning, begin with this document first. 

A data dictionary is provided in an excel table within the main folder of this 
repository. 

## Analysis 

The analyses conducted include descriptive analyses, a binary logistic regression 
assessing which variables are associated with a higher BIPQ score, and a 
linear regression of the proportion of visits attended versus scheduled for each 
patient regressed on their BIPQ score level. The second analysis is weighted, 
using inverse probability weighting for having a High BIPQ score, as predicted 
by Model 1. 

To conduct the analysis, open the file "Analysis.rmd" located within the 
`/Writing` folder. 