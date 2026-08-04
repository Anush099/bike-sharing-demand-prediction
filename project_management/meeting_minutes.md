# Meeting Minutes

## Meeting 1

**Date:** 12 June  
**Student Name:** Anush Goud Akula  
**Project Title:** Predicting Urban Bike Sharing Demand Using Weather, Seasonal, and Calendar-Based Machine Learning Features  

### Discussion Points
- The supervisor explained the importance of maintaining meeting minutes for every meeting.
- The supervisor advised using GitHub to track project progress.
- The supervisor discussed proper referencing and bibliography management.
- The supervisor suggested keeping clear records of weekly tasks and agreed actions.

### Agreed Tasks
- Create a GitHub repository for the dissertation project.
- Add project management documents to GitHub.
- Upload the Gantt chart.
- Maintain meeting minutes after every supervisor meeting.
- Continue improving the research proposal.
- Start understanding the Seoul Bike Sharing Demand dataset.

### Progress Before Next Meeting
- GitHub repository created.
- README file added.
- Meeting minutes file added.
- Gantt chart and weekly progress log to be uploaded.





# Meeting 2 Minutes – 26 June

## Meeting Information

**Date:** 26 June
**Supervisor:** Jose Paredes
**Project Title:** Predicting Urban Bike Sharing Demand Using Weather, Seasonal, and Calendar-Based Machine Learning Features

## Project Discussion

The meeting included a discussion of the machine-learning approach being followed for the bike-sharing demand prediction project. It was confirmed that the project will use machine-learning algorithms to predict a numerical outcome from the available dataset.

The use of the Scikit-learn library was discussed. The student was advised to review the library because it provides several useful functions for dataset preprocessing, model training, validation, and performance evaluation.

## Training and Testing Strategy

The discussion explained the conventional method of dividing a dataset into training and testing portions. An example was provided in which approximately 80% of the data is used to train the algorithm and the remaining 20% is used to test its performance.

A repeated validation approach was also discussed. Instead of training and testing the model only once, the dataset may be divided into multiple sections so that different portions are used for training and validation across several iterations. This approach is related to cross-validation and can provide a more reliable estimate of model performance.

The supervisor agreed that this would be a sensible approach and encouraged the student to explore it.

## Data Normalisation and Preprocessing

The meeting highlighted that some numerical variables may require normalisation or standardisation because the dataset features may use different measurement scales.

It was also explained that categorical values cannot be interpreted directly by most machine-learning algorithms. Therefore, variables containing categories must be transformed into an appropriate numerical representation before model training.

The student was advised to select the encoding method based on the meaning and structure of each categorical variable.

## Missing-Data Handling

The possibility of missing values was discussed using humidity as an example. Where values are missing, suitable approaches such as mean-based imputation or interpolation may be considered.

The supervisor identified this process as interpolation and supported exploring suitable missing-data methods where required.

The Seoul Bike Sharing dataset was later checked and no missing values were found. Therefore, no interpolation or imputation was required for the current Seoul dataset. However, the procedure should still be checked when the parallel dataset is introduced.

## Agreed Actions

1. Review the Scikit-learn library and its available preprocessing and evaluation functions.
2. Continue cleaning and preparing the Seoul Bike Sharing Demand dataset.
3. Check all columns for missing values and duplicate records.
4. Convert categorical features into a suitable numerical format.
5. Consider normalisation or standardisation for numerical variables where appropriate.
6. Prepare an 80/20 train-test split for the later modelling stage.
7. Explore cross-validation to obtain a more reliable model-performance estimate.
8. Document the reasoning behind the selected preprocessing methods.
9. Continue updating GitHub with code, meeting minutes, outputs, and weekly progress.

## Work Completed After the Meeting

* The Seoul dataset was inspected and found to contain 8,760 hourly records.
* No missing values were identified.
* No duplicate records were identified.
* Column names were cleaned.
* Date-based features were extracted.
* Categorical variables were one-hot encoded.
* Weekend and peak-hour indicators were created.
* Exploratory data analysis was completed.
* The final preprocessed Seoul dataset was saved.
* The Introduction chapter was prepared.

