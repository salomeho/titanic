# Titanic Survival Prediction with Genetic Programming (DEAP)

## Project Overview
- Loaded Kaggle Titanic `train.csv` / `test.csv` and performed preprocessing and feature encoding.
- Cleaned missing values:
  - Filled numeric fields (e.g., Age/Fare) with dataset statistics.
  - Imputed categorical fields (e.g., Embarked/Cabin) using probability distributions derived from the data.
- Built baseline classifiers for comparison:
  - Decision Tree
  - Support Vector Machine (linear kernel)
  - Neural Network (MLPClassifier)
- Implemented a Genetic Programming pipeline with DEAP:
  - Defined a primitive set over Titanic features (Pclass, Sex, Age, SibSp, Parch, Fare, Cabin, Embarked).
  - Evolved candidate expressions (individuals) using crossover/mutation.
  - Evaluated individuals using a Pareto objective: minimize false positives and false negatives.
  - Visualized the Pareto front and computed an area-under-curve style summary for the front.
