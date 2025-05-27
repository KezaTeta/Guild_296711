# **Guilds Dataset Analysis and Prediction**

## **Team Members**
- Keza Teta Sandra Carine - 296711
- Zuhal Bobrek - 296981
- Sunandan Mahajan - 305351

---

## **[Section 1] Introduction**
This project focuses on a comprehensive analysis of the Guilds dataset, with the central objective of predicting individuals' connections within the distinct guild categories (`No_Guild`, `Master_Guild`, or `Apprentice_Guild`). Using advanced machine learning techniques, the goal is to build a robust classification model based on features like magical potential, stamina, and experience. The primary objective is a detailed demonstration of data preprocessing methodologies, thorough exploratory data analysis (EDA) and the systematic approach of machine learning models can accurately classify guild memberships and identify key features driving the predictions. This work shows how structured data analysis and machine learning can effectively address complex classification problems and provide actionable insights. This work demonstrates the practical power of structured data analysis and machine learning in tackling complex classification challenges and revealing actionable insights from multifaceted data. Our ultimate goal is to provide the Council of Marendor with a powerful tool to anticipate guild assignments and strategically guide the kingdom's future progress.

---

## **[Section 2] Methods**

### **Proposed Ideas**
Our approach involved strategic feature selection and the application, unraveling the mysteries of guild membership was guided by a rigorous evaluation of powerful algorithms. It is also supported by ideal choices for data handling.
1. **Feature Selection:** 
   - Features identified as highly correlated with the target variable, `Guild_Membership`, were prioritized. The prioritized ones were `Fae_Dust_Reserve`, `Mystical_Index`, and `Rune_Power` due to their strong correlation with the target variable (`Guild_Membership`).
2. **Algorithms:** 
Three distinct classification algorithms were chosen:
   - Random Forest Classifier
   - AdaBoost Classifier
   - Gradient Boosting Classifier

   The classifiers that we initially intended on using which are KNN and SVM classifiers are not included in our project as we were not able to run them properly due to the size of our dataset. With the help of AI tools and the internet, we searched for other appropriate classifiers. We chose the classifiers AdaBoost and Gradient Boosting because they are more suitable for the size of our dataset, even though they might have limitations that will be discussed further in the report. 
3. **Design Choices:**
   - **Imputation:** Missing values in numerical features were handled using the median. For categorical features, the most frequent value was used.
   - **Encoding:** Categorical features were encoded to a numerical format compatible with machine learning algorithms.


## **[Section 3] Experimental Design**

### **Purpose**
The primary purpose of this experiment was to predict guild memberships accurately and to evaluate the contribution of various features to model performance.

### **Baseline**
A Random Forest model was used with its default parameters as the baseline for performance comparison. This provided a standard against all other algorithms.

### **Evaluation Metrics**
- **Accuracy:** To evaluate the models, ("\nModel Performance") and accuracy_score was used to measure the overall proportion of correct predictions.
- **Confusion Matrix:** To evaluate model predictions and misclassifications.
- **F1-Score:** To balance precision and recall for each guild category, especially for underrepresented ones.

---

## **[Section 4] Results**

### **Main Findings**

#### **Accuracy Scores**
The performance of the evaluated models is summarized by their achieved accuracy scores:
- **Random Forest:** 85.78%
- **AdaBoost:** 85.74%
- **Gradient Boosting:** 85.86%

#### **Best Model**
- Gradient Boosting achieved the highest predictive accuracy with the score **85.86%**, making it the most effective model for predicting guild memberships.

### **Confusion Matrix**
The confusion matrix below illustrates the Random Forest model's performance:

![Confusion Matrix](image/cf.png)
(This figure presents the confusion matrix for the Random Forest model, detailing the distribution of actual versus predicted guild memberships.)

### **Feature Importance**
The top three predictors of guild membership are identified below:
1. `Rune_Power`
2. `Mystical_Index`
3. `Fae_Dust_Reserve`

The plot below shows feature importance as determined by the Random Forest model:

![Feature Importance](image/features.png)
(This figure displays the feature importance, highlighting the most impactful variables for guild prediction.)
---

## **[Section 5] Conclusions**

### **Takeaway Points**
Our analysis confirms that Gradient Boosting is the most effectiev algorithm for predicting guild memberships in the provided dataset, achieving **85.86% accuracy**. The study also shows the significant predictiveness of features such as `Rune_Power`, `Mystical_Index`, and `Fae_Dust_Reserve` in predicting guild membership.

### **Limitations and Future Work**

#### **Limitations**

Despite the successful outcomes, some possible limitations were identified. One notable challenge we encountered was the inherent class imbalance within the dataset, particularly affecting predictions for smaller guild categories (e.g., `Apprentice_Guild`). The reason for it is because we were not able to use KNN and SVM which would have been more optimal for smaller categories like Apprentice Guild. This can lead to models being overly biased towards the majority classes, potentially underperforming on the smaller ones.
Another possible limitation is missing data imputation bias. Despite our careful selection of imputation methods (median for numeric, mode for categorical), it may introduce a degree of bias into the dataset, potentially influencing model outcomes. 

#### **Future Directions**

To adrdess the impact of imbalanced classes, advanced oversampling techniques like SMOTE (Synthetic Minority Over-sampling Technique) might be explored. This would generate synthetic examples for underrepresented classes, providing a more balanced dataset for our models to learn from. Dataset expansion could also be, the integration of additional datasets or the engineering of new features to enrich the predictive capability of the models. Also, exploring the application of deep learning models to leverage their capacity for automatic feature extraction and handling of complex, non-linear relationships within the data.



---

## **Figures and Artifacts**

### **Figures**
- **Confusion Matrix:** `image/cf.png`
- **Feature Importance:** `image/features.png`

### **Code and Notebooks**
- All analysis and model implementation can be found in `main.ipynb`.
