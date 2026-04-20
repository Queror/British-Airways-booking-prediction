# British-Airways-booking-prediction
Python scikit-learn Forage Status

Predictive modelling project completed as part of the British Airways Data Science Job Simulation on Forage.

* Project Overview
British Airways operates in a highly competitive market where understanding customer behaviour is critical. In this project, I built a machine learning model to predict whether a customer will complete a flight booking, based on their search and purchase behaviour.


* Dataset Properties
Records	50,000 customer booking entries
Features	14 original + engineered features
Target	booking_complete (1 = completed, 0 = not completed)
Source	British Airways via Forage

Key columns:

purchase_lead — days between booking and flight
length_of_stay — duration of trip
flight_duration — length of flight in hours
booking_origin — country where booking was made
route — flight route code
wants_extra_baggage, wants_preferred_seat, wants_in_flight_meals — add-on preferences
sales_channel — Internet or Mobile

* Project Workflow

1.  Exploratory Data Analysis
2. Feature Engineering
3.  Model Training
4.  Evaluation
5-Fold Stratified Cross-Validation (StratifiedKFold ensures each fold preserves class balance)

* Results
Metric	Score
ROC-AUC (5-fold CV)	0.768 ± 0.004
F1 Score (5-fold CV)	0.415 ± 0.004
Precision (Booked class)	0.30
Recall (Booked class)	0.74
Test Accuracy	0.70
ROC-AUC of 0.768 means the model correctly ranks a booker above a non-booker 77% of the time — well above random guessing (0.5).

* Key Findings
booking_origin is the dominant predictor (with a 42% feature importance): where a customer books from is the single strongest signal
route and length_of_stay are the next most influential features
trip_type and is_group_booking contribute very little predictive value
High recall (74%) on the booked class means the model catches most actual bookings — useful for targeted marketing campaigns
The StratifiedKFold fix was critical — regular KFold gave misleading ROC-AUC of 0.388 due to class imbalance in folds


* Certificate
This project was completed as part of the British Airways Data Science Job Simulation on Forage (March 2026).

👤 Author
Umar Ibrahim LinkedIn | GitHub
