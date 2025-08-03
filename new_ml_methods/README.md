This Jupyter notebook, ml_methods.ipynb, explores alternative machine learning approaches to the
  k-Nearest Neighbors (KNN) algorithm originally used in NPOmix for linking Biosynthetic Gene Clusters (BGCs) to Gene Cluster Families (GCFs). The primary goal of this notebook is to investigate whether other models, such as Random Forest, can provide more accurate and robust predictions for this task.

  The notebook is structured into the following sections:

   * 1) Import packages: This section imports the necessary Python libraries for the analysis, including such as pandas, scikit-learn, and matplotlib.

   * 2) Load datasets: In this part, the notebook loads the required datasets, which include the
     molecular family dictionary (mf_dict.pkl), the pre-computed testing and training dataframes
     (pre_testing_df.pkl, training_df.pkl, testing_df.pkl), and the final dataframe (final_df.pkl).
     These files contain the processed data from the initial NPOmix workflow.

   * 3) ML model: This is the core section of the notebook, where the machine learning models are
     implemented and evaluated. The main steps are:
       * Data Preparation: The training data is split into features (X_train) and labels (y_train), and the labels are encoded for use in the model.
       * Model Training: A Random Forest Classifier is trained on the prepared data. This model was chosen as an alternative to KNN to explore its potential for improved performance.
       * Prediction: The trained model is used to predict the top-3 GCFs for each sample in the test set.
       * Evaluation: The predictions are then evaluated by comparing them against a ground truth
         dataset, annotated_nodes_df.pkl, which contains known BGC-GCF links. This allows for an
         assessment of the model's accuracy and its ability to generalize to new data.

  This notebook serves as a starting point for exploring more advanced machine learning techniques for the NPOmix pipeline. Future work could involve experimenting with other algorithms, optimizing hyperparameters, and incorporating more complex feature engineering to further improve the accuracy of BGC-GCF predictions.
