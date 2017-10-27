# TF1.3_New_Input_Pipeline_Demonstration

This is a demonstration of the TensorFlow's new Dataset and Estimator APIs. here I have used 
The trained model categorizes Iris flowers based on four botanical features (sepal length, sepal width, petal length, and petal width). So, during inference, you can provide values for those four features and the model will predict that the flower is one of the following three beautiful variants: Sertosa, Versicolor or Virginica. The model is built using a pre-made Deep Neural Net Regression Classifier - an Estimator provided by the new Estimator API.

Requirements:
1. Python 3 or above
2 Tensorflow 1.3 or above


Steps:
1. Import tensorflow, os and sys
2. Download Datasets from given URL
3. Create Data Pipeline for Input into the Model(Preprocess, split, batch)
4. Create Model DNNClassifier using Tensorflow Estimators
5. Train DNNClassifier with training data from Input Pipeline
6. Evaluate Model with .evaluate with testing data from Input Pipeline
7. Test Prediction with Test data, then test prediction with your data.

All steps have been described and implemented in the Jupyter Notebook : tf1.3_pipeline_estimator_DNNClassifier.ipynb


Reference Links:
1. https://www.tensorflow.org/versions/master/extend/estimators
2. https://medium.com/onfido-tech/higher-level-apis-in-tensorflow-67bfb602e6c0
3. https://www.tensorflow.org/programmers_guide/datasets
4. https://apimirror.com/tensorflow~guide/programmers_guide/reading_data
5. https://kratzert.github.io/2017/06/15/example-of-tensorflows-new-input-pipeline.html
6. https://github.com/tensorflow/workshops/blob/master/notebooks/07_structured_data.ipynb


Reference Papers:
1. https://arxiv.org/pdf/1708.02637.pdf - TensorFlow Estimators: Managing Simplicity vs. Flexibility in
High-Level Machine Learning Frameworks


Problems:
1. Updating Tensorflow to v1.3 caused my Tensorboard to get uninstalled. But could be easy fixed by using pip to install again

2. Allowed structure had changed. Now x = make_iterator; x.get_next() returns an error. it must be eg.) 
batch_features, batch_labels = dataset.make_one_shot_iterator().get_next()





