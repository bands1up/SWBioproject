For the code to run you will need to install pandas, seaborn, matplotlib, numpy, scipy, and all sklearn modules into your anaconda environment.

You will also need to save the SoloProject.ipynb and plotknn.py files in the same folder and open them together.

**Introduction/motivation**

The wine dataset is a multi-class and multi-feature classification data set containing three classes of wine with 59 + 71 + 48 = 178 samples total. 

In this python script I employ k-nearest neighbours analysis to invesitgate the contribution that two features of the wine samples (hue and proline) make towards predicting the class of the wine. 

I also use principal components analysis (PCA) to reduce the dimensionality of the data set and investigate how the variance of every feature collectively predicts the class of wine, visualised as a class-dependent clustering of the data below. 

I wanted to use these techniques in order to hone my ability to employ k-nearest neighbours analysis and PCA to analyse a multi-class and multi-feature classification data set, as this will prove useful when classifying and clustering neuronal populations based on electrophysiology data further down the line in my PhD project.

**Methods**

I initially imported and visualised the Scikit-Learn wine data set as a data frame.

Then, I established and visualised my target response variable as the three classes of wine (0, 1, and 2) in an array.

Next, I plotted a scatter matrix of every possible feature pair and selected hue versus proline as a feature pair to analyse further, due to a distinct 2D spread of the data, implying that each feature in the pair will contribute to identifying the class of wine that a sample belongs to.

Subsequently, I created a data set for hue and proline and split this data set into a training and test data set. 

Then, I used hyperparameterisation to identify the optimal number of nearest numbers to use in the k-nearest neighbours analysis of hue versus proline. 

After that I plotted the results of the unscaled k-nearest neighbours analysis. 

Next, I rescaled the data and plotted it again. 

A model score was calculated for the scaled and unscaled k-nearest neighbours analysis. 

I then conducted a PCA to reduce the dimensionality of the data set and investigate how the variance of every feature collectively predicts the class of wine, visualised as a class-dependent clustering of the data. 

Finally I conducted a k-nearest neighbours analysis of PC1 and PC2 to visualise the clustering of the data and to aid the predicted classifcation of new hypothetical data added into the data set.

**Results**

Unscaled k-nearest neighbour analysis of hue versus proline gave a score of 0.755...

Scaled k-nearest neighbour analysis of hue versus proline gave a score of 0.955...

k-nearest neighbours analysis of PC1 and PC2 from the PCA gave a score of 0.977...

**Summary/conclusions**

PCA predicted the class of wine to a greater degree of accuracy than the scaled k-nearest neighbours analysis comparing the hue and proline of the wine. 

This is visualised as a more distinct clustering of the data from each class of wine in our PCA in comparison with the hue versus proline k-nearest neighbours analysis. 

Therefore, for a multi-class and multi-feature electrophsyiology and RNA sequencing data set, I predict that PCA would classify/cluster a neuron into a genetically defined neuronal subpopulation with a greater degree of accuracy than a k-nearest neighbours analysis would. 