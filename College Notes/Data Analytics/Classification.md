# Lecture 3: Classification Process
**Instructor:** Aurelia Power  
**Year:** 2024  
**Course:** H4030 Data Analytics  

---

## **Topics Covered**
1. Approaches to learning.
2. What is classification?
3. Training a classifier and generating test sets:
   - Training and test datasets
   - Holdout and Cross Validation
4. Evaluating a classifier:
   - Accuracy
   - Precision
   - Recall

---

## **Approaches to Learning**
### Supervised Learning
1. **Classification:** Predicts a class/category for instances.
2. **Regression:** Predicts numerical values for instances.

### Unsupervised Learning
1. **Clustering:** Groups similar instances.
2. **Association:** Finds relationships between items.

---

## **Classification**
- Assigns objects to predefined categories (class labels).
- **Goal:** Build a model to assign correct classes to instances based on attributes.
- **Applications:** Predictive modeling, descriptive modeling.

### Common Algorithms
- Decision Trees
- Neural Networks
- Naïve Bayes
- Support Vector Machines (SVM)
- k-Nearest Neighbors (k-NN)

---

## **Criteria to Evaluate Classification Algorithms**
1. **Predictive performance:** How accurately it predicts unseen data.
2. **Speed and scalability:** Time to construct and use the model.
3. **Robustness:** Ability to handle noise and missing values.
4. **Interpretability:** How understandable the model is.
5. **Data compatibility:** Types of data it can handle.

---

## **Decision Trees for Classification**
1. Supervised learning method for classification and regression.
2. Learns decision rules from data features.
3. Outputs a model capable of labeling unseen data.
4. Uses a tree structure:
   - Nodes represent conditions.
   - Leaves represent class labels.

### Example Table

```markdown
| Tid | Refund | Marital Status | Taxable Income | Cheat |
|-----|--------|----------------|----------------|-------|
| 1   | Yes    | Single         | 125K           | No    |
| 2   | No     | Married        | 100K           | No    |
| 3   | No     | Single         | 70K            | No    |
| 4   | Yes    | Married        | 120K           | No    |
| 5   | No     | Divorced       | 95K            | Yes   |
```


---

# Classification Process

1. Split dataset into **training** and **test** datasets.
2. Train the model using the training set.
3. Evaluate performance on the test set.
4. Adjust model or preprocessing steps and repeat until satisfied.

---

# Overfitting vs. Underfitting

- **Underfitting:** Model is too simple, fails to capture data complexity.
- **Overfitting:** Model is too complex, memorizes training data but fails on unseen data.

| Error Type    | Description                                        |
| ------------- | -------------------------------------------------- |
| Underfitting  | Both training and test errors are high.            |
| Overfitting   | Training error is low, but test error is high.     |
| Best Mode Fit | Balanced between low training and low test errors. |

---

# Model Evaluation

## Confusion Matrix

The confusion matrix helps evaluate a classifier's performance by comparing actual and predicted labels.

| Predicted Class | Yes                  | No                   |
| --------------- | -------------------- | -------------------- |
| **Actual Yes**  | True Positives (TP)  | False Negatives (FN) |
| **Actual No**   | False Positives (FP) | True Negatives (TN)  |

---

### **Performance Metrics**

1. **Accuracy:** Proportion of correctly classified instances.

$$
		\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
$$

2. **Precision:** Proportion of predicted positive cases that are correct. 
  $$ \text{Precision} = \frac{TP}{TP + FP} $$

3. **Recall (Sensitivity)**: Proportion of actual positive cases correctly predicted. 
  $$ \text{Recall} = \frac{TP}{TP + FN} $$
4. **F1 Score**: Harmonic mean of precision and recall. 
 $$ F1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}} $$

---


### **Example Confusion Matrix** 

Given a classifier's predictions:

| Predicted Class | Yes | No  |
| --------------- | --- | --- |
| **Actual Yes**  | 1   | 1   |
| **Actual No**   | 2   | 3   |

#### Calculations:

- **Accuracy:** $$ \text{Accuracy} = \frac{1 + 3}{1 + 1 + 2 + 3} = 0.57 \, \text{(or 57\%)} $$
- **Recall (Yes):** $$ \text{Recall} = \frac{1}{1 + 1} = 0.5 \, \text{(or 50\%)} $$
- **Recall (No):** $$ \text{Recall} = \frac{3}{3 + 2} = 0.6 \, \text{(or 60\%)} $$
- **Precision (Yes):** $$ \text{Precision} = \frac{1}{1 + 2} = 0.33 \, \text{(or 33\%)} $$
- **Precision (No):** $$ \text{Precision} = \frac{3}{3 + 1} = 0.75 \, \text{(or 75\%)} $$

---
