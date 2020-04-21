<!DOCTYPE html>
<html>
<body>

<h1>Overview</h1>
COVID-19 has infected more than 10,000 people in South Korea. KCDC (Korea Centers for Disease Control & Prevention) announces the information of COVID-19 quickly and transparently. This structured dataset is collected in line with the report materials of KCDC and local governments. Intuitively, we are collecting insigts into the dataset by answering some critical questions.

<h3>Acknowledgements</h3>
Thanks sincerely to all the members of KCDC and local governments.
Source of data: KCDC (Korea Centers for Disease Control & Prevention)
https://www.kaggle.com/kimjihoo/coronavirusdataset

<h2>Data preparation</h2>
Data should be checked for the following items:
<br />
 - Each column is a variable, and each row is an individual
 <br />
 - Number of columns and rows in each of datasets
 <br />
 - Missing data, and whether those missing data should be imputed or removed
 <br />
 - Data types check (if they are loaded as the datatype as we expected)
 <br />
 - Exploratory plots like bar charts and histograms to better understand the data
 <br />

 <h3>Imputing missing data</h3>
I first check for the missing value in the basic table called PatientInfo which is the general epidemiological data of COVID-19 patients in South Korea. There was no all missing columns, but there exist columns with more than 75 percent but not fully null. We are going to impute numerical value simply with the mean value. However, those columns are not important for the later analysis here and we do this as a good practice. For the categorical missing values, I first cerated dummy variables for each of the categories, then replaced the missing values by the categories with the highest frequency among the others. The codes are all included in the jupyter notebook under Imputing missing data section.  

<h3> Data type check </h3>
Sometimes, the expected datatypes of the read dataset are not teh same as what we expected. For example, date and time data columns are commonly loaded as object type. The object type will prevent us from working or visualizing this column for time-series analysis. So, we need to change that object datatype into date/time datatype before any further analysis. The codes are all included in the jupyter notebook under Data type check section.   

<h3> Exploratory plots </h3>
I explored some data field as necessary, and used my findings to solve the questions in the next section.
One of the intersting insigts is that how the virus has affected people in different ages. As you can see int he following picture, people born in 1995 and 1996 have the highest number of incidents.

<img src="plots/birth.png" style="vertical-align:bottom">

In terms of gender, women (1798) have overtaken men (1420)

<img src="plots/gender.png" style="float:center">


<h2>Insights and Questions</h2>
(1) What are the top 10 sources of infection? 
<br />
(2) How different levels of community interactions are related in terms of virus spread? 
<br />
(3) What were the top 10 provinces where COVID-19 spread the most?
<br />
(4) How different confirmed and recovered cases change over the last month?
<br />
(5) How daily web searches on COVID-19, cold, or flu are related?
<br />
<h6>Modeling</h6>

</body>
</html>

