# ecg-heartbeat-classifier
ECG heartbeat classification using machine learning and the MIT-BIH Arrhythmia Database.
# ECG Heartbeat Classifier

## About the Project

This project is about using machine learning to classify ECG (Electrocardiogram) heartbeats as normal or abnormal. I developed this project using Python to understand how machine learning can identify patterns in ECG signals.

I worked on preparing the dataset, training different machine learning models, comparing their performance, and visualizing the heartbeat data. Through this project, I wanted to gain practical experience in machine learning and understand how it can be applied to healthcare-related data.

This project is created for learning and educational purposes. It is not intended to diagnose any medical condition.

## Dataset

This project uses the **MIT-BIH Arrhythmia Database**, which contains ECG recordings used for research and experimentation.

- ECG signals are processed using the WFDB library.
- The data is prepared for machine learning classification.
- Training samples: 80,509
- Testing samples: 20,196

## Technologies Used

- Python
- Google Colab
- VS Code
- NumPy
- Pandas
- SciPy
- Matplotlib
- Scikit-learn
- WFDB

## Project Workflow

1. Load the ECG dataset.
2. Process and prepare the heartbeat data.
3. Split the data into training and testing sets.
4. Train different machine learning models.
5. Evaluate and compare model performance.
6. Visualize heartbeat patterns using PCA.

## Machine Learning Models

I trained and compared the following models:

- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest
- Logistic Regression

## Model Evaluation

I evaluated the models using Precision, Recall, F1-score, F1-score standard deviation, ROC-AUC, and execution time. These metrics help compare classification performance, consistency, ability to identify abnormal heartbeats, and computational efficiency.

| Model | Precision | Recall | F1-score | F1 Std | ROC-AUC | Time (seconds) |
|---|---:|---:|---:|---:|---:|---:|
| Random Forest | 0.630770 | 0.638281 | 0.605727 | 0.215047 | 0.885505 | 299.1117 |
| Logistic Regression | 0.432791 | 0.812818 | 0.531595 | 0.230413 | 0.874943 | 33.42848 |
| SVM (RBF) | 0.366016 | 0.837801 | 0.473886 | 0.210443 | 0.876739 | 50.5388 |
| KNN (k=5) | 0.321533 | 0.706003 | 0.432595 | 0.128085 | 0.796104 | 28.40421 |

### Key Observations

- **Random Forest:** Achieved the highest F1-score (0.605727) and ROC-AUC (0.885505), but required the longest execution time, approximately 299 seconds.
- **Logistic Regression:** Provided a good balance between recall (0.812818) and execution time (33.43 seconds).
- **SVM (RBF):** Achieved the highest recall (0.837801), making it the strongest model among these experiments for identifying abnormal-class samples, based on recall.
- **KNN (k=5):** Had the shortest execution time (28.40 seconds), but achieved the lowest ROC-AUC (0.796104) and F1-score (0.432595).

## PCA Visualization

I used Principal Component Analysis (PCA) to visualize the heartbeat data in two dimensions. This helps explore how normal and abnormal heartbeat samples are distributed.

## How to Run the Project

### Using Google Colab

1. Open `ECG_Heartbeat_Classifier.ipynb` in Google Colab.
2. Make sure the MIT-BIH dataset is available in your Google Drive.
3. Update the dataset path if required.
4. Run the notebook cells in order.
5. Review the model results and visualizations.

### Using VS Code

1. Install Python and the Jupyter extension in VS Code.
2. Install the required libraries:

   `pip install numpy pandas scipy matplotlib scikit-learn wfdb`

3. Download or access the MIT-BIH dataset.
4. Update the dataset path in the notebook.
5. Open the notebook and run the cells in order.

## What I Learned

While working on this project, I learned how to process ECG data, prepare datasets, train different machine learning models, evaluate their performance, and visualize data using PCA.

Comparing different models also helped me understand why accuracy alone is not always enough to evaluate a classification model.

## Future Improvements

- Improve ECG signal preprocessing.
- Experiment with additional machine learning algorithms.
- Perform hyperparameter tuning and cross-validation.
- Analyze confusion matrices and class-wise performance.
- Test the models on independent datasets.
- Explore deep learning techniques for ECG classification.

## Disclaimer

This project is developed for educational purposes only. It is not a medical device and should not be used to diagnose or make decisions about any person's health.

## Author

**Shreejith M K**
