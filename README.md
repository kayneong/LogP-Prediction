# LogP-Prediction

# Project Title
Prediction of the partition coefficient (LogP) of molecules using supervised machine learning and neural networks. 

# Project Overview
The goal of this academic project is to accurately predict the LogP values of chemical molecules using their SMILES data (structural information) through feature engineering followed by construction and evaluation of various supervised machine learning models and neural networks. The models constructed in this project include Ridge regression, Support Vector regression, Multiple Linear Regression as well as Sigmoid and ReLU activation neural network models. The sigmoid-activated neural network model had the lowest mean squared error of 0.092 and the highest correlation coefficient of 0.9730 for the synthetic data set. However, when compared against a dataset collected experimentally, the support vector regression model seems to have a more consistent performance. 

# Business Understanding 
While the project was only meant for educational purposes in an academic setting, accurate prediction of LogP values can be beneficial in the chemical industry, especially for research and pharmaceutical organizations. A high-performing and stable model would allow precise prediction of LogP values for various novel leads of solvents or active pharmaceutical ingredients. This would allow efficient triaging of compounds if a target range of LogP values is established for further research and development of a new chemical product, saving labor and monetary costs for the companies. 

# Data Understanding 
The synthetic dataset was provided through our professor and the access to the link has been removed. A copy of the synthetic dataset can be found in the files of this repository. The synthetic dataset contains 14610 rows and the feature given was the SMILES notation structural information of the molecules while LogP was the outcome variable to predict. Feature transformation and extraction of the SMILES values were conducted to create additional features such as but not limited to: the number of heavy, carbon, oxygen, halogen and nitrogen atoms, number of valence electrons, and total polarisable surface area. These additional features are known to influence LogP values and hence, may be important predictors of LogP for our models. 

# Modeling and Evaluation 
The scatterplots below show comparisons between the LogP predictions of each model versus the test set and their corresponding correlation coefficients for the synthetic dataset. The sigmoid-activated neural network model shows the highest correlation coefficient of 0.9730
![image](https://github.com/kayneong/LogP-Prediction/assets/150570357/87ca7c2a-31d7-43c6-a3af-6cdf13477fb6)

However, the scatterplots for the model evaluations on the experimental dataset below show that the support vector machine regression (SVM) was performing more consistently than the other models that were constructed whether on the synthetic or experimental dataset. 
![image](https://github.com/kayneong/LogP-Prediction/assets/150570357/86040120-0c23-435d-b915-b040196fec9b)

# Conclusion
This project has concluded that while the sigmoid-activated neural network model was the most accurate in prediction for the synthetic dataset, the support vector machine regressor was the most stable with acceptable performance overall. It is worth noting that the experimental dataset was small, with only 658 rows representing molecules for the models to train on and data collection was conducted ambiguously without external reaction parameters included as features for training. That is to say, the LogP values collected for the experimental dataset may not have been conducted in a controlled environment. Further recommendations include the addition of other features such as reaction parameters and conditions, inter and intra-molecular interactions as well as entropic considerations. The models could also be trained on the synthetic dataset before being evaluated on the smaller experimental dataset if the data collection was conducted in a controlled fashion. 
