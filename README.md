# Credit_Card
Credit_Card_Fraud_Detection
Credit-Card-fraud-detection-system-using-Machine-Learning

Detect Fraudulent Credit Card transactions using different Machine Learning models and compare performances

In this notebook, I explore various Machine Learning models to detect fraudulent use of Credit cards. I compare each model's performance and results. The best performance is achieved using SMOTE technique.

Please note that this approach can be transferred to other detection analyses in alternative domains. The feature extraction process remains similar and can be replicated on many other detection issues.
Problem Statement

In this project, we want to identify fraudulent transactions with Credit Cards. Our objective is to build a Fraud detection system using Machine learning techniques. In the past, such systems were rule-based. Machine learning offers powerful new ways.

The project uses a dataset of 300,000 fully anonymized transactions. Each transaction is labelled either fraudulent or not fraudulent. Note that the prevalence of fraudulent transactions is very low in the dataset. Less than 0.1% of the card transactions are fraudulent. This means that a system predicting each transaction to be normal can reach an accuracy of over 99.9% despite not detecting any fraudulent transaction. This will necessitate adjustment techniques.
Techniques used in the project

The project compares the results of different techniques :

    Machine learning techniques:
        Random Forest
        Decision Trees
    Deep Learning Techniques:
        Neural network using fully connected layers.

The performance of the neural network is compared for different optimization approaches:

    plain binary cross-entropy loss minimization
    minimization using weights to compensate for the class imbalance
    Under-sampling of the non-fraudulent class to match the fraudulent class

Note about the difference between Random Forest and Decision tree models:

    A Random Forest is essentially a collection of Decision Trees. A decision tree is built on an entire dataset, using all the features/variables, whereas a random forest randomly selects observations (rows) and specific features/variables to build multiple decision trees from and then averages the results. After a large number of trees are built using this method, each tree "votes" or chooses the class, and the class receiving the most votes by a simple majority is the "winner" or predicted class.
    When using a decision tree model on a given training dataset the accuracy improves with more and more splits. You can easily overfit the data and it is recommended to use cross validation technique. The advantages of a simple decision tree model: easy to interpret, you know what variable and what value of that variable is used to split the data and predict outcome.
    A random forest is like a black box. You can specify the number of trees you want in your forest(n_estimators) and the max_num of features to be used in each tree. But you cannot control the randomness: which feature used for which tree, which data point is part of which tree... Accuracy keeps increasing as you increase the number of trees, but becomes constant at certain point. Random forest reduces the variance part of error rather than bias part. Unlike decision tree, it won't create highly biased model overfitting the data. By choosing features randomly during the training process, random forest does not depend highly on any specific set of features. This is a special characteristic of random forest over bagging trees. It generalizes better and on unseen validation dataset, Random forest always wins over Decision Tree in terms of accuracy.
