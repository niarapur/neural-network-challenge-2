# Neural Network Challenge -2
Module 19 challenge

The task is to create a neural network that HR can use to predict whether employees are likely to leave the company. As HR believes some employees may be better suited to other departments, the model is built to also predict the department that best fits each employee. These two columns are predicted using a branched neural network.

# DATA
the data source is 'https://static.bc-edx.com/ai/ail-v-1-0/m19/lms/datasets/attrition.csv' consisting of 1470 rows and the follwoing columns:

Dataset
--------
Age	43
Attrition	2
BusinessTravel	3
Department	3
DistanceFromHome	29
Education	5
EducationField	6
EnvironmentSatisfaction	4
HourlyRate	71
JobInvolvement	4
JobLevel	5
JobRole	9
JobSatisfaction	4
MaritalStatus	3
NumCompaniesWorked	10
OverTime	2
PercentSalaryHike	15
PerformanceRating	2
RelationshipSatisfaction	4
StockOptionLevel	4
TotalWorkingYears	40
TrainingTimesLastYear	7
WorkLifeBalance	4
YearsAtCompany	37
YearsInCurrentRole	19
YearsSinceLastPromotion	16
YearsWithCurrManager	18

The values to be predicted include:

'Department ' : 
---------------
Human Resources	50
Research & Development	717
Sales	335

Attrition
---------
No	934
Yes	168


Model:
------
A neural network model with 2 shared layers and branched output layers for department and attrition were built:

The activation function used for the department output layer is 'softmax'. Softmax is the activation function of choice for the output layer of a model when dealing with multi-class classification, where each input belongs to one and only one class out of several possible classes. This was the ideal choice as the classes for both were also mutually exclusive. For the 'Attrition' output layer, a sigmoid with binary cross entropy function was used as it is predicting a 'Yes', 'No'.