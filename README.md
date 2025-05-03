# AI-Enhanced-Intrusion Detection System (IDS)

Implementation
The proposed system was developed using Python and several powerful libraries for machine learning and data visualization. The overall objective was to build an efficient intrusion detection system by applying different machine learning models on the KDD ’99 dataset and combining their outputs through an ensemble voting mechanism.

Project Setup
Initially, the project environment was prepared by installing necessary Python libraries, including pandas, scikit-learn, matplotlib, seaborn, and xgboost. A structured setup was followed to ensure reproducibility, with all dependencies and usage instructions documented.

Dataset Ingestion and Preprocessing
The KDD ’99 dataset, available in CSV/GZ format, was used for model training and evaluation. Data ingestion and preprocessing were carried out using pandas and scikit-learn. During preprocessing, necessary steps such as handling missing values, encoding categorical variables, and splitting features and labels were performed to prepare the data for model training.

Exploratory Data Analysis (EDA)
Exploratory Data Analysis (EDA) was conducted to understand the underlying patterns and distribution of the data. Tools such as pandas, matplotlib, and seaborn were employed to visualize the data, analyze feature distributions, and detect any anomalies or imbalances within the dataset. This step helped in selecting appropriate features and understanding how different types of attacks were distributed.

Model Training
Three different machine learning models were implemented and trained on the preprocessed data:

Decision Tree Classifier:
A Decision Tree model was trained using scikit-learn. It worked by learning simple decision rules inferred from the features of the dataset to predict the attack category.

Gaussian Naive Bayes Classifier:
A Gaussian Naive Bayes model was also trained using scikit-learn. Since it assumes that the features are normally distributed, it was particularly efficient for high-dimensional data.

XGBoost Classifier:
An XGBoost model was trained separately using the xgboost library. XGBoost is a gradient boosting technique known for its speed and performance, especially with large datasets like KDD ’99.

Each model was trained independently to maximize its ability to detect different types of intrusions.

Ensemble Voting Aggregation
After training the individual classifiers, an ensemble voting mechanism was implemented. The outputs of the Decision Tree, Gaussian Naive Bayes, and XGBoost models were combined using a majority voting strategy. In this strategy, each model provided a prediction for a given input, and the final prediction was made based on the class that received the majority of votes among the three models. This ensemble method improved the overall performance by leveraging the strengths of individual models and reducing the impact of their weaknesses.

Evaluation and Results
Finally, the performance of the ensemble model was evaluated using appropriate metrics and plots. The system's accuracy, precision, recall, and F1-score were calculated to measure how effectively it could detect different types of network intrusions. Visualization techniques were used to represent the evaluation results, making it easier to analyze the performance of the models and compare them.

In addition to overall accuracy, evaluation metrics such as Precision, Recall, and F1-Score were used to analyze the model performance:

Precision measured the proportion of true positive predictions among all positive predictions.

Recall measured the ability of the model to detect all actual positive cases.

F1-Score provided a balance between precision and recall, especially useful when the dataset was imbalanced.

The final prediction in the ensemble method was made using a majority voting mechanism, where each individual model cast a "vote" for the predicted class, and the class with the highest votes was selected as the final output.

A confusion matrix was also generated to visually assess the number of correct and incorrect predictions across different intrusion categories.
