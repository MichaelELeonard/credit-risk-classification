# Week 20 Challenge - Credit-Risk-Classification

<img src="ReadMe Pics/Pic 12.png" width="648" height="391">

In this challenge, we were tasked to utilize a supervised machine learning logistic regression model to evaluate loan risk. A dataset of lending activity from a peer-to-peer lending services company was provided to build a model that could identify the creditworthiness of borrowers.   


## Split the Data into Training and Testing Sets

### Read `lending_data.csv` data into a Pandas DataFrame.

 The data was read into a Pandas DataFrame for analysis.  
<br>
<img src="ReadMe Pics/Pic 1.png" width="858" height="167">

<br>


The “loan_status” column was removed from the DateFrame and it was placed in its own DataFrame resulting in two standalone DataFrames of data.  The two Dataframes can be viewed below. 

<br>
<img src="ReadMe Pics/Pic 3.png" width="785" height="155">
<img src="ReadMe Pics/Pic 2.png" width="299" height="136">


## Create a Logistic Regression Model with the Original Data

### Fit a logistic regression model by using the training data.

The data in the two Dataframes were portioned into groups that were used to train and test the logistic regression model.  The data was the fit to the model and predictions were tabulated. The resulting data comparing predicted and actual results was read into a DataFrame for further examination.  

<img src="ReadMe Pics/Pic 16.png" width="390" height="42">

<br>

<img src="ReadMe Pics/Pic 4.png" width="202" height="277">
<br>



## Evaluate the model’s performance

### Generate a confusion matrix.


<br>
<img src="ReadMe Pics/Pic 5.png" width="317" height="74">

### Print the classification report.

<img src="ReadMe Pics/Pic 18.png" width="489" height="177">
<br>

## Credit Risk Analysis Report
### Overview of the analysis

In this Challenge, we structured a machine learning model to evaluate loan risk of borrowers.  This determination was based off of a variety of factors including <br>
* Loan Size
* Interest Rate
* Borrower Income
* Debt to Income Ratio
* Number of Revolving Accounts
* Past Negative Credit Marks
* Total Debt

A Logistic Regression Model was established using the original data and a confusion matrix and classification report was run to evaluate the model’s performance.  



### The Results

The Confusion Matrix results show:
<br>
* 18,679 individuals were CORRECTLY identified as credit worthy (True Negative)
* 558 individuals were CORRECTLY identified as not credit worthy (True Positive)
* 67 individuals that were INCORRECTLY identified as not credit worthy (False Negative)
* 80 individuals were INCORRECTLY identified as credit worthy (False Positive)

The rows and columns were summed and compared to assess accuracy and precision.  Both aggregate totals were 19,384 so we can consider the model to be accurate and precise.

<img src="ReadMe Pics/Pic 17.png" width="421" height="287">

The Classification Report results show:
<br>
* The accuracy of the entire model was 99%
* The precision for Healthy Loans was 100% 
* The recall for Healthy Loans was 100%
* The precision for High-Risk Loans was 87% 
* The recall for Healthy Loans was 89%  

### Summary
Some trends can be observed when examining the results of the Logistic Model.  Overall, the model performed exceptionally well with a 99% accuracy rate. The model excelled at identifying healthy loans scoring a 100% success rate in precision and recall.  The model did drop off when identifying high-risk loans scoring 87% in precision and 89% in recall.  One potential reason for the drop in high-risk loans scores may be due data to the sample size provided to the model, as the high-risk loans only accounted for 3.2% of the total data examined.  Increasing this sample size may provide greater learning opportunities for the model, thus boosting its performance.  It may also be prudent to expose this data to other machine learning models to see if the output performance increases.            
