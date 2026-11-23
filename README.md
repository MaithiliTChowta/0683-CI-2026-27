ASSIGNMENT
Exploratory Data Analysis & Feature Engineering
for Flight Price Prediction
Individual Practical Assignment
Assignment Type	Individual	Primary Tools	Python, Pandas, NumPy
Libraries	Matplotlib, Seaborn, Scikit-learn	Submission	Jupyter Notebook (.ipynb)
1. Problem Statement
Airline ticket prices can vary depending on factors such as the airline, journey route, departure and arrival timings, travel duration, number of stops, travel date, and booking lead time. In this assignment, you will work with a flight-price dataset to understand its structure, identify patterns and data-quality issues, and transform raw columns into useful features for a potential flight-price prediction task.
2. Objective
Perform Exploratory Data Analysis (EDA) and Feature Engineering on the Flight Price Prediction dataset. The objective is to prepare an analysis-ready dataset and explain the decisions made during cleaning and transformation.
3. Dataset
Dataset: Flight Price Prediction
Kaggle link: https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction
Use the flight dataset associated with the provided reference notebook. Download the dataset from Kaggle and load the relevant Excel/CSV file into your notebook. Do not assume that the notebook's intermediate outputs will be available in your environment.
4. Dataset Features
Feature	Description
Airline	Name of the airline; categorical.
Date_of_Journey	Date on which the journey takes place; raw date field.
Source	City from which the flight departs; categorical.
Destination	City where the flight arrives; categorical.
Route	Sequence of route locations; categorical/text field.
Dep_Time	Departure time; raw time field.
Arrival_Time	Arrival time; may contain additional date text for overnight journeys.
Duration	Total travel duration, represented using hours and/or minutes.
Total_Stops	Number of stops between source and destination.
Additional_Info	Additional flight information; categorical/text field.
Price	Flight ticket price; target variable for the prediction context.
5. Tasks to be Performed
Task 1 – Data Loading and Initial Inspection
•	Import the required Python libraries and load the dataset into a Pandas DataFrame.
•	Display the first five and last five records.
•	Inspect the shape, column names, data types, and non-null counts using suitable Pandas methods.
•	Generate descriptive statistics for numerical columns and inspect unique values in categorical columns.
•	Write a brief observation about the dataset structure.
Task 2 – Data Quality Assessment
•	Identify missing/null values in every column and report their counts.
•	Check for duplicate records and decide whether any duplicates should be removed. Explain your decision.
•	Inspect inconsistent labels, unexpected values, and columns that may contain mixed formats.
•	Identify possible outliers or unusually high/low values in the Price and other numeric features. Use suitable summaries or visualizations.
•	Document each issue found and the action taken. Do not silently replace values without justification.
Task 3 – Exploratory Data Analysis (EDA)
•	Analyze the distribution of the target variable Price using suitable numerical summaries and visualizations.
•	Study the number of flights and price patterns across Airline.
•	Compare prices across Source and Destination cities.
•	Explore the relationship between Total_Stops and Price.
•	Explore how departure time, arrival time, journey date/month, and Duration relate to ticket prices.
•	Use appropriate plots such as count plots, bar plots, histograms, box plots, and correlation heatmaps where applicable.
•	Write at least five meaningful observations supported by your analysis. Avoid describing a chart without explaining its insight.
Task 4 – Date and Time Feature Engineering
•	Split Date_of_Journey into day, month, and year components and convert them to appropriate numeric data types.
•	After validating the extracted values, remove the original date column if the new features preserve the information required for analysis.
•	Extract hour and minute components from Dep_Time.
•	Clean Arrival_Time carefully before extracting its hour and minute components. Account for values that include an additional date portion.
•	Convert extracted hour and minute features to numeric data types and validate the resulting ranges.
•	Explain why the original time columns may be dropped after successful extraction.
Task 5 – Stops and Duration Transformation
•	Inspect all distinct values in Total_Stops, including missing values.
•	Convert stop descriptions such as non-stop, 1 stop, and 2 stops into a numeric representation.
•	Handle missing stop information using a reasoned approach. If you use mode or another imputation method, state why it is appropriate and acknowledge the assumption.
•	Convert Duration into a numeric feature, preferably total duration in minutes. Correctly handle hour-only, minute-only, and hour-plus-minute formats.
•	Check for malformed or unparsed duration values and report how they were handled.
•	Do not drop Route or other columns without explaining whether they are required for your analysis or future modelling.
Task 6 – Categorical Feature Encoding
•	Identify categorical columns that may be useful for analysis or a future prediction model.
•	Apply One-Hot Encoding to suitable nominal features, including Airline, Source, and Destination.
•	Display the generated encoded feature names and a sample of the encoded data.
•	Combine the encoded columns with the numerical/transformed features while preserving row alignment and the target Price.
•	Explain why encoding is required before many machine-learning algorithms can use categorical variables.
•	Ensure that the target variable Price is not one-hot encoded.
Task 7 – Final Dataset Validation
•	Display the final DataFrame's head, shape, column names, and data types.
•	Check for remaining missing values and unexpected object/string columns that should have been transformed.
•	Confirm that the number of rows has not changed unexpectedly during feature engineering or encoding.
•	Clearly identify the target column (Price) and the input features.
•	Save the cleaned and transformed dataset to a CSV file.
6. Expected Deliverables
•	One well-organized Jupyter Notebook (.ipynb) containing executable code, outputs, and explanations.
•	EDA visualizations with titles, axis labels, and readable formatting.
•	At least five written insights derived from the dataset.
•	A final cleaned and feature-engineered dataset saved as CSV.
•	A short conclusion summarizing the important findings, data-quality decisions, and transformations performed.
7. Submission Guidelines
•	This is an individual assignment. Each submission must represent the individual's own analysis and implementation.
•	Submit the completed Jupyter Notebook with all relevant cells executed and outputs visible.
•	Submit the exported final dataset (.csv) along with the notebook.
•	Use meaningful variable names and organize the notebook using Markdown headings.
•	Add brief explanations before or after important code sections, especially when making data-cleaning or imputation decisions.
•	Ensure that file paths are relative or clearly documented so the notebook can be run in another environment.
•	Do not submit only screenshots or copied outputs; the code and reasoning must be present.
8. Evaluation Rubric
Evaluation Area	What will be assessed
Data loading and understanding	Dataset loaded correctly; structure, columns, data types, and summaries inspected.
Data quality assessment	Missing values, duplicates, inconsistencies, and unusual values identified and handled with justification.
Exploratory data analysis	Relevant visualizations created and meaningful patterns interpreted.
Feature engineering	Date, time, stops, and duration features extracted and transformed accurately.
Categorical encoding and integration	Suitable categorical features encoded and combined without row misalignment or target leakage.
Final validation and communication	Final dataset validated and saved; notebook is readable, reproducible, and includes clear insights.
9. Important Notes
•	The attached notebook is a reference workflow for selected data-inspection and feature-engineering steps. It is not a complete end-to-end solution: some operations are left unfinished, and a full EDA, complete duration conversion, final feature integration, and prediction model are not demonstrated.
•	This assignment focuses on EDA and Feature Engineering. Building, training, and evaluating a machine-learning prediction model is not required unless separately instructed.
•	Make data-driven decisions. For example, replacing a missing Total_Stops value with the mode is an assumption, not a confirmed fact; state and justify any such choice.
•	Be careful with time and duration parsing. A flight may arrive on the next calendar day, and a duration value may contain only hours or only minutes.
