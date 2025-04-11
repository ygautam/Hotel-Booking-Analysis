# Hotel Booking Analysis

This dataset provides comprehensive insights into the population, geographical distribution, and growth dynamics of different countries worldwide. It includes key metrics such as land and water area, birth and death rates, migration trends, and population growth rates. This data is valuable for analyzing global demographic patterns, understanding population distribution, and forecasting future growth trends.

## Dataset Overview
- Rows: 119391
- Columns: 32
- Column Description
- hotel: Type of hotel.
- is_canceled: Target variable, indicating whether the booking was canceled (1) or not (0).
- lead_time: Number of days between the booking date and the arrival date.
- arrival_date_year: Year of arrival.
- arrival_date_month: Month of arrival.
- arrival_date_week_number: Week number of the arrival date.
- arrival_date_day_of_month: Day of the month of arrival.
- stays_in_weekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed.
- stays_in_week_nights: Number of weeknights (Monday to Friday) the guest stayed.
- adults: Number of adults included in the booking.
- children: Number of children included in the booking.
- babies: Number of babies included in the booking.
- meal: Type of meal booked.
- country: Country of origin of the guest.
- market_segment: Market segment designation.
- distribution_channel: Booking distribution channel.
- is_repeated_guest: Whether the guest is a repeated guest (1) or not (0).
- previous_cancellations: Number of previous cancellations by the guest.
- previous_bookings_not_canceled: Number of previous bookings not canceled.
- reserved_room_type: Code for the room type reserved.
- assigned_room_type: Code for the room type assigned.
- booking_changes: Number of changes made to the booking.
- deposit_type: Type of deposit made for the booking.
- agent: ID of the travel agency that made the booking.
- company: ID of the company that made the booking.
- days_in_waiting_list: Number of days the booking was on the waiting list.
- customer_type: Type of customer.
- adr: Average daily rate for the stay.
- required_car_parking_spaces: Number of car parking spaces required.
- total_of_special_requests: Number of special requests made.
- reservation_status: Final status of the reservation.
- reservation_status_date: Date of the last status change.

## Questions
### Data Cleaning And Preprocessing
- Missing Data Handling: Identify and handle missing values in columns like children, country, and agent. Decide whether to impute missing values or remove rows with missing data.
- Outlier Detection: Check for anomalies in columns like adr (extreme values) and lead_time (very high values may need handling).
Data Type Conversion: Ensure all data columns have the correct data types.


### Feature Engineering
- Feature Scaling: Apply scaling techniques to numerical features.
- Categorical Grouping: Group bookings into three categories based on lead_time:
    Short: lead_time < 30 days
    Medium: 30 days < lead_time < 90 days
    Large: 90 days > lead_time

### Complex Calculations And Advanced Functions
- Running Total Analysis: Create a running total chart to show cumulative booking cancellations over time.
- Weighted Booking Score: Compute a weighted cancellation rate by considering both previous_cancellations and previous_bookings_not_canceled.
- Dynamic Rank Calculation: Use ranking techniques to dynamically rank hotels based on their cancellation rate.

### Advanced Filtering And Parameterized Visualizations
- Dynamic Market Segment Analysis: Create a query that allows users to filter bookings by market segment dynamically.
- Find High-Risk Customers: Retrieve a list of customers who had multiple cancellations in the past.
- Most Frequent Guests: Identify the most frequent guests based on repeated bookings.
- Seasonal Booking Trends: Identify peak booking months and trends across different hotels.

### Joins And Multi-Table Queries
- Hotel-Specific Cancellation Rate: Find the total number of cancellations per hotel type.
- Countries With High Cancellation Rates: List all countries from which guests have a high tendency to cancel bookings.

### Model Building
- Split the Dataset: Split the dataset into training and testing sets (e.g., 80% training, 20% testing).
Experiment with models, mainly logistic regression, decision tree, random forest, gradient boosting machines, support vector machines.
- Hyperparameter Tuning: Use Grid Search or Random Search to optimize hyperparameters.

### Model Testing
- Evaluate performance using accuracy, precision, recall, F1-score and AUC-ROC. Use cross-validation techniques. Compare model performance and determine the best one based on evaluation metrics.
