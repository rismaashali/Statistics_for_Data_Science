# Statistics for Data Science
# Definition of Statistics
Statistics is a set of mathematical methods and tools that enable us to answer important questions about data.
# Definition of Data
Data is a collection of facts, such as numbers, words, measurements, observations or just descriptions of things
- Qualitative data are measures of 'types' and may be represented by a name, symbol, or a number code. Qualitative data are data about categorical variables (e.g. what type).
- Quantitative data are measures of values or counts and are expressed as numbers. Quantitative data are data about numeric variables (e.g. how many; how much; or how often).
# Types of Variables
- Numerical
  - Continuous
  - Discrete
- Categorical
  - Ordinal
# Probability Concept
Probability is a measure of the likelihood of an event to occur. Many events cannot be predicted with total certainty. Probability can range from 0 to 1, where 0 means the event to be an impossible one and 1 indicates a certain event.
Probability of an event = (Number of Favorable Outcomes) / (Total Number of Possible Outcomes)
# Types of Statistics
-	Descriptive Statistics
-	Inferential Statistics
# Descriptive Statistics
Organizing, summarizing, and presenting data in an informative way
-	Measure of Central Tendency
-	Measure of Spread / Dispersion
-	Skewness
-	Correlation
## Measure of Central Tendency
### Mean
Mean represents the average of the given collection of data. It is applicable for both continuous and discrete data.
•	All scores in distribution affected the mean
•	Many samples from the same population will have similar means
•	The mean will change if we add extreme value
### Median
Median represents the mid-value of the given set of data when arranged in a particular order.
•	Doesn't change much by extreme values (outliers).
•	Median is a robust statistics.
### Modus
The most frequent number occurring in the data set is known as the mode.
## Measure of Spread / Dispersion
### Range
It is simply the difference between the maximum value and the minimum value given in a data set.
### Variance
-	Variance is the expected value of the squared variation of a random variable from its mean value, in probability and statistics.
-	Informally, variance estimates how far a set of numbers (random) are spread out from their mean value.
### Standard Deviation
The standard deviation is a measure of the amount of variation or dispersion of a set of values.
-	A low standard deviation indicates that the values tend to be close to the mean of the set.
-	While a high standard deviation indicates that the values are spread out over a wider range.
## Skewness
Skewness is a measure of the asymmetry of a distribution. A distribution is asymmetrical when its left and right side are not mirror images.
There are 3 types of skewness
- Positive skewness : A positive skew distribution is longer on the right side of its peak than on its left. Positive skew is also referred to as right-skewed
- Negative skewness : A negative skew distribution is longer on the left side of its peak than on its right. Negative skew is also referred to as left-skewed
- No Skew : When a distribution has no skew, it is symmetrical. Its left and right sides are mirror images.
## Correlation
Correlation is a statistical measure that expresses the extent to which two variables are linearly related (meaning they change together at a constant rate). It’s a common tool for describing simple relationships without making a statement about cause and effect.
In Python we can see correlation in data by using DataFrame.corr()

## Outliers and Missing Value
### Check Outliers using Boxplot
- A box plot is a good way to show many important features of quantitative (numerical) data.
- It shows the median of the data. This is the middle value of the data and one type of an average value.
- It also shows the range and the quartiles of the data. This tells us something about how spread out the data is.

### Check Outliers using IQR
IQR tells how spread the middle values are. It can be used to tell when a value is too far from the middle. 
An outlier is a point which falls more than 1.5 times the interquartile range above the third quartile or below the first quartile. 
- Step 1: Arrange the data in incresing order
- Step 2: Calculate first (q1) and third quartile (q3) 
- Step 3: find interquartile range (q3-q1)
- Step 4: Find lower bound (q1*1.5)
- Step 5: Find upper bound (q3*1.5)
Anything that lies outside of lower and upper bound is an outlier

#Handling Outliers
One of the simplest way to handle outliers is to just remove them from the data or . If you believe that the outliers in the dataset are because of errors during the data collection process then you should remove it or replace it with NaN.

### Handling missing value
Missing values are usually represented in the form of Nan or null or None in the dataset.
In this case, we will be filling the missing values with a certain number. The possible ways to do this are:
- Filling the missing data with the mean or median value if it’s a numerical variable.
- Filling the missing data with mode if it’s a categorical value.
- Filling the numerical value with 0 or -999, or some other number that will not occur in the data. This can be done so that the machine can recognize that the data is not real or is different.
- Filling the categorical value with a new type for the missing values.
You can use the fillna() function to fill the null values in the dataset.

# Inferential Statistics
Inferential statistics provides a way to draw conclusions about broad groups or populations based on a set of sample data. In some instances, it’s impossible to get data from an entire population or it’s too expensive. Inferential statistics solves this problem.
Inferential statistics is process to obtain conclusion based on sample that aims to generalize of the population.

## Confidence Intervals
A confidence interval, in statistics, refers to the probability that a population parameter will fall between a set of values for a certain proportion of times. Analysts often use confidence intervals than contain either 95% or 99% of expected observations. Thus, if a point estimate is generated from a statistical model of 10.00 with a 95% confidence interval of 9.50 - 10.50, it can be inferred that there is a 95% probability that the true value falls within that range.

## Hypothesis Testing
Hypothesis Testing is a type of statistical analysis in which you put your assumptions about a population parameter to the test. It is used to estimate the relationship between 2 statistical variables.
