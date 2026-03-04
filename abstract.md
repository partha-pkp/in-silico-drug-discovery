## Abstract


Intro?  
Recent work in the senolytics field has demonstrated the potential of machine learning to accelerate the discovery of small‑molecule senolytic compounds. In one of the studies, researchers generated more than 200 physicochemical descriptors from SMILES strings to perform feature selection, and trained several classification models to identify candidate senolytics. In another interesting work, they trained graph neural networks based on SMILES strings and screened close to a million compounds for potential senolytics. These two studies are the data sources and form the ideological basis for the present project.


Aiden:  
Semi-Supervised K-Means Model. Using a simple logistic regression model + the projection of the compounds on the Principal Components' Axes, I will cluster the data using K-Means. The cluster with the highest density of senolytics would be the best place to check for more senolytics. Given the lack of data on true senolytic compounds, the unsupervised structure of K-Means seemed appropriate for the data.


Avanie:
Logistic regression will be used to classify chemical compounds as senolytic or non-senolytic using molecular descriptor data. The preprocessing pipeline includes removing non-informative attributes, standardizing features, and converting the senolytic label to nominal format. Models will be trained in WEKA using stratified 10-fold cross-validation while tuning the ridge regularization parameter. Because the dataset is highly imbalanced, SMOTE will be applied to generate additional minority-class samples. Model performance will be evaluated using precision, recall, and F1-score for the senolytic class, since F1 balances precision and recall and is more informative than accuracy for imbalanced datasets. Different SMOTE percentages will also be tested to analyze how oversampling affects performance and the detection of senolytic compounds.


Pardis



Partha:  
The feature‑selection phase in Smer-Barreto et al. (2023) retained almost 175 out of 200 attributes. Their technique falls short in critically examining the significant features that effectively classify the target class. There is a need for a robust feature selection analysis that improves model interpretability and predictive performance.
To address this methodological gap, we plan to use WEKA to systematically evaluate stronger feature‑selection strategies, such as information gain, correlation‑based subset selection, and wrapper methods with cross‑validation.



Vishakh