## Tasks for the Next Week

* Select and download a parallel bike-sharing dataset from another city or country.
* Inspect and document the parallel dataset columns.
* Explain how the columns relate to the bike-sharing demand prediction problem.
* Identify comparable features between the Seoul and parallel datasets.
* Check missing values, duplicates, and categorical variables in the parallel dataset.
* Remove any variables that may result in target leakage.
* Prepare both datasets for train-test splitting, scaling, and cross-validation.




# Meeting 3 Minutes

## Meeting Information

**Date:** 17/07/26  
**Supervisor:** Jose Paredes  
**Student Name:** Anush Goud Akula  
**Project Title:** Predicting Urban Bike Sharing Demand Using Weather, Seasonal, and Calendar-Based Machine Learning Features  

## Project Discussion

The meeting focused on improving the evaluation stage of the bike-sharing demand prediction project. The supervisor suggested extending the project by using a parallel bike-sharing dataset in addition to the main Seoul Bike Sharing Demand dataset.

The purpose of using a parallel dataset is to check whether the machine learning workflow developed for the Seoul dataset can also perform effectively on another city’s bike-sharing data. This would strengthen the project by showing that the modelling approach is not limited only to one dataset.

The supervisor advised that the parallel dataset should be tested using the developed machine learning models. The performance of the models on the new dataset should then be analysed and discussed clearly, regardless of whether the results are strong or weak.

## Parallel Dataset Discussion

The Washington D.C. Bike Sharing Dataset was selected as the parallel dataset because it contains hourly bike rental demand records and includes time, calendar and weather-related variables. This makes it suitable for comparison with the Seoul Bike Sharing Demand dataset.

The supervisor suggested that the project should include:

1. Cross-validation using the parallel dataset.
2. A separate modelling study using the parallel dataset.
3. A clear comparison of how the developed models perform on both datasets.
4. A proper explanation of the results, even if the model performance differs between the datasets.

## Agreed Actions

1. Select a suitable parallel bike-sharing dataset.
2. Use the Washington D.C. Bike Sharing Dataset as the parallel dataset.
3. Inspect the dataset structure, columns and target variable.
4. Identify comparable features between the Seoul and Washington D.C. datasets.
5. Remove any columns that could cause target leakage.
6. Preprocess the parallel dataset separately.
7. Apply the same machine learning models used for the Seoul dataset.
8. Evaluate model performance using MAE, RMSE and R² score.
9. Perform cross-validation on the Washington D.C. dataset.
10. Compare the model results between Seoul and Washington D.C.
11. Explain the findings clearly in the Results and Evaluation chapter.
12. Update GitHub with the new dataset work, results, figures and meeting minutes.

## Work Completed After the Meeting

- The Washington D.C. Bike Sharing Dataset was selected as the parallel dataset.
- The dataset was downloaded and loaded into the notebook.
- Dataset columns, missing values and duplicate records were checked.
- No missing values or duplicate records were found.
- Leakage columns such as `casual` and `registered` were removed because they directly contribute to the target variable.
- Date-based features were created.
- Weekend and peak-hour indicators were created.
- Categorical columns were encoded.
- The same models were applied: Linear Regression, Random Forest, Gradient Boosting and XGBoost.
- Model evaluation was completed using MAE, RMSE and R² score.
- K-Fold cross-validation and time-series cross-validation were completed.
- Feature-importance analysis was completed.
- Seoul and Washington D.C. results were compared.
- A final comparative dashboard was created.

## Tasks for the Next Week

- Finalise the Washington D.C. parallel dataset results.
- Save all result tables and figures.
- Upload the updated notebook and output files to GitHub.
- Update the methodology chapter to include the parallel dataset workflow.
- Write the Results and Evaluation chapter using the Seoul and Washington D.C. outputs.
- Include the final comparative dashboard in the report.
- Explain clearly that RMSE values should not be directly compared across datasets because the rental-count scales are different.
- Use R² score as the safer high-level metric for comparing both datasets.
