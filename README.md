# Combining-Multiple-Classifiers-To-Increase-Accuracy

Generally one classifier is used to get the label of the data. Mostly parameter optimization is performed to get better accuracy. However, in this project, multiple classifiers are used to classify the label, If the majority of the classifier give a label to the data, then that will be considered as accurate label of the data. There also arise the question in mind, if multiple weak classifiers are combined then definitely the result will be false. However, to address this, first a threshold will be set for the classifier to be eligible for classification. E.g, the minimum accuracy of the model must be over 80% (Just suppose), then the model can predict the label. This will ensure the result more accuracte as multiple strong classifier will have higher chances to predict hte label correctly. 

# Tools and Technology Used

In this project, mainly pyspark with python is used which will be helpful when dealing with large data, this project can be run in google colab directly [https://colab.research.google.com/drive/13Azau9luZTHGO6h0ARq9DuGvd1rSBF9l?usp=sharing].
Classification Algorithms used are Naive Bays, Random Forest Classifier and Decision Tree Classifier. Pyspark, Python are used for coding

# Methology 

1. First of all data is pre-processed, then subset of data is taken randomly.
2. On each subset, three different algorithms are trained. 
3. Now for testing, the same record is passed through each model i-e ,
<pre>
   Naive Bays  -------  Decision Tree ---------- Random Forest ------- Final Label / Target
   
   1                       0                         1                         1   
   
   0                       0                         1                         0    </pre>
   
 4. Here we can see the first record has major true outputs (two 1's and one 0) so the final output will be 1.

# Results
While applying the same technique, the naive bays classifer accuracy was 59%, but when multiple classifiers were used, the accuracy inreased to 76%, Attached here is screen shot ![image](https://github.com/GhiasAli17/Combining-Multiple-Classifiers-To-Increase-Accuracy/assets/76915661/e4b5dc92-3cfc-4124-84c4-cde77fd24387)
