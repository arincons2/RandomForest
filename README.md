# Machine learning (supervised learning) via Random Forest 

Complete google collab script (Python code):
...

## **Problem statement**
The data are related to leads, that is, persons interested in the education product (process), 
 and this leads may or may not convert to paid customers.

## **Objective** 
 The goals of the project are:

-Analyze and build an ML model to help identify which leads are more likely to convert to paid customers.

-Find the factors driving the lead conversion process.

-Create a profile of the leads which are likely to convert.

## **Techniques utilized**

✅Main tasks:
-Data description: definition of columns (variables)
-Importing libraries and data
-Data overview (observations and sanity cheks)
-Univariate analysis of numerical columns (boxplots and histograms)
-Univariate analysis of categorical columns (countplots)
-Bivariate and multivariate analysis for lead status and current_occupation, first_interaction, profile_completed and last_activity. 
-bivariate and multivariate analysis for lead status and channels (print media, digital media, educational channels, referrals) 
-Bivariate and multivariate analysis for numerical variables.

-Data preprocessing (for the Random forest modelling)
-Examination of data (including basic statistics, checking for mull values, dummy variables, separation of target variable, definition of model evaluation criterion, etc)
-building of decision tree model (includes evaluation of model performance on training and testing dataset, pruning of the tree, development of the feature importance diagram)
-building of the Random forest model (includes evaluatin of model performance 
 on training and testing dataset, tuning of the Random Forest classifier, evaluation of tuned model performance on training and testing dataset, development of the feature importance diagram, formulation of observarions).
-Formulation of the overall conclusions and reccomendations

✅

## **Tools utilized**
✅Language: Python (Google collab)

✅ Python libraries: Numpy, Pandas, Matplotlib, Seaborn

## **Overall conclusions** 
From the count plots it follows that:

☑️

## **Recommendations** 
☑️

# Complete script (google colab script, including detailed code, insights and recommendations): 

https:

https://github.com/arincons2



## Data Description
The data contains the different attributes of leads and their interaction details with ExtraaLearn. Meaning of data: 

ID: ID of the lead

age: Age of the lead

current_occupation: Current occupation of the lead. Values include 'Professional','Unemployed',and 'Student'

first_interaction: How did the lead first interacted with ExtraaLearn. Values include 'Website', 'Mobile App'

profile_completed: What percentage of profile has been filled by the lead on the website/mobile app. Values include Low - (0-50%), Medium - (50-75%), High (75-100%)

website_visits: How many times has a lead visited the website

time_spent_on_website: Total time spent on the website

page_views_per_visit: Average number of pages on the website viewed during the visits.

last_activity: Last interaction between the lead and ExtraaLearn.

Email Activity: Seeking for details about program through email, Representative shared information with lead like brochure of program , etc
Phone Activity: Had a Phone Conversation with representative, Had conversation over SMS with representative, etc

Website Activity: Interacted on live chat with representative, Updated profile on website, etc
print_media_type1: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Newspaper.

print_media_type2: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Magazine.

digital_media: Flag indicating whether the lead had seen the ad of ExtraaLearn on the digital platforms.

educational_channels: Flag indicating whether the lead had heard about ExtraaLearn in the education channels like online forums, discussion threads, educational websites, etc.

referral: Flag indicating whether the lead had heard about ExtraaLearn through reference.

status: Flag indicating whether the lead was converted to a paid customer or not.
