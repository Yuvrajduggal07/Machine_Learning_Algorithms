The Spaceship Titanic case study involves analyzing passenger data from the famous interstellar cruise liner, Spaceship Titanic. The goal is to build a Logistic Regression model that can accurately identify passengers who are likely to have been transported to their destination based on various features and amenities provided during the voyage. This analysis is crucial for understanding the factors that contribute to successful transportation and enhancing the overall passenger experience on future interstellar journeys.

Dataset Description:

PassengerId - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is traveling with and pp is their number within the group. People in a group are often family members, but not always.
HomePlanet - The planet the passenger departed from, typically their planet of permanent residence.
CryoSleep - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
Cabin - The cabin number where the passenger is staying. Takes the form deck/num/side, where the side can be either P for Port or S for Starboard.
Destination - The planet the passenger will be debarking to.
Age - The age of the passenger.
VIP - Whether the passenger has paid for special VIP service during the voyage.
RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
Name - The first and last names of the passenger.
Transported - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.
Below are the data files:

spaceship_titanic_test.csv - Test File spaceship_titanic_train.csv - Train File Final_Report_Spaceship_Titanic - Output file

Conclusion: Below are the valuable insights that I gained from Spaceship Titanic Dataset.

The Spaceship Titanic training dataset contains 8693x15 records and the test dataset contains 4277x14 records.

Data Quality: Ensured dataset's integrity by checking for duplicates, and no duplicate records were found.

Feature Engineering:I split the "Cabin" feature into "Deck Num" and "Deck Side" features, which allowed me to extract additional information relevant to passenger transportation.

Preprocessing: I handled missing values using appropriate imputation techniques, such as median for numerical columns and mode for categorical columns, ensuring data completeness. Label Encoding and Onehot Encoder techniques were used to handle encoding. Outlier treatment was not done as outliers do not impact the logistic regression model. Data is balanced so no imbalance treatment is done.

Distribution Analysis: Analyzed the distribution of numerical and categorical columns, which provided valuable insights into the dataset's characteristics.

Significant Variables: An Anova Test was performed to identify significant categorical variables, all of which were found to be impactful in predicting passenger transportation.

Model Performance: My logistic regression model achieved promising results, with a training accuracy of 72.4% and a test accuracy of 73.0%. The precision, recall, and F1-score metrics were well-balanced, indicating consistent performance.

Cross-Validation: To validate the model's generalization performance, I performed k-fold cross-validation. The model demonstrated stability with a mean accuracy of 0.72 in training data and 0.73 in testing data.

ROC AUC Score: My model achieved a ROC AUC score of 0.72, which indicates its ability to distinguish between positive and negative instances reasonably well.

The next steps include applying other algorithms to explore potential improvements in model performance.
