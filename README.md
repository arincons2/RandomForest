# Machine learning (supervised learning) via Random Forest 

Complete google collab script (Python code):

https://github.com/arincons2/RandomForest/blob/325ef5d2ddb61e4daa4c97cb76fb499323f08f4e/MEJORA3_RandForestProject.ipynb

## **Context and Problem statement**
The project aims to analyze and model the data of an online education company that uses digital marketing resources to reach its audience with their offerings.
The customers who show interest in these offerings are termed as leads. There are various sources of obtaining leads for Edtech companies, like:
- The customer interacts with the marketing front on social media or other online platforms.
- The customer browses the website/app and downloads the brochure
- The customer connects through emails for more information.
- The company then nurtures these leads and tries to convert them to paid customers.

For this, the representative from the organization connects with the lead on call or through email to share further details. The leads may or may not convert to paid customers.

## **Objective** 
 The goals of the project are: i) Analyze and build an ML model to help identify which leads are more likely to convert to paid customers; ii) Find the factors driving the lead conversion process, iii) Create a profile of the leads which are likely to convert.

## **Techniques utilized**

Main tasks:

✅ Importation of libraries and data.

✅ Exploration, cleaning and preparation of data (observations and sanity cheks).

✅ Univariate analysis of numerical columns (boxplots and histograms).

✅ Univariate analysis of categorical columns (countplots).

✅ Multivariate analysis for categorical variables: i) Bivariate and multivariate analysis for lead status and current_occupation, first_interaction, profile_completed and last_activity (which are not related to communication channels); ii) Bivariate and multivariate analysis for lead status and channels (print media, digital media, educational channels, referrals). 

✅ Bivariate and multivariate analysis for numerical variables.

✅ Data preprocessing (as preparation for the Random forest modeling).

✅ Examination of preprocessed data (including basic statistics, checking for mull values, dummy variables, separation of target variable, definition of model evaluation criterion, etc).

✅ Building of decision tree model (includes evaluation of model performance on training and testing dataset, pruning of the tree, development of the feature importance diagram).

✅ Building of the Random forest model (includes evaluation of model performance on training and testing dataset, tuning of the Random Forest classifier, evaluation of tuned model performance on training and testing dataset, development of the feature importance diagram, formulation of observarions).

✅ Formulation of the overall conclusions and recommendations.

## **Tools utilized**
✅Language: Python (Google collab)

✅ Python libraries: Numpy, Pandas, Matplotlib, Seaborn, statsmodels, sklearn.

## **Overall conclusions** 

From the Exploratory Data Analysis -EDA for categorical variables no related to communication channels (current occupation, first_interaction, profile_completed and last_activity), it follows that:

☑️ The highest percentage of converted leads is attained by the 'first_interaction' variable, with 'Website' value.

☑️ For the 'current occupation' variable, the values 'Professional' and 'Unemployed' exhibit a significantly higher percentage of converted leads than 'Student'.

From the EDA for categorical variables that imply communication channels (print media, digital media, educational channels, referrals), it follows that:

☑️ The highest percentage of converted leads is attained by the 'referral' variable, with 'Yes' value.

From the EDA for numerical variables (age, web site visits, time spent on website, and page views per visit), it follows that:

☑️ The four numerical variables exhibit a high effect on the status %.

☑️ The 'age' variable with values higher than 30 years exhibits higher positive status % compared to age lower than 30.

☑️ The 'Time spent on website' variable with values higher than 507 exhibits significantly higher positive status % compared to values lower than 507.

From the Random forest model it follows that:

☑️ **The 'time_spent_on_website', 'first_interaction_Website', 'profile_completed_Medium', 'age', 'current_occupation_Unemployed' are the five most important columns (variables), according to the feature importance diagram for the tuned Random forest**.

☑️ **In contrast, the 'referral_Yes', 'educational_channels_Yes', 'print_media_type1_Yes', 'print_media_type2_Yes' variables have a low importance**.

☑️ **The leads with higher likelyhood to become paid customers are characterized by: spend time on website longer than 507, their first interaction is through website, have a High level of profile completion; they are older than 30 years, and their current occupation is professional**.

☑️ **Also, referral is the channel with higher importance**.

Other conclusions:

- We have utilized the decision tree, pruned decision tree,
random forest and tuned random forest.
- The tuning of random forest resulted in avoidance if overfitting.
- The obtained values of precision and recall compared between train and test are very similar, with a precision of 0.83-0.84 and a recall of 0.73-0.78.
- We have identified the key factors involved in the conversion of leads to paid customers, by means of the 'feature importance' diagram.
- It is possible to improve the tuning by including other parameters in the optimization, and by modifying the parameter values used as possible values in the optimization.

## **Recommendations** 
☑️The variables 'time_spent_on_website' and 'first_interaction_Website' are the most important ones for identifying which leads are more likely to convert to paid customers. Then, to improve the conversion of unpaid to paind customers, the ExtraaLearn company should focus on: i) increasing the advertising that motivates people to interact through the website, rather than email or phone; ii) reviewing the website (the information that is given to the readers) and improving it if possible, as it results in higher conversion rate.

☑️The variables 'current_occupation_Unemployed' has a significantly higher importance than 'current_occupation_Student'. Therefore, the ExtraaLearn company should focus its advertising and communication campaigns on Unemployed people and Professional people rather than students.

# Complete script (google colab script, including detailed code, insights and recommendations): 

https://github.com/arincons2/RandomForest/blob/325ef5d2ddb61e4daa4c97cb76fb499323f08f4e/MEJORA3_RandForestProject.ipynb

https://github.com/arincons2



## Data Description
The data contains the different attributes of leads and their interaction details with ExtraaLearn. Meaning of data: 

- ID: ID of the lead

- age: Age of the lead

- current_occupation: Current occupation of the lead. Values include 'Professional','Unemployed',and 'Student'

- first_interaction: How did the lead first interacted with ExtraaLearn. Values include 'Website', 'Mobile App'

- profile_completed: What percentage of profile has been filled by the lead on the website/mobile app. Values include Low - (0-50%), Medium - (50-75%), High (75-100%)

- website_visits: How many times has a lead visited the website

- time_spent_on_website: Total time spent on the website

- page_views_per_visit: Average number of pages on the website viewed during the visits.

- last_activity: Last interaction between the lead and ExtraaLearn.

- Email Activity: Seeking for details about program through email, Representative shared information with lead like brochure of program , etc

- Phone Activity: Had a Phone Conversation with representative, Had conversation over SMS with representative, etc

- Website Activity: Interacted on live chat with representative, Updated profile on website, etc

- print_media_type1: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Newspaper.

- print_media_type2: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Magazine.

- digital_media: Flag indicating whether the lead had seen the ad of ExtraaLearn on the digital platforms.

- educational_channels: Flag indicating whether the lead had heard about ExtraaLearn in the education channels like online forums, discussion threads, educational websites, etc.

- referral: Flag indicating whether the lead had heard about ExtraaLearn through reference.

- status: Flag indicating whether the lead was converted to a paid customer or not.
