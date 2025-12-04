# AI-for-Early-Detection-of-Cardiovascular-Events

## BACKGROUND                                                                                                              
Cardiovascular diseases (CVDs) remain the leading cause of morbidity and mortality in the US and globally. A major portion of the CVD events, such as stroke and Heart Attack, occur unwitnessed, delaying treatment and increasing the risk of death or disability. The delayed detection and management of these CVD events increases the cost of medical care which is associated with poor prognosis. However, timely detection and alerts to caregivers or emergency responders could help reduce treatment delays and facilitate a faster recovery.
Artificial Intelligence (AI) offers the opportunity to leverage real-time monitoring data from wearable devices to detect major events and alert the caregivers and emergency services for prompt responses

<img width="1146" height="542" alt="image" src="https://github.com/user-attachments/assets/c7765e72-4ae8-4814-a9e2-08d93e8dae60" />

## OBJECTIVES
1. Develop an AI-powered system for early detection of cardiovascular events (stroke & heart attack).
2. Implement automated alerts for caregivers and emergency responders to ensure a timely and effective response.

## HYPOTHESES                                                                                                             
1. Primary: An AI-powered system integrating real-time data from wearable devices can accurately detect early signs of cardiovascular events (e.g., stroke, myocardial infarction) with higher sensitivity and specificity >95%.
2. Secondary: Automated alert delivery to patients, caregivers, and emergency responders reduces the time-to-intervention for cardiovascular emergencies, thereby improving patient outcomes and survival rates.

## DATASET                                                                                                                                             
The dataset is taken from Kaggle, which was extracted from MIMIC III. It consists of 23,468 samples.                                                                                                                                          Features used include heart rate, blood pressure, SpO2, respiratory rate, and temperature. Target labels are 0 and 1, indicating the absence or presence of a CVD event, respectively.

<img width="2100" height="584" alt="image" src="https://github.com/user-attachments/assets/8ecbd3b5-2854-4a75-8182-6da4711209d5" />

## Machine Learning Models                                                                                                               
1. Logistic Regression: A good and computationally efficient baseline model for binary classification tasks. 
2. Decision Trees:  A simple ensemble algorithm noted for capturing non-linear relationships between features.
3. Random Forest: An ensemble method that combines multiple decision trees. This often leads to improved accuracy and robustness compared to a single decision tree.
4. Extreme Gradient Boosting: A gradient boosting algorithm known for its high performance and ability to handle complex datasets.


## Train-Test Split and Cross Validation

Train-Test-Split: The data was split into training (80%) and testing (20%) sets using train_test_split with random_state=42
Cross-Validation:  To get a more robust evaluation of model performance by splitting the data into multiple folds and running the model on different combinations of these folds. This helps to reduce the impact of a single train/test split and provides a better estimate of how the model will perform on unseen data. A 10-fold cross-validation was used to validate the models adequately.

## Cross-Validation Results (10-fold)
Cross-validation confirmed the strong performance of the tree-based models (Decision Tree, Random Forest, and XGBoost) with mean ROC-AUC scores very close to 1.0000 and low standard deviations, indicating robust performance across different subsets of the data. Logistic Regression had the lowest ROC-AUC


<img width="979" height="707" alt="image" src="https://github.com/user-attachments/assets/a1bc961a-0ece-446f-8098-028aff9a1b3f" />


## Models Performance
Evaluation Metrics: Models were evaluated using Accuracy, Precision, Recall (Sensitivity), F1-score, ROC-AUC, and Specificity on the test set, and Mean ROC-AUC (CV) and Standard Deviation ROC-AUC (CV) from 10-fold cross-validation.

<img width="1095" height="805" alt="image" src="https://github.com/user-attachments/assets/557a55b6-c710-49ff-9f37-7f8a6631f249" />

## Best Performing Models
Both Decision Tree and Random Forest models achieved perfect or near-perfect scores (1.0000) across most metrics on the test set, including Accuracy, Precision, Recall, F1-score, and ROC-AUC. XGBoost also performed exceptionally well

<img width="979" height="682" alt="image" src="https://github.com/user-attachments/assets/3eea8f99-acbf-4bbc-9252-359cd98ca103" />

## Overfitting Analysis
Training accuracy and ROC-AUC scores were calculated for all trained models.
The difference between training and testing scores for all models was found to be very small (less than 0.05 for both accuracy and ROC-AUC), indicating no significant overfitting.  

<img width="979" height="417" alt="image" src="https://github.com/user-attachments/assets/09cdf896-c921-48cf-9b88-f1960c6f82f3" /> <img width="926" height="381" alt="image" src="https://github.com/user-attachments/assets/d3f167f4-8ca9-4ea0-9471-ce19a4ac9287" />

## Correlation Heatmap
The correlation heatmap visualizes the pairwise correlations between the features in the dataset. Each cell in the heatmap represents the correlation coefficient between two features.                                 

<img width="979" height="555" alt="image" src="https://github.com/user-attachments/assets/4acb7300-8391-4f9f-8349-599bf595739e" />

<img width="1924" height="1011" alt="image" src="https://github.com/user-attachments/assets/713f5e88-d071-43bf-94c4-711697b948c9" />

## CONCLUSION
1. This research demonstrates that integrating AI-powered predictive modeling with wearable devices and interoperable health data systems can provide real-time detection of cardiovascular emergencies such as strokes and heart attacks. By linking patient-generated health data to a cloud-based AI engine and delivering timely alerts to patients, caregivers, and emergency responders, the system addresses a critical gap in early recognition of unwitnessed events
2. The proposed solution not only enhances patient safety and outcomes but also reduces delays in treatment, potentially lowering morbidity and mortality. Furthermore, the feedback loop into EHRs ensures continuous learning and system improvement, making the platform adaptive and scalable.


## SIGNIFICANCE AND IMPACT                                                                                                    
1. Quality of Care: Early detection and intervention directly translate into better recovery, reduce complications, and improve patient and caregiver satisfaction
2. Access to Care: As a digital safety net, the system ensures that a timely emergency response is available for vulnerable populations without robust social support.
3. Population Health Impact: By addressing the 25-36 % of unwitnessed strokes and up to 45% of silent MI, the system targets a substantial fraction of cardiovascular events.
4. Healthcare System Efficiency: Early interventions reduce the high costs associated with delayed treatment and complications               












