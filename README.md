# Communicate-Data-Findings
Udacity's Data Analyst Nanodegree - Project

### Introduction
Bay Wheels is a regional public bicycle sharing system in the San Francisco Bay Area, California operated by Motivate in a partnership with the Metropolitan Transportation Commission and the Bay Area Air Quality Management District. Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States. It was established as Bay Area Bike Share in August 2013. As of January 2018, the Bay Wheels system had over 2,600 bicycles in 262 stations across San Francisco, East Bay and San Jose. On June 28, 2017, the system officially re-launched as Ford GoBike in a partnership with Ford Motor Company. After Motivate's acquisition by Lyft, the system was subsequently renamed to Bay Wheels in June 2019. The system is expected to expand to 7,000 bicycles around 540 stations in San Francisco, Oakland, Berkeley, Emeryville, and San Jose.


### The "Why"
Data visualization is an important skill that is used in many parts of the data analysis process. 
> *Exploratory* Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations. 

> *Explanatory* Its a techniques used by generating findings from the Data via EDA and data visualization, and are used to help communicate your results to others. 

![Ford GoBike Picture](https://images.ctfassets.net/q8mvene1wzq4/4nRp3KxeJFxEhiYUjsKHZm/65c7e155fc0b6494d6bd4205af1f987b/Watson_bike.jpg)


### Project Details

#### Data Gathering
> Ford GoBike is a publicly available dataset that will enable different folks with different skillsets to play around with. Data is downloaded from https://www.fordgobike.com/system-data

> There are 12 CSVs provided and the same is downloaded

> For the current analysis, 2018 data is downloaded 

Brief description about the data Each trip is anonymized and includes:
- Trip Duration (seconds)
- Start Time and Date
- End Time and Date
- Start Station ID
- Start Station Name
- Start Station Latitude
- Start Station Longitude
- End Station ID
- End Station Name
- End Station Latitude
- End Station Longitude
- Bike ID
- User Type (Subscriber or Customer — “Subscriber” = Member or “Customer” = Casual)


### Data Wrangling:
- All datasets are downloaded programatically and appended
- Upon a detailed review of the data, I was able to identify the below quality issues
- Update start_time and end_time to date-time format
- Convert the start_station_id and end_station_id int int64

### Data Preparation
Based on the business questions listed above, and identified quality gaps below are some updates needed

- Defining the day of the week
- Extracting time information form the start and end time columns
- Defining the distance using Orgin and Destination using Latitude & Longitude information as Kilometer and Miles
- New Hours Column driven from duration_sec column
- Defining new column as start_date & end_date Column which was driven from start_time & end_time
- Creating a time of the day variable

### Summary of Findings
- Subscribers use the bike sharing system on working days (Mon-Fri) and especially during rush hours.
- When compare to Subscribers Customers tend to use less service and ride for fun in the afternoon or early evenings over weekends.
- The number of trips spikes around 8-9am and 05-06pm during a working day 
- There were more trips on work days (Mon-Fri) compared to weekends.
- The riding trips tend to be shorter on Monday through Friday compared to weekends.

### Key Findings

- Tuesdays and Wednesdays record highest peak of using Ford bike sharing .
- The usage drops on Saturdays and Sundays
- October is the most popular month, followed by July/June/August
- Most usage of bike is during the morning hours of 8-9am, and in the afternoon hours of 5-6pm .
- Usage of bike system is higher in July for Customers.
- Usage of bike system is higher in October for Subscribers.
- The average distance traveled by customers is slightly higher than subscribers. The commuting distance for the subscribers is less  than the average ride a customer takes.
- Customer has little spike on sat & sun where as Subscribe dip on sat & sun


### Files
- readme.md - This Markdown file contains sections that you should fill out as you select your dataset, complete your exploration, and plan your explanatory analysis. 

- exploration_template.ipynb - This Jupyter Notebook contains section templates to help you organize your exploration, starting from loading in the data, working through univariate visualizations, and ending with bivariate and multivariate exploration. 

- slide_deck_template.ipynb - This Jupyter Notebook contains starter cells to help you organize your slide deck deliverable. These cells provide an example of how the slide deck should be organized, including pre-set slideshow settings.

To view the slide deck, you will need to use the expression (all one line):
jupyter nbconvert Example_Project_Diamonds_Part2.ipynb --to slides --post serve --template output_toggle

- output_toggle.tpl - This template file can be used with nbconvert to export your slide deck. This adds extra functionality to the slide deck by hiding the code to start, only making it visible if the reader clicks on the output (which should mostly be visualizations in the case of this project). 
