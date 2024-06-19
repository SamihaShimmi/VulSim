This repository contains the artifact for the paper "VulSim: Leveraging Similarity of Multi-Dimensional Neighbor Embeddings for Vulnerability Detection" (accepted in USENIX Security 2024)

# Steps to run VulSim (Replicate Table 3)
Our final model is a decision tree-based classifier. 

The code to run the classifier is available in the Classifier folder (decisionTree.ipynb). 

Our model relies on three existing models code2vec, SBERT and CodeBERT. We processed the data using these three models and the input data to the classifiers are available in Classifier/data folder. In order to directly run the classifier, we do not have to run  code2vec, SBERT and CodeBERT. We can use the pre-processed data avalable in  Classifier/data folder and replicate result for Table 3 in the paper.

As we can see from the paper, we have several sets of results based on n=5 and n=3 settings. Additionally, we have results for single dimension, double dimension and hybrid dimension. The hybrid dimension merges all 3 dimensions and we consider that as the final result for VulSim. To run VulSim for n=3 and n=5, the file name in decisionTree.ipynb will be code2vecSBERTCodeBERTN=3.xlsx and code2vecSBERTNCODEBERTN=5.xlsx respectively. In order to replicate the results for single and double dimensions, the appropriate file name should be selected and the filenames in data folder are self-explanatory.

# Our model relies on three existing models code2vec, SBERT and CodeBERT. We pre-processed the data using these three models that is available in Classifier/data folder. In order to pre-process data yourself, the following steps need to be done.

# Dataset
we used Devign dataset. Link to devign datataset is https://sites.google.com/view/devign.

We had to remove 71 records due to the code2vec implementation. Our test, train and validation file can be found at clearnDevignJsonl folder after removing 71 records.
After removing 71 records, modified dataset can be downloaded from here https://drive.google.com/drive/folders/1AGFr3Z3yfhwY5HYW3vvMSY5KGrVzFG7K?usp=sharing


# code2vec (trained on Devign) is implemented using https://github.com/dcoimbra/dx2021 and needs to be downloaded using their instructions. 

Our part is available in code2vec folder.

given dataset, ReportCC++Code2Vec.ipynb file generates the embeddings

cosine similarity and rankings are generated using ReportCC++Code2VecOurs.ipynb file

the result after applying the rankings are availabe inside classifier folder. There is a folder named 'data'. The data folder contains the ranking results in single dimension, double dimension and hybrid dimension(VulSim). you can use those data to feed into the decisionTree.ipynb classifier inside classifier folder and get the result directly.

# SBERT is implemented using https://www.sbert.net/

the classifying result using SBERT was implemented using https://towardsdatascience.com/sbert-vs-data2vec-on-text-classification-e3c35b19c949

Our part is available in SBERT folder

ReportCC++SBERTOurs.ipynb file generates the embeddings, cosine similairity and ranking

Similarly the result can be passed to the  decisionTree.ipynb

Then codebertOurs.ipynb generates the ranking and we can pass it to the classifier.

# CodeBERT is implemented from Microsoft CodexGlue benchmark https://github.com/microsoft/CodeXGLUE/tree/main/Code-Code/Defect-detection. The model need to be donwloaded and fine-tuned using their instruction.

Our part is available in CodeBERT folder

A2 - Code Edits.ipynb this file generates the embeddings and calculates cosine similarity.
Then codebertOurs.ipynb generates the ranking and we can pass it to the classifier.


# Visualization
visualization part can be downloaded from Visualization directory. data.7zip should be extractd. Then you can run using python3 -m http.server / python -m http.server command. Run localhost to see the report.
