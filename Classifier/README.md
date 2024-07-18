1. You have to place the decisionTree.ipynb file in the desired drive in Google Drive.

2. Download all the files from "data" folder which is located inside "Classifier".

3. Place all the files ( decisionTree.ipynb, all files you downloaded from the "data" folder) in the same folder.

4. Start running from cell 1

5. In the third cell of the decisionTree.ipynb file, you have to provide the location of your folder where you placed all the files.

6. In cell 7, please provide the file name you want to run the experiment. For example, if you want to run the multidimensional model (VulSim) , the required file is "code2vecSBERTNCODEBERTN=5.xlsx" for n=5. For n = 3, the required file is "code2vecSBERTCodeBERTN=3.xlsx". Please note that, for each file you have to run the full code starting from the beginning and provide the corresponding file name. For example, if you are running the experiment for n = 5, change the file name to "code2vecSBERTNCODEBERTN=5.xlsx" and run the remaining steps.

7. Run the remaining code and in the last cell, you will get the accuracy, precision and recall for the corresponding model. For the given example, you will get the result of the last segment of Table 3. For example, when you select "code2vecSBERTCodeBERTN=3.xlsx", it will give the accuracy 75.34% and the corresponding precision and recall.

8. You need to repeat the whole code with a new file name every time you want to generate one of the results of Table 3. 

9. corresponding file name for each part of the table: Single Dimension n =5 semantic space "resultSBERTN=5.xlsx" Single Dimension n = 3 semantic space "resultSBERTN=3.xlsx" Single Dimension n = 5 syntactic space "resultTop5CodeBERT.xlsx" Single Dimension n = 3 syntactic space "resultTop3CodeBERT.xlsx" Single Dimension n = 5 contextual space "resultTop5Code2vec.xlsx" Single Dimension n = 3 contextual space "resultTop3Code2vec.xlsx" Double Dimension n = 5 semantic-contextual space "code2vecSBERTN=5.xlsx" Double Dimension n = 3 semantic-contextual space "code2vecSBERTN=3.xlsx" Double Dimension n = 5 semantic-syntactic space "codeBERTSBERTN=5.xlsx" Double Dimension n = 3 semantic-syntactic space "SBERTCodeBERTN=3.xlsx" Double Dimension n = 5 syntactic-contextual space "code2vecCodeBERTn=5.xlsx" Double Dimension n = 3 syntactic-contextual space "code2vecCodeBERTN=3.xlsx" Multi-Dimensions (VulSim) n = 5 semantic-contextual-syntactic space "code2vecSBERTNCODEBERTN=5.xlsx" Multi-Dimensions (VulSim) n = 3 semantic-contextual-syntactic space "code2vecSBERTCodeBERTN=3.xlsx"

10. To run on a new dataset, you have to pre-process the files and provide the classifier with that pre-processed data
