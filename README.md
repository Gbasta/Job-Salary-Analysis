# Job Salary Analysis
Analysis and interpretation of data based on data roles in the job market.

The data has features of job title, work year, experience level, salary, remote ratio, and company size.
My goal with this code is to see how good of a predictor each of these features are for salary in the job market.

This code uses and compares 4 different MCMC models to determine which is best, then analyzes the results.
To determine if a model is good enough for predicting, I analyzed the r-hat, neff ratio, trace plots, and autocorrelation for each MCMC model.

To compare the predicting accuracy of each of the models, I created visualizations with a prior predictive check to see the errors of each model and then used ELPD with loo to verify.

This all resulted in a hierarchical model to be best at predicting job salaries given the features in the dataset. This is expected, as a hierarchical model groups the jobs into groups based on their job title, whereas the other models were pooling all the jobs together to get more general results.

# Results
The hierarchical model determines that there is no significant relationship between remote ratio and the year worked, but found the following significant relationships:
* Being hybrid lowers salary compared to being in person or fully remote
* Being in a small company lowers salary compared to being in any other sized company
* Experience level increases salary as expected, going up from the lowest to highest ranging from entry level, mid level, senior level, and the highest at executive level
The model also shows that, of the most popular data jobs, the jobs that are named "Data Architect" get paid the most, while "Data Analysts" get paid the least.
