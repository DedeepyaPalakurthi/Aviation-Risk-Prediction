# Trained Model Checkpoints Summary

This folder contains the final model checkpoints selected for the project:  
**"Predicting Aviation Risk: Explainable Injury and Damage Classification"**

---

## Models

### 1. Damage_DropoutBNN_elu_Epoch723_LR1e-02_Dim500.pt

- **Model Type:** Dropout Bayesian Neural Network  
- **Target:** Aircraft Damage Severity  
- **Activation:** ELU  
- **Hidden Dimensions:** 500  
- **Epochs:** 723  
- **Learning Rate:** 0.01  
- **Reason for Selection:**  
  Achieved the highest macro F1-score and demonstrated stable performance across evaluation folds.  
  Selected as the final model for damage classification.

---

### 2. Injury_AttentionBNN_sigmoid_Epoch675_LR1e-03_Dim500.pt

- **Model Type:** Attention-based Bayesian Neural Network  
- **Target:** Injury Severity Classification  
- **Activation:** Sigmoid  
- **Hidden Dimensions:** 500  
- **Epochs:** 675  
- **Learning Rate:** 0.001  
- **Reason for Selection:**  
  Delivered the best macro F1-score for injury prediction and showed consistent confidence across validation folds.  
  Chosen as the final model for injury severity.

---

These models are intended for predictive risk assessment, explainability through LIME/SHAP, and potential deployment in decision-support tools for aviation risk assessment.
