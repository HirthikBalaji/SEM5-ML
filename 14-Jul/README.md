# Machine Learning Evaluation Lab Summary

The laboratory experiments focusing on **Model Evaluation Metrics for Classification and Regression** have been completed successfully. Two versions of the pre-executed Jupyter Notebook have been compiled:

1.  **Full Report Notebook:** Contains aims, problem statements, LaTeX equations, code, outputs, and interpretations.  
    *   [Machine_Learning_Evaluation_Lab.ipynb](file:///Users/hirthikbalaji/Documents/SEM5/MACHINE%20LEARNING/LAB/14-Jul/Machine_Learning_Evaluation_Lab.ipynb)
2.  **Code and Output Only Notebook:** Contains only the code cells and their pre-computed outputs/visual plots.  
    *   [Machine_Learning_Evaluation_Lab_Code_Only.ipynb](file:///Users/hirthikbalaji/Documents/SEM5/MACHINE%20LEARNING/LAB/14-Jul/Machine_Learning_Evaluation_Lab_Code_Only.ipynb)

---

## Experiment 1: Disease Prediction (Binary Classification)

### Problem Statement
Evaluate a disease prediction system using actual and predicted diagnoses:
*   **Actual:** `[1, 1, 1, 0, 0, 0, 1, 0, 1, 0, 1, 0]`
*   **Predicted:** `[1, 0, 1, 0, 0, 1, 1, 0, 0, 0, 1, 0]`

### Calculated Metrics
*   **True Positives (TP):** 4
*   **True Negatives (TN):** 5
*   **False Positives (FP):** 1 (Type I error)
*   **False Negatives (FN):** 2 (Type II error)
*   **Precision:** $\frac{TP}{TP + FP} = \frac{4}{4 + 1} = 0.8000$ (80.00%)
*   **Recall:** $\frac{TP}{TP + FN} = \frac{4}{4 + 2} = 0.6667$ (66.67%)
*   **F1-Score:** $2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \\text{Recall}} = 0.7273$ (72.73%)
*   **Confusion Matrix:**
    $$\begin{pmatrix} 5 & 1 \\ 2 & 4 \end{pmatrix}$$

---

## Experiment 2: Spam Detection (Binary Classification from Text Labels)

### Problem Statement
Convert categorical labels to binary values (`Spam` $\rightarrow$ 1, `Not Spam` $\rightarrow$ 0) and evaluate the classifier:
*   **Actual:** `['Spam', 'Spam', 'Spam', 'Not Spam', 'Spam', 'Not Spam', 'Spam', 'Not Spam', 'Spam', 'Not Spam']`
*   **Predicted:** `['Spam', 'Spam', 'Not Spam', 'Not Spam', 'Spam', 'Spam', 'Spam', 'Not Spam', 'Spam', 'Not Spam']`

### Calculated Metrics
*   **Actual Binary:** `[1, 1, 1, 0, 1, 0, 1, 0, 1, 0]`
*   **Predicted Binary:** `[1, 1, 0, 0, 1, 1, 1, 0, 1, 0]`
*   **True Positives (TP):** 5
*   **True Negatives (TN):** 3
*   **False Positives (FP):** 1
*   **False Negatives (FN):** 1
*   **Precision:** $\frac{5}{5 + 1} = 0.8333$ (83.33%)
*   **Recall:** $\frac{5}{5 + 1} = 0.8333$ (83.33%)
*   **F1-Score:** $0.8333$ (83.33%)
*   **Confusion Matrix:**
    $$\begin{pmatrix} 3 & 1 \\ 1 & 5 \end{pmatrix}$$

---

## Experiment 3: Iris Dataset Multi-class Classification (Decision Tree)

### Problem Statement
1. Load the Iris dataset.
2. Split dataset (70% training, 30% testing).
3. Train a Decision Tree classifier.
4. Predict and evaluate performance using Scikit-learn.

### Calculated Metrics (Test Split)
*   **Overall Accuracy:** 1.0000 (100.0%)
*   **Weighted Precision:** 1.0000 (100.0%)
*   **Weighted Recall:** 1.0000 (100.0%)
*   **Weighted F1-Score:** 1.0000 (100.0%)
*   **Classification Report:**
    *   *Setosa:* Precision = 1.00, Recall = 1.00, F1-Score = 1.00
    *   *Versicolor:* Precision = 1.00, Recall = 1.00, F1-Score = 1.00
    *   *Virginica:* Precision = 1.00, Recall = 1.00, F1-Score = 1.00

---

## Experiment 4: Temperature Prediction (Regression Metrics)

### Problem Statement
Calculate MAE, MSE, and RMSE for daily temperature predictions:
*   **Actual:** `[30, 32, 31, 35, 36, 34, 33]`
*   **Predicted:** `[29, 33, 30, 34, 37, 35, 32]`

### Calculated Metrics
*   **Mean Absolute Error (MAE):** $1.0000\text{ }^\circ\text{C}$
*   **Mean Squared Error (MSE):** $1.0000\text{ }(^\circ\text{C})^2$
*   **Root Mean Squared Error (RMSE):** $1.0000\text{ }^\circ\text{C}$

---

## Experiment 5: Student Exam Marks (Regression Evaluation & Interpretation)

### Problem Statement
Evaluate final examination marks predictions and interpret results:
*   **Actual Marks:** `[78, 85, 90, 72, 88, 95, 80]`
*   **Predicted Marks:** `[80, 82, 89, 75, 86, 93, 79]`

### Calculated Metrics
*   **Mean Absolute Error (MAE):** $2.0000\text{ marks}$
*   **Mean Squared Error (MSE):** $4.5714\text{ marks}^2$
*   **Root Mean Squared Error (RMSE):** $2.1381\text{ marks}$

### Interpretation
1.  **MAE (2.0000):** On average, the model's predictions deviate from the actual marks by 2.0 marks.
2.  **MSE (4.5714):** A squared error metric useful for optimization; larger errors are penalized more heavily.
3.  **RMSE (2.1381):** Represents the standard deviation of residuals. Because $\text{RMSE} > \text{MAE}$, it confirms variance in error magnitudes (specifically, a few errors are slightly larger, such as predictions off by $\pm 3$).

---

## Visualizations Included in the Notebooks
1.  **Experiment 1:** Heatmap of the confusion matrix.
2.  **Experiment 2:** Heatmap of the spam classifier confusion matrix.
3.  **Experiment 3:** Visual tree structure of the trained Decision Tree.
4.  **Experiment 5:** Side-by-side bar chart showing Actual vs. Predicted student marks.

