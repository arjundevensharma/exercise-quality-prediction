# Exercise Quality Prediction from Accelerometer Data

This project uses machine learning to predict the quality of weight lifting exercises based on accelerometer data from sensors placed on the belt, forearm, arm, and dumbbell of 6 participants.

## Project Overview

Using devices such as Jawbone Up, Nike FuelBand, and Fitbit, it's now possible to collect large amounts of data about personal activity relatively inexpensively. This project analyzes data from accelerometers to predict how well participants performed barbell lifts.

The participants performed barbell lifts correctly and incorrectly in 5 different ways:
- Class A: Exactly according to specification
- Class B: Throwing elbows to the front
- Class C: Lifting the dumbbell only halfway
- Class D: Lowering the dumbbell only halfway
- Class E: Throwing the hips to the front

## Files

- `exercise_analysis.Rmd`: R Markdown source file containing the complete analysis
- `exercise_analysis.html`: Compiled HTML report with results and visualizations
- `pml-training.csv`: Training dataset with 19,622 observations
- `pml-testing.csv`: Test dataset with 20 observations for final predictions

## Analysis Summary

The analysis includes:
- Data preprocessing and cleaning
- Exploratory data analysis with correlation plots
- Implementation of multiple machine learning models:
  - Decision Trees
  - Random Forest
  - Gradient Boosting
- Model comparison and selection
- Cross-validation strategy
- Out-of-sample error estimation
- Final predictions on test data

## Results

The Random Forest model achieved the best performance with:
- **99.5% accuracy** on the validation set
- **0.5% expected out-of-sample error**
- Robust performance across 5-fold cross-validation

## View the Analysis

You can view the complete analysis online at:
[https://arjundevensharma.github.io/exercise-quality-prediction/](https://arjundevensharma.github.io/exercise-quality-prediction/)

## Data Source

The data for this project comes from:
[Human Activity Recognition - Weight Lifting Exercise Dataset](http://web.archive.org/web/20161224072740/http:/groupware.les.inf.puc-rio.br/har)

## Reproducibility

To reproduce this analysis:
1. Clone this repository
2. Ensure you have R with the following packages installed:
   - caret
   - randomForest
   - corrplot
   - rpart
   - rpart.plot
   - gbm
   - rmarkdown
   - knitr
3. Run `rmarkdown::render('exercise_analysis.Rmd')` to generate the HTML report
