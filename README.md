# Transformer versus Traditional Natural Language Processing: How Much Data is Enough for Automated Radiology Report Classification?
This repository contains sample code references for a manuscript in preparation with the above title. In the article, the performance of transformer and traditional machine learning models were evaluated on multiple classification tasks. As the workflow for all tasks were identical, one notebook for each approach is stored here as samples for reference. We are not able to share any patient data. All data are formatted identically, where for each report, there exists key columns containing radiology texts and binary ground-truth labels for the target classification task. 

## Notebook Contents

- Brain_MRI_Head_CT_NLP_Sample.ipynb contains the code for the following sections of the manuscript for infarction classification:
  - Materials and Methods: CT and Brain MRI Data Annotation and Filtering
  - Materials and Methods: Radiology Text Preprocessing
  - Materials and Methods: NLP Model Training - Traditional NLP Models
  - Materials and Methods: NLP Model Testing
  - Materials and Methods: Subsampling Experiments
  - Results
- Knee_Transformer_Sample.ipynb contains the code for the following sections of the manuscript for meniscus tear classification:
  - Materials and Methods: Knee MRI Data Annotation and Filtering
  - Materials and Methods: Radiology Text Preprocessing
  - Materials and Methods: NLP Model Training - Transformer Deep Learning Model
  - Materials and Methods: NLP Model Testing
  - Materials and Methods: Subsampling Experiments
  - Results

## Abstract
 
RATIONALE AND OBJECTIVES: 		

Current state-of-the-art natural language processing (NLP) techniques use transformer deep learning architectures, which depend on large training datasets. We hypothesized that traditional NLP techniques may perform better than transformers for smaller radiology report datasets. 	

MATERIALS AND METHODS:

We compared the performance of BioBERT, a deep learning-based transformer model pre-trained on biomedical text, and three traditional machine learning models using bag-of-words feature representation (gradient boosted tree, random forest, and logistic regression) on multiple classification tasks given free-text radiology reports. Classification tasks included detection of appendicitis, diverticulitis, bowel obstruction, or enteritis/colitis on abdomen/pelvis CT reports, ischemic infarct on brain CT/MRI reports, and medial or lateral meniscus tears on knee MRI reports (7204 total annotated reports). The performance of NLP models on held-out test sets were compared after training using the full training set, and 2.5%, 10%, 25%, 50%, and 75% random subsets of the original training data. 
 
RESULTS:

In all the classification tasks tested, BioBERT performed poorly at smaller training sample sizes compared to non-deep learning NLP models. Specifically, BioBERT required training on approximately 1,000 reports to perform similarly or better than non-deep learning models. At around 1,250 to 1,500 training samples, the testing performance for all models began to plateau, where additional training data yielded minimal performance gain.

CONCLUSION:			

With larger sample sizes, deep learning-based transformer NLP models achieved superior performance in radiology report binary classification tasks. However, with smaller sizes (<1000) and more imbalanced training data, traditional NLP techniques performed better. 

