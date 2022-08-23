# Exploratory Data Analysis on Airbnb NYC 2019 Data

### Problem Statement:
Since 2008, guests and hosts have used Airbnb to expand on traveling possibilities and present a more unique, personalized way of experiencing the world. Today,
Airbnb became one of a kind service that is used and recognized by the whole world. Data analysis on millions of listings provided through Airbnb is a crucial
factor for the company. These millions of listings generate a lot of data, data that can be analyzed and used for security, business decisions, understanding of
customers’ and hosts’ behavior and performance on the platform, guiding marketing initiatives, implementation of innovative additional services and much
more.

The dataset has around 49000 observations and 16 columns in it which is a mix of categorical and numerical variables. The main objective here is to explore and
analyze the data to find out insights such as:

● What can we learn about different hosts and areas?

● What can we learn from predictions?

● Which hosts are the busiest and why?

● Is there any noticeable difference of traffic among different areas and what
could be the reason for it?

EDA will help us generate such insights not limited to these which will help the company, hosts and travelers to make better decisions in future.

---
### The different features the dataset contains:

● id: It is an unique id given to the property listed in airbnb NYC which is a numerical variable.

● name: It represents the name of the airbnb listed property which is a categorical variable.

● host_id: This is an unique id given to the host of the property which is a numerical variable.

● host_name: The name of the host of the property listed which is a categorical variable.

● neighbourhood_group: This represents a big neighborhood inside which there are many mini neighborhoods which is a categorical variable. There
are 5 neighborhood groups in the data:

    ○ Manhattan
    
    ○ Brooklyn
    
    ○ Staten Island
    
    ○ Queens
    
    ○ Bronx

● neighbourhood: This represents all the mini neighborhoods present in NYC which is another categorical variable.

● latitude: latitude coordinates

● longitude: longitude coordinates

● room_type: This represents the type of room in the listed property which is a categorical variable. There are three room types available in the dataset:

    ○ Entire Home/Apt
    
    ○ Private Rooms
    
    ○ Shared Rooms

● price: Represents the price per day of stay in the respective listed property which is a numerical variable.

● minimum_nights: This represents the minimum number of nights a person has to pay for or stay in the property which is a numerical variable.

● number_of_reviews: The number of reviews given to the property and the host which is a numerical variable.

● last_review: The date of the last review given which is a datetime object.

● reviews_per_month: The number of reviews given over a month to a property or the host which is a numerical variable.

● calculated_host_listings_count: How many listings a particular host has in NYC which is another numerical variable.

● availability_365: Availability of the property out of 365 days which is also a numerical variable.

---
### Approach:

To accomplish the above task, it was divided into two parts as follows:

● Data Cleaning:

When it comes to data, there are many different sorts of quality issues, which is why data cleaning is one of the most time consuming aspects of
data analysis. Formatting issues, missing values, duplicated rows, spelling discrepancies, and so on could all be present. These difficulties make data
analysis difficult, resulting in inaccuracies or inappropriate results. The first step was to look for duplicate values in the dataset. Thankfully,
there were no duplicate values present. The second step was to look for missing values and there were 4 columns which had a good number of missing values present. 
Missing values are usually represented in the form of NaN or NULL or NONE in the dataset.

Missing values can be dealt with any of the following techniques:

1. Deleting the columns with missing data
2. Deleting the rows with missing data
3. Imputing the missing data with an appropriate value
4. Imputing the missing data with an additional column

There were few columns with missing values which were irrelevant for our analysis so I decided to drop those columns and imputed a few columns with an appropriate 
value.

● EDA:

EDA is used to take insights from the data and the outcomes help businesses to know their customers, expand their business and make decisions accordingly.
The third step was to explore and perform some univariate, bivariate and multivariate analysis to discover insights from the data. This step helped me
figure out that the ‘price’ column was heavily skewed and there were few observations with ‘price’ listed as 0 which cannot be true. Assuming that no
one is giving Airbnb stays for free, the data containing ‘price’ as 0 was excluded from the analysis.
The process of EDA helped uncover a lot of insights about different things which were not known by looking at the data.

---
### Results:

#### **Insights about the different hosts:**

● There are 37455 unique hosts in NYC.

● Sonder (NYC) has the most multiple property listings in NYC. Despite having the most number of properties she isn’t the busiest host in NYC.

● Maya who receives the most number of reviews is the one who is the busiest of all in NYC. She has 5 properties listed in the same neighborhood and
there are multiple reasons acting in favor of receiving the most number of customers.

    ○ The price at which she offers her properties is less than the average price of all neighborhood groups.

    ○ The condition for minimum nights is one, which is way less than many others.

    ○ There is enough availability of her properties out of 365 days.
  
    ○ High number of reviews will definitely help customers make a booking.

● There are many hosts who don’t receive a huge number of customers but still stay occupied for the whole year. This could be due to the reason that
the customers they are getting are staying for a longer period of time keeping their properties occupied.

#### **Insights about the different areas:**

● Manhattan has the most number of properties listed followed by Brooklyn. These two neighborhoods are the most expensive and receive the most
number of customers or traffic as compared to others.

● Staten Island being mostly a residential area has the least number of properties listed and receives the least number of customers. Interestingly,
the average prices of Private Rooms in Staten Island are the least expensive and stay available for a good number of days which makes a good choice for
customers seeking low cost accommodations.

● Manhattan contains the most number of Entire Home/Apt and in general they are costlier than any other room type across all neighborhoods.

● Bronx is the least expensive neighborhood and less preferred by customers.

#### **Insights about the different room types:**

● There are 25407 Entire Home/Apt and 22319 Private Rooms which is way higher than the number of Shared Rooms available.

● Entire Home/Apt is the most expensive room type and the most preferred by customers.

● Entire Home/Apt and Private Rooms receive way more customers than Shared Rooms across all neighborhoods.

● Shared Rooms are the least preferred room type and remain the most available out of 365 days.

***
