 Udacity : Data analyst Nanodegree
Project 4 - Wrangle_and_Analyze-WeRatesDogs

Introduction

Using Python and its libraries, you will gather data from a variety of sources and in a variety
of formats, assess its quality and tidiness, then clean it. This is called data wrangling.
The dataset I will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter
user @dog_rates, also known as WeRateDogs

Project details

The tasks of this project are as follows:
   Data wrangling, which consists of:
     Gathering data
     Assessing data
   Cleaning data
   Visualization
   Reporting on
     our data wrangling efforts (Report 1- Wrangle report)
     our data analyses and visualizations (Report 2- act-report)
    
Gathering data

The data for this project consist on three different dataset that were obtained as following:
  1. The twitter_archive_enhanced.csv was provided by Udacity and downloaded
  manually.
  2. This file (image_predictions.tsv) is hosted on Udacity's servers and was downloaded
  programmatically using the Requests library and URL information
  3. By using twitter developer account got an access to download @dog_rates Twitter
  archive.  
  Then I query the Twitter API for each tweet's JSON data using Python tweepy library
  and stored each tweet's entire set of JSON data in a file called tweet_json.txt file.
  
Assessing data

After the data was gathered, Dataframes consists:
  Twitter archive file as twitter_df
  Shape: (2356, 17)
  
  The tweet image predictions as image_pred
  Shape: (2075, 12)
  
  Twitter API & JSON as tweet_api
  Shape: (2331, 4)
  
After visual and programmatic assessments of datasets I have come up with
following quality and tidiness issues:

   Merge all Data set (twitter_df , image_pred , tweet_api) by Tweet_id
   Convert timestamp to datetime
   Convert text to Str type
   Dog Breed Prediction (Prediction_1)
   Extract url from text column
   Extract Dog types from doggo, floofer, pupper, puppo columns
   Incorrect names have lowercase letter (replace with NaN).
   Calculating Ratings of the Dog
   Drop Unwanted columns and save data set into "twitter_archive_master.csv"
.
Conclusion

  Finally cleaning above quality and tidiness issues, twitter_archive_master.csv is the
  combined and cleaned data which consists (2059, 11) Rows and Columns.
  
Sources:
https://stackoverflow.com/questions/28384588/twitter-api-get-tweets-with-specific-id
https://www.tutorialspoint.com/python_text_processing/python_extract_url_from_text.htm
https://jakevdp.github.io/PythonDataScienceHandbook/03.07-merge-and-join.html
https://knowledge.udacity.com/questions/45245
