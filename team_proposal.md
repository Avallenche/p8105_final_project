team_proposal
================
Wenyu Zhang
2023-11-11

# Group Members:

- Wenyu Zhang (wz2675)
- Wenwen Li (wl2926)
- Siyan Wen (sw3866)
- Linshen Cai (lc3807)

# Title:

Evaluation of Wine from Multiple Perspectives

# Motivation:

In the rich and varied world of wine, selecting the perfect bottle is an
art form guided by personal taste and often influenced by the collective
voice of ratings. However, wine ratings and scores, often seen as
benchmarks of quality, can serve as a compass for selection. The
motivation for analyzing wine evaluation and price datasets is twofold:
Explore the correlation between wine rating and their prices, providing
a data-driven approach to understanding the valuation of wines. To
develop an analysis that can illustrate the relationship between ratings
of wines and the price, thereby assisting consumers in discovering good
wines. Final Products: A well-formulated website includes plots, tables
that helps explain the ideas and issues we observed during cleaning up
the dataset and analysis for each elements inside this website.

# Data Source:

<https://www.kaggle.com/datasets/budnyak/wine-rating-and-price/code>

# Analysis:

For the dataset, linear regression is a suitable choice if we want to
predict wine prices based on the other variables, such as location of
production, wine rating, taster, and year of production. I would use
multiple linear regression, as it allows for multiple independent
variables to be considered simultaneously. In this case, wine price
would be the dependent variable, and the location of production, wine
rating, taster, and year of production would be the independent
variables. This model would help in understanding how each of these
factors influences wine prices and provide a predictive model for
estimating wine prices based on these features. Regularization
techniques like Ridge or Lasso regression might also be considered to
address multicollinearity or overfitting if necessary.

# Challenges:

Clean and merge the datasets: Missing Data: Handling missing data is one
of the main problems. The dataset may have missing values in some
columns, which could compromise the accuracy of your research. The
choices made regarding the imputation, removal, or other handling of
missing data can affect the outcome. Geographic representation: Handling
Big Datasets: The sheer amount of data in huge datasets can make
computing difficult and make EDA time-consuming. It may be necessary to
apply more effective techniques or to sample the data.

# Timeline:

- 11/08/2023: Team registration and proposal
- 11/13/2023: Project Review meeting(Finish dataset cleaning))
- 11/15/2023: Project Review meeting(Clear division of labor and start )
- 11/17/2023: Project Review meeting (with TA)
- 11/27/2023: Project Review meeting (Write draft of report))
- 11/29/2023: Project Review meeting (Finish code part of the website))
- 12/01/2023-12/05/2023: Report (Final version))
- 12/05/2023-12/08/2023: Finish website making
