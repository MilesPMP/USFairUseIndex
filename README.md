# USFairUseIndex

The dataset, the PMP US Fair Use Index dataset, is an update and expansion of a dataset provided by the U.S. Copyright Office on Fair Use. This version supports further analytics.  

## Background
Fair use is the unlicensed but permitted use of copyright-protected works.

The U.S. Copyright Office Fair Use Index tracks judicial decisions to help understand the types of uses courts have previously determined to be fair—or not fair. The decisions span over a century of decisions and in 2022 over 240 decisions but is not exhaustive. 

## Data needs reshaping
We reviewed the index, found it to be fairly user-friendly but flawed. For each decision the index includes the case name, a “summary of the facts, the relevant question(s) presented, and the court’s determination as to whether the contested use was fair.” The records include court name, jurisdiction, e.g., circuit, and year. The index also includes category and outcome data. 

The data format of the Fair Use Index isn’t useful for further analysis. The categories are listed as comments in one cell. The terms used are inconsistent in capitalization and punctuation -- commas and semicolons are both delimiters. As well, the descriptions of the outcomes are inconsistent. There were some other issues like inconsistent names for the same court. 

## Changes
We took the data from the U.S. Copyright Office as pushed in 2022 August.  We pulled the data again in 2023. 

We cleaned up the category -- capitalization and punctuation -- to make 18 categories.  We then made each a category a flag in a two-dimensional table and then reshaped the data into a one-dimensional table. 

We classified all outcomes in to three types to group the specific labels from the Copyright Office: 

•	Fair Use Found -- Fair use found | Fair use found; Mixed result | Fair use found; Affirmed on appeal

•	Fair Use Not Found -- Fair use not found | Fair use not found, preliminary ruling | 
Preliminary ruling; Fair use not found | Preliminary ruling; Fair use not found; Mixed result

•	Other -- Mixed Result | Preliminary ruling; Remand | Preliminary ruling; Mixed result or Remand

Other changes include standardizing the names of the courts, cleaning up the punctuation, and splitting URLs from case names.  

## Results
The data can now be analyzed by a pivot table. You can track the change in findings over time.  You can compare circuits, categories, or both.  

## Notes

### Files
This repository includes this read me, license, data, and metadata files. 

### Sources
PMP acknowledges the dataset is provided by U.S. Copyright Office. And while this work is in the public domain we are grateful to the employees of the office that created and maintain the index. 

### License
The PMP US Fair Use Index dataset and all datasets in this repository, are licensed under a creative commons license in the attached [LICENSE.md](LICENSE.md) file. By accessing or copying any part of the datasets, the user accepts the terms of the license and becomes a Licensee.
