#Exploratory Data Analysis on NYC Taxi Trip Dataset
This project focuses on performing Exploratory Data Analysis (EDA) on the NYC Taxi Trip Dataset. The dataset is provided by a taxi service provider operating in New York City, with the goal of estimating the approximate time it would take for a trip to be completed. The insights gained from this analysis can help the service provider deploy their fleet of cabs more efficiently.

Dataset Description
The dataset consists of the following variables:

id: A unique identifier for each trip.
vendor_id: A code indicating the provider associated with the trip record.
pickup_datetime: Date and time when the meter was engaged.
dropoff_datetime: Date and time when the meter was disengaged.
passenger_count: The number of passengers in the vehicle (driver-entered value).
pickup_longitude: The longitude where the meter was engaged.
pickup_latitude: The latitude where the meter was engaged.
dropoff_longitude: The longitude where the meter was disengaged.
dropoff_latitude: The latitude where the meter was disengaged.
store_and_fwd_flag: Flag indicating whether the trip record was held in vehicle memory before sending to the vendor (Y=store and forward; N=not a store and forward trip).
trip_duration: Duration of the trip in seconds (target variable).
Steps Performed
Read the Dataset: The dataset containing 729,032 rows and 11 columns was read into the analysis.
Checked the Shape of the Dataset: The shape of the dataset was found to be 729,032 rows and 11 columns, indicating no missing values.
Statistics of the Variables: The descriptive statistics of the variables in the dataset were examined.
Missing Values Verification: It was confirmed that there were no missing values in the dataset.
Checking Variable Types: The variable types were reviewed, and necessary changes were made, such as converting pickup_datetime and dropoff_datetime to datetime format and store_and_fwd_flag to categorical type.
Calculating Trip Distance: The distance of each trip was calculated using the pickup and dropoff coordinates.
Segregating Trips by Duration: The trips were categorized based on their duration.
Univariate Analysis: Several univariate analyses were conducted to gain insights into different aspects of the dataset.
Pickup and Dropoff Week: Friday was observed to be the busiest day of the week.
Months of the Year: March followed by April were the busiest months.
Trip Recording: Only 1% of the trips were recorded in the server.
Passenger Count Distribution: Most trips had 1 or 2 passengers, with a few outliers having 7 or 9 passengers.
Trip Time of the Day: Most trips occurred in the evening and morning.
Trip Durations: The majority of trip durations were short, with some outliers.
Average Speed of Taxi Drivers: The average speeds were found to be low, indicating heavy traffic in NYC.
Bivariate Analysis: Relationships between different variables were explored to identify patterns and correlations.
Passengers and Vendor ID: Vendor 2 was preferred by most passengers.
Trip Duration and Vendor ID: Vendor 1 offered mostly short trips, while Vendor 2 offered both short and long trips.
Store and Forward Flag and Trip Duration: Longer trips were not recorded, while shorter trips were recorded.
Finding the Correlation between different variables of the Dataset: The correlation between variables was analyzed to identify relationships and dependencies. It was observed that Pickup Day and Dropoff Day had the highest correlation among all the variables.

Plotting Heatmap for Numerical Variables: A heatmap was created to visualize the correlation between numerical variables. Key observations include:

Similar correlation patterns were observed in Kendall and Spearman correlation.
Most variables showed insignificant correlations.
The major correlation was found between Dropoff Hour and Pickup Hour.
Observing Passenger Count and Trip Duration: The relationship between passenger count and trip duration was explored. Key observations include:

The majority of trip durations fell within the range of 800 to 1000 seconds.
Trip durations close to 0 seconds could be outliers or indicative of canceled trips.
Observing Time-based Patterns in Trip Duration:

The graph of pickup_hour vs. trip_duration showed a peak at 15 hours, indicating that the time period between 2:00 PM and 4:00 PM had the longest trips.
The graph of pickup_timeofday vs. trip_duration also peaked in the afternoon, suggesting that the longest trips generally occurred during that time.
Performing T-test and Z-test on Data: T-tests and Z-tests were conducted to compare the average speed between Vendor 1 and Vendor 2. Key observations include:

The average speeds for both Vendor 1 and Vendor 2 were found to be similar.
Observations on Vendor Trips:

Vendor 2 offered longer trips compared to Vendor 1.
The dataset contained numerous outliers.
Multivariate Analysis:

Calculating the Correlation: The correlation between variables was calculated. Key observations include:
The strongest correlation was found between Pickup Day and Dropoff Day.
There was a medium correlation between average speed and distance.
Observing Pickup Hour, Trip Duration, Store and FWD Flag: The relationship between pickup hour, trip duration, and the store and forward flag was examined. Key observations include:
During long trips, the store and forward flag was recorded more frequently compared to shorter trips.
Observing Pickup Hour, Average Speed, and Pickup Time of Day: The relationship between pickup hour, average speed, and pickup time of day was explored. Key observations include:
During midnight hours (12 AM - 5 AM), average speeds ranged from 18 km/h to 24 km/h, indicating low traffic.
Average speeds reduced to 12-20 km/h during morning and afternoon hours, indicating increased city traffic.
These steps provide a comprehensive overview of the exploratory data analysis performed on the NYC Taxi Trip Dataset, highlighting key findings and insights obtained from the analysis.
