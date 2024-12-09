# Comparing Algorithms: Naive Bayes, FFNN, and MLP

This is a study that shows why Naive Bayes is worse than the Feed-Forward Neural Network (FFNN) and Multi-Layer Perceptron (MLP) in the performance of the given spam detection task.

## 1. **Performance Evaluation**

### General Overview of the Results:

| Algorithm           | Precision (%) | F1 Score | Confusion Matrix        |
|---------------------|----------------|----------|------------------------|
| **Naive Bayes**     | 89.18          | 0.80     | [[702, 37], [75, 221]] |
| **FFNN**            | 98.07          | 0.97     | [[727, 12], [8, 288]]  |
| **MLP**             | 97.68          | 0.96     | [[722, 17], [7, 289]]  |

---

## 2. **Why FFNN and MLP Performed Better than Naive Bayes**

### **2.1 Naive Bayes**

Naive Bayes operates on certain assumptions that hinder its ability to generalize well in complex datasets such as spam detection. These assumptions include:

- **Feature Locality Assumption**: Naive Bayes assumes that all features are independent of one another to simplify computations. While this reduces complexity, it fails to capture real-world feature interdependencies.
  
- **Sequential Bias on the Target Variable**: Naive Bayes performs exceptionally well on linearly separable datasets. However, in situations like spam detection, where patterns are highly interdependent and complex, this assumption fails.

**Conclusions on Performance:**

Despite its speed and simplicity, Naive Bayes has limitations in handling non-linear relationships. Spam detection requires capturing patterns between multiple features that interact in a non-linear way, which Naive Bayes cannot effectively model.

---

### **2.2 Feed-Forward Neural Network (FFNN)**

Feed-Forward Neural Networks demonstrate superior performance due to their ability to capture non-linear relationships through a multi-layered architecture. Some of the key reasons for their success include:

- **Non-Linear Learning Mechanism**: FFNNs use non-linear activation functions across multiple hidden layers to learn intricate feature patterns. Unlike Naive Bayes, they do not rely on feature independence or overly simplistic statistical assumptions.
  
- **Feature Interaction Modeling**: The FFNN's ability to interactively learn combinations of features allows it to uncover patterns in complex, multi-dimensional data, a capability that Naive Bayes lacks.

These attributes explain why FFNNs achieve 98.07% accuracy and a higher F1 Score of 0.97 compared to Naive Bayes.

---

### **2.3 Multi-Layer Perceptron (MLP)**

The Multi-Layer Perceptron (MLP) builds on the principles of the FFNN but introduces additional layers to further increase its ability to generalize from data. Key reasons MLP performs better include:

- **Deeper Neural Architecture**: MLPs consist of multiple layers of neurons, enabling them to capture more intricate, abstract relationships between features than FFNNs or Naive Bayes can.
  
- **Feature Generalization**: MLPs generalize better across varied examples in spam detection, even when feature interactions are sparse or inconsistent.

The MLP achieves an accuracy of **97.68%** and an F1 Score of **0.96**, showing that even with a slightly different architecture than FFNN, MLP performs at comparable levels.

---

## 4. **Conclusion**

- **FFNN and MLP outperform Naive Bayes** because they can model non-linear relationships and feature interactions, critical for accurately detecting spam patterns.
- **Naive Bayes**, while efficient and interpretable, assumes feature independence and fails to capture the complexities and dependencies in real-world spam data.
- Neural networks like **FFNN and MLP** trade-off computational cost for improved accuracy by learning intricate, non-linear feature interactions.

When facing robust datasets with non-linear relationships like spam detection, **FFNN and MLP** are superior choices for classification tasks.
