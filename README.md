# British Airways Sentiment Analysis and Flight Booking Prediction

## Overview

This repository presents a comprehensive analysis of customer sentiments towards British Airways, utilizing reviews sourced from SkyyTrax.com. The project is divided into two main parts:

## 1. Sentiment Analysis
Explore the sentiments expressed by customers in their reviews of British Airways on SkyyTrax.com. The sentiment analysis provides insights into the overall customer satisfaction, identifying positive and negative sentiments, and highlighting key areas for improvement.

WebScrapping
Data wrangling
Feature Selection
WordClouds
TfidfVectorizer, SentimentIntensityAnalyzer



### BUSINESS OBJECTIVE

Find the sentimets of customers from Reviews on skyytraxx and Provide feedback from sentiments.


### WEBSCRAPPING
Scrapping 37 pages with 100 reviews per page from Skyttrax.com
3700 Reviews were collected in Total

![Screenshot 2024-02-06 at 7 28 36 PM](https://github.com/GordonMensah/British-airways/assets/148505242/fb1fae97-d76f-4877-99b2-64538f1ec80f)


### DATA WRANGLING
Cleaning text data to reserve only reviews for analysis
Placing reviews into columns to keep uniqueness in reviews 
Use of TfidfVectorizer and SentimentIntensityAnalyzer to find the Polarity scores for each review and their compound score to determine which catagory they belong
use of wordclouds to Forecest expressed sentiments

![Screenshot 2024-02-06 at 7 28 46 PM](https://github.com/GordonMensah/British-airways/assets/148505242/2cf531b1-25b2-481f-a4eb-0fdab316ba88)
![Screenshot 2024-02-06 at 6 50 29 PM](https://github.com/GordonMensah/British-airways/assets/148505242/44510d0a-c5a8-481a-acb2-af94dd3e43e6)
![Screenshot 2024-02-06 at 6 50 10 PM](https://github.com/GordonMensah/British-airways/assets/148505242/7249cf00-e90a-4ec6-b69b-2a33ec1091d0)
![Screenshot 2024-02-06 at 6 50 29 PM](https://github.com/GordonMensah/British-airways/assets/148505242/0817cf0c-661f-4232-a1a1-97765413963f)
![Screenshot 2024-02-06 at 6 50 23 PM](https://github.com/GordonMensah/British-airways/assets/148505242/3cf7f270-a08f-4e1d-bc5a-4f110dc2731b)

![Screenshot 2024-02-06 at 6 50 02 PM](https://github.com/GordonMensah/British-airways/assets/148505242/f360595d-4ed0-4811-9123-8c2cadf00981)


### MODEL BUILDING
Built a model with TfidfVectorizer and SentimentIntensityAnalyzer
Built a Pipeline to easily analyse future data with informatuion from this set
![Screenshot 2024-02-06 at 6 50 10 PM](https://github.com/GordonMensah/British-airways/assets/148505242/d72a7ce6-d9aa-4ce3-8607-0fa6fc7d0a8d)



### INSIGHTS
Positive Sentiments were more compared to the negative
Overall people had good things to say about British Airways
Customers werent happy about the Airline in general, Flight connections, Cancelled flughts, The Overall Customer Service, Majority of these analysis were from Business Class Passengers
Csutomers were please with the flight times, The Airline In General, Flight attendant Services, , Choicago flights  were spoken well; about  
![Screenshot 2024-02-06 at 6 50 54 PM](https://github.com/GordonMensah/British-airways/assets/148505242/95c5cee4-2d6c-4ece-a4cd-82b1137935b1)
![Screenshot 2024-02-06 at 6 50 41 PM](https://github.com/GordonMensah/British-airways/assets/148505242/27811002-5427-461f-99d6-80d24bedf635)



## 2. Flight Booking Prediction
Main Objective was to Predict the probability of a customer booking a flight based on various features. This predictive model aims to assist in understanding the factors influencing customers' decisions to book a flight with British Airways. The analysis can be valuable for marketing strategies, customer engagement, and enhancing the overall booking experience.

Performed data cleaning
Data Preparartion and Transformation 
Feature Selection
RandomUnderSampler
Hyperparameter Tuning
Machine Learning Modeling Using RandomForest, GridCV



### BUSINESS OBJECTIVE

Find the Probability Of A customer to book a flight
Factors that are associated with booked flights


### DATA PREPARATION
One Hot Encoding of features 'sales_channel','trip_type','flight_day'
Dummies were made for the number of passengers selected per booking
Corrected Skewness inPurchase lead, Length of stay, Flight hour, Flight Duration

Data Showed just 15% of customers making Bookings

![Screenshot 2024-02-06 at 7 32 33 AM](https://github.com/GordonMensah/British-airways/assets/148505242/08434ea4-b427-4607-ace0-3e8cb2004445)

![Screenshot 2024-02-06 at 5 42 38 AM](https://github.com/GordonMensah/British-airways/assets/148505242/f405ed2c-47d9-4d64-8255-83b5fe3f89c7)



![Screenshot 2024-02-06 at 7 33 24 AM](https://github.com/GordonMensah/British-airways/assets/148505242/f2cd3bf9-3316-4236-9328-4b793ce2af61)



### DATA MODELLING
Random Forest,LogisticRegression,GridSearchCV, was used for the classification and prediction of the model
Correlation was checked using a heat map 
Model was rechecked after dropping features
Feature Selection
Hyperparameter Tunning was finaly done to ensure increased Accuracy and Precision
Confusion Matrix to evaluate performance 

![Screenshot 2024-02-06 at 7 11 37 AM](https://github.com/GordonMensah/British-airways/assets/148505242/c574f0cf-b029-43ec-b74a-cdff4ad7967a)
![Screenshot 2024-02-06 at 7 11 09 AM](https://github.com/GordonMensah/British-airways/assets/148505242/b271b6e6-289c-471d-90ef-c91743b7b1a4)

![Screenshot 2024-02-06 at 7 12 49 AM](https://github.com/GordonMensah/British-airways/assets/148505242/8971a3c8-4808-4393-99aa-143c6740fa53)




### INSIGHTS
Purchase_lead,Flight_hour, Length, Flight_duration determined an increase in the possibility of a customer booking a flight
The price wasnt a concern but quality of services given by the company
Customers making bookings on their mobiles were more likely to book a flight
Customer who planned to stay for shorter periods usually ended up booking their flights
If the customer selected an in flight meal or seat preference, they booked the flight
Suggestions were made to look into to flights that had more purchases in order to adjust flight hour for non performing flights
Follow up emails for customers who are predicted to end up making bookings since just 15% of searchers ended up making bookings, there is more potential for incrase in flight purchases






## Repository Structure

data/: Contains the raw and processed data used in the analysis.
notebooks/: Jupyter notebooks detailing the step-by-step analysis.
models/: Saved models or model artifacts for the flight booking prediction.
Dependencies

## Python 3.x
Jupyter Notebooks
Required Python libraries (requests, BeautifulSoup, re, pandas, seaborn, numpy as np, string, matplotlib.pyplot as plt, wordcloud, STOPWORDS, ImageColorGenerator, sys, os, path, PIL)
Usage

## Clone the repository.
Follow the instructions in the provided notebooks to reproduce the analysis.
Explore and adapt the code to your specific use case.
Contributions

#### Contributions, bug reports, and feature requests are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License.

## Acknowledgments

Special thanks to SkyyTrax.com for providing the valuable dataset.
Inspired by the need to understand customer sentiments and predict booking behaviors.
Feel free to customize the description to better fit your project and provide any additional details that may be relevant.
