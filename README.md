

This project predicts the tip amount given to a waiter based on several restaurant-related features.



\# Dataset features



\* total\_bill: the total bill

\* tip: tip given to waiter in dollars

\* sex: gender of the person paying the bill

\* smoker: whether person smoked or not

\* day: day of the week

\* time: lunch or dinner

\* size: number of people



\# Model



Linear Regression was used because there is a linear relationship between \*\*total\_bill\*\* and \*\*tip\*\*. The model predicts the tip amount using the provided instances.

The dataset was split into \*\*80% training\*\* and \*\*20% testing\*\* data.



\# Libraries and Functions



1\. \*\*NumPy\*\*

&nbsp;  Used for numerical operations and working with arrays.



2\. \*\*Pandas\*\*

&nbsp;  Used for:



\* Loading dataset (`pd.read\_csv`)

\* Data manipulation

\* Encoding categorical variables (`pd.get\_dummies`)

\* Creating new data for prediction (`pd.DataFrame`)



3\. \*\*Plotly Express\*\*

&nbsp;  Used for data visualization:



\* `px.scatter()` → visualize the relationship between \*\*total\_bill\*\* and \*\*tip\*\*

\* `px.pie()` → show distribution of categorical variables



4\. \*\*Scikit-Learn\*\*

&nbsp;  Used for machine learning:



\* `train\_test\_split()` → split dataset into training and testing sets

\* `LinearRegression()` → regression model

\* `model.fit()` → train the model

\* `model.score()` → calculate R² score

\* `model.predict()` → predict tip amount



\# Model Evaluation



The model achieved an \*\*R² score of 0.6160\*\*, meaning it explains approximately \*\*61.6% of the variance\*\* in tip amounts.



R² = \*\*0.6160453998996112\*\*



The model’s \*\*mean absolute error (MAE)\*\* is \*\*0.5474\*\*, which means that on average the predicted tip differs from the actual tip by about \*\*$0.55\*\*.



MAE = \*\*0.5474409041050161\*\*



\# Prediction Example

new\_data = pd.DataFrame({

&nbsp;   "total\_bill": \[25.0],

&nbsp;   "size": \[2],

&nbsp;   "sex\_Male": \[0],

&nbsp;   "smoker\_Yes": \[0],

&nbsp;   "day\_Sat": \[1],

&nbsp;   "day\_Sun": \[0],

&nbsp;   "day\_Thur": \[0],

&nbsp;   "time\_Dinner": \[1]

})



Predicted Tip:3.4591255575825657



