# Practical Machine Learning Course Project

This repository contains the project files for the Practical Machine Learning Course Project. In this project, we analyze the Human Activity Recognition (HAR) Weight Lifting Exercises Dataset and build machine learning models to classify different types of exercises based on sensor data.

## Project Overview

The goal of this project is to predict the type of exercise performed by individuals (classe variable) using sensor data from accelerometers, gyroscopes, and magnetometers placed on different parts of the body (arm, forearm, belt, and dumbbell). We implemented various machine learning models to improve prediction accuracy and compared their performance using cross-validation.

## Dataset

The data comes from the Human Activity Recognition (HAR) study, where six young healthy participants performed a set of 10 repetitions of the Unilateral Dumbbell Biceps Curl in five different ways:

* Class A: Exactly according to the specification.
* Class B: Throwing the elbows to the front.
* Class C: Lifting the dumbbell halfway.
* Class D: Lowering the dumbbell halfway.
* Class E: Throwing the hips to the front.

## Project Structure

pml_course_project.Rmd: The main RMarkdown file containing the analysis, data preprocessing, model training, and model evaluation.
pml_course_project.html: The HTML output of the project report generated from the .Rmd file.
model_stack.rds: The saved stacked model object that was built using various base models.
weight_lift_image.png: A diagram or image showing the placement of sensors on the body for better visualization.

## Key Steps in the Analysis

### Data Preprocessing:

Omitted metadata such as user names and timestamps to avoid overfitting.
Removed columns with more than 70% missing data.
Scaled and centered the data, and applied Principal Component Analysis (PCA) to reduce dimensionality.
Model Training:

### Trained several machine learning models:

Multinomial Logistic Regression
k-Nearest Neighbors (k-NN)
Decision Tree
Random Forest
Gradient Boosting Machine (GBM)
Stacked the models using glmnet to improve prediction accuracy.

## Model Evaluation:

Compared model performance using cross-validation and confusion matrices.
Analyzed accuracy, sensitivity, and specificity of each model.

### Results

The stacked model (combining Random Forest, Boosting, k-NN, Decision Tree, and Logistic Regression) provided the highest prediction accuracy. The performance of the models was evaluated on a validation set to ensure generalization to unseen data.

### Dependencies

The following R packages were used in the analysis:

DataExplorer
dplyr
randomForest
caret
ggplot2
rpart
rpart.plot
skimr
corrplot
caretEnsemble
pryr
gbm3
glmnet
You can install these packages using the following commands in R:

```
install.packages(c("DataExplorer", "dplyr", "randomForest", "caret", "ggplot2", 
                   "rpart", "rpart.plot", "skimr", "corrplot", "caretEnsemble", 
                   "pryr", "gbm3", "glmnet"))
```

# References
Human Activity Recognition (HAR) Weight Lifting Exercises Dataset: [link](https://web.archive.org/web/20161224072740/http:/groupware.les.inf.puc-rio.br/har)


