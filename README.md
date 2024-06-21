# Homeless-Shelter-Analysis
Final project for my "Applied Statistical Methods" class. The project required to do 3 different analyses in R, one being a difference in means, another being a categorical analysis, and the last being a regression analysis. This class assumes introductory statistics knowledge, so we focused on assumption exploration and how to approach an analysis when assumptions are not met.

**Background Information**

The dataset "HomelessShelter.csv" captures information on individuals seeking assistance from a homeless shelter in 2019. This dataset is useful for gaining insights into the demographics and circumstances surrounding individuals experiencing homelessness, and sheds light on the factors that may influence their experiences within shelter programs.

There are 115 observations of 9 variables. The dataset was already cleaned.

_Variables:_

AGE: Age of client (Quantitative)

GENDER: Gender of client (Categorical--male, female) 

completed: Has the client complete the shelter’s program (Indicator)

VETERAN: Is the client a veteran (Indicator)

assistance_type: Temporary or permanent assistance (Indicator)

INCOME: Annual income of client (Quantitative)

substanceabuse: Does the client have substance abuse (Indicator)

probation: Is the client on probation (Indicator)

NIGHTS: Number of nights the client has stayed at the shelter (Quantitative)

**Analysis 1: Difference in Means via T-Test**

Analyzing the difference in mean age by gender in a homeless shelter dataset is crucial for tailoring support services, allocating resources efficiently, developing targeted policies and interventions, and improving outreach efforts.

_T-test Assumptions:_

Sampling data is approximately normal
Outcome data is quantitative
Independent observations
Homogeneity of variances

_Result:_

With a p-value of 0.0003009 (less than our alpha level of 0.05), we reject our null hypothesis. We have enough evidence to claim a statistically significant difference in the age of clients between males and females.

**Analysis 2: Test of Proportions via Chi Sq Test of Independence**

The relationship between substance abuse and probation status is important for creating interventions, allocating resources, assessing support needs, guiding policy development, improving rehabilitation programs, and contributing to long-term solutions for homelessness.

_Result:_

With a p-value of 0.03481 (below our alpha of 0.05), we reject our null hypothesis. We have sufficient evidence to conclude that substance abuse and probation status are associated.

**Analysis 3: Regression**

Analyzing the variables that most impact the number of nights stayed at the homeless shelter is important for tailoring services to specific demographics and efficiently allocating resources.

_Analysis Plan:_

Create full linear model
Determine best subset of variables
Check assumptions
Form conclusion
Model Selection

_Tools:_

OLS Regression using the olsrr package in R
Criteria: Akaike Information Criterion (AIC) and Mallows' Cp
Best Subset of Variables: AGE, substanceabuse, completion

_Assumptions_

Independent Errors
Linear relationship between Y and X
Constant variance across all values of X (homoscedasticity)
Given X, the Y’s are independent
Errors follow a normal distribution
Quantitative Outcome Variable

_Results:_

Although we identified a significant relationship between the number of nights stayed and the variables age, substance abuse, and completion of the shelter program, the assumptions of normality and homoscedasticity were not fully met. Further data transformation or robust regression is needed for more statistically sound results.

**Findings:**
- **Gender and Age:** Statistically significant difference in the age of clients between males and females.
- **Substance Abuse and Probation Status:** Sufficient evidence to conclude that substance abuse and probation status are associated.
- **Regression Analysis:** Identified AGE, substanceabuse, and completion as significant predictors for the number of nights stayed at the shelter, although further data transformation is necessary to meet all regression assumptions.
