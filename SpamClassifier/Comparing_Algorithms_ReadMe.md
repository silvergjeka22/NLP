
# Comparing Algorithms: Naive Bayes, FFNN, and MLP

This README file provides an in-depth explanation of a study comparing the performance of Naive Bayes, Feed-Forward Neural Networks (FFNN), and Multi-Layer Perceptrons (MLP) for spam detection tasks. The analysis demonstrates why FFNN and MLP outperform Naive Bayes in this domain.

---

## Overview

Spam detection involves identifying whether an email is spam or not based on its content and metadata. The dataset used in this study contains a linear structure with labeled examples of **spam** and **non-spam** emails. The algorithms were evaluated based on key performance metrics such as precision, F1 score, and confusion matrix.

### Dataset Structure

- **Number of emails:** Large dataset containing both spam and non-spam samples.
- **Features:** Textual features and metadata extracted from emails.
- **Labels:** Binary classification (“Spam” or “Non-Spam”).

---

## Performance Evaluation

### General Results:

| Algorithm       | Precision (%) | F1 Score | Confusion Matrix       |
| --------------- | ------------- | -------- | ---------------------- |
| **Naive Bayes** | 89.18         | 0.80     | [[702, 37], [75, 221]] |
| **FFNN**        | 98.07         | 0.97     | [[727, 12], [8, 288]]  |
| **MLP**         | 97.68         | 0.96     | [[722, 17], [7, 289]]  |

#### Performance Metrics:

- **Precision:** Measures the proportion of true positives among all positive predictions.
- **F1 Score:** Harmonic mean of precision and recall, capturing the balance between false positives and false negatives.
- **Confusion Matrix:** Summarizes classification results into true positives (TP), true negatives (TN), false positives (FP), and false negatives (FN).

---

## Why FFNN and MLP Perform Better than Naive Bayes

### **1. Naive Bayes**

Naive Bayes uses probability and assumes:

1. **Feature Independence:** All features are treated as independent, which simplifies computation but fails to capture interactions.
2. **Linear Decision Boundaries:** Performs well on linearly separable datasets but struggles with non-linear relationships.

#### Key Limitations:

- Assumes text features (e.g., word frequencies) are independent, which is unrealistic in spam detection where words often appear in correlated patterns.
- Relies on simplistic models of feature relevance, limiting its performance in complex scenarios.

**Performance Summary:**
While Naive Bayes is computationally efficient, it lacks the flexibility to model intricate patterns, leading to lower accuracy in spam detection tasks.

---

### **2. Feed-Forward Neural Network (FFNN)**

FFNNs utilize multiple layers of neurons to model complex relationships. Key strengths include:

#### Key Features:

- **Non-Linear Activation Functions:** Allow the network to learn non-linear patterns in the data.
- **Hidden Layers:** Enhance the network’s ability to detect feature interactions and dependencies.

#### Advantages Over Naive Bayes:

- Models feature dependencies explicitly.
- Captures non-linear interactions, improving its ability to classify spam accurately.

**Performance Summary:**
FFNN achieved the highest precision and F1 score in this study, demonstrating its robustness in handling complex spam detection tasks.

---

### **3. Multi-Layer Perceptron (MLP)**

The MLP builds on FFNN architecture by incorporating more hidden layers and neurons, enabling better generalization and feature learning.

#### Key Features:

- **Deep Learning Architecture:** Includes additional hidden layers for extracting abstract feature representations.
- **Generalization Ability:** Adapts well to varied and complex datasets.

#### Advantages Over Naive Bayes:

- Provides a richer representation of features through hierarchical learning.
- Outperforms in scenarios where feature interactions are sparse or noisy.

**Performance Summary:**
While slightly less precise than FFNN in this specific experiment, MLP remains a powerful choice for spam detection.

---

## Visual Explanation of Results

### Naive Bayes:


*Naive Bayes assumes linear separability, which fails to capture non-linear relationships in spam data.*

### FFNN and MLP:


*FFNN and MLP capture complex, non-linear patterns through multi-layered architectures.*

---

## Conclusion

### Key Takeaways:

- **Naive Bayes:** Efficient but limited by feature independence assumptions.
- **FFNN and MLP:** Superior in capturing non-linear relationships and feature dependencies.

### Recommendations:

For spam detection and similar tasks involving complex, interdependent patterns:

1. Use **FFNN** or **MLP** to achieve higher accuracy and F1 scores.
2. Reserve **Naive Bayes** for scenarios where simplicity and speed are prioritized over accuracy.

---

## Future Work

- Experiment with additional deep learning models (e.g., LSTM, CNN) for enhanced text feature extraction.
- Incorporate domain-specific pre-processing techniques, such as Natural Language Processing (NLP) methods.

---

Thank you for exploring this comparative study. Feel free to reach out for further discussion or collaboration!
