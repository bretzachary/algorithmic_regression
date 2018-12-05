[source](https://www.stata.com/support/faqs/statistics/stepwise-regression-problems/)
Frank Harrell’s comments:

Here are some of the problems with stepwise variable selection. 
1. It yields R-squared values that are badly biased to be high. 
2. The F and chi-squared tests quoted next to each variable on the printout do not have the claimed distribution. 
3. The method yields confidence intervals for effects and predicted values that are falsely narrow; see Altman and Andersen (1989).
4. It yields p-values that do not have the proper meaning, and the proper correction for them is a difficult problem. 
5. It gives biased regression coefficients that need shrinkage (the coefficients for remaining variables are too large; see Tibshirani [1996]). 
6. It has severe problems in the presence of collinearity. 
7. It is based on methods (e.g., F tests for nested models) that were intended to be used to test prespecified hypotheses. 
8. Increasing the sample size does not help very much; see Derksen and Keselman (1992). 
9. It allows us to not think about the problem. 
10. It uses a lot of paper. 

“All possible subsets” regression solves none of these problems. 

Conclusions


“The degree of correlation between the predictor variables affected the frequency with which authentic predictor variables found their way into the final model.” 

“The number of candidate predictor variables affected the number of noise variables that gained entry to the model.” 

“The size of the sample was of little practical importance in determining the number of authentic variables contained in the final model.” 

“The population multiple coefficient of determination could be faithfully estimated by adopting a statistic that is adjusted by the total number of candidate predictor variables rather than the number of variables in the final model.” 

References
Altman, D. G. and P. K. Andersen. 1989.Bootstrap investigation of the stability of a Cox regression model. Statistics in Medicine 8: 771–783. Copas, J. B. 1983.Regression, prediction and shrinkage (with discussion). Journal of the Royal Statistical Society, Series B 45: 311–354. Shows why the number of CANDIDATE variables and not the number in the final model is the number of degrees of freedom to consider. Derksen, S. and H. J. Keselman. 1992.Backward, forward and stepwise automated subset selection algorithms: frequency of obtaining authentic and noise variables. British Journal of Mathematical and Statistical Psychology 45: 265–282. Hurvich, C. M. and C. L. Tsai. 1990.The impact of model selection on inference in linear regression. American Statistician 44: 214–217. Mantel, Nathan. 1970.Why stepdown procedures in variable selection. Technometrics 12: 621–625. Roecker, Ellen B. 1991.Prediction error and its estimation for subset—selected models. Technometrics 33: 459–468. Shows that all-possible regression can yield models that are too small. Tibshirani, Robert. 1996.Regression shrinkage and selection via the lasso. Journal of the Royal Statistical Society, Series B 58: 267–288. 

Ronan Conroy’s comments:

I am struck by the fact that Judd and McClelland in their excellent book Data Analysis: A Model Comparison Approach (Harcourt Brace Jovanovich, ISBN 0-15-516765-0) devote less than two pages to stepwise methods. What they do say, however, is worth repeating: 
1. Stepwise methods will not necessarily produce the best model if there are redundant predictors (common problem).
2. All-possible-subset methods produce the best model for each possible number of terms, but larger models need not necessarily be subsets of smaller ones, causing serious conceptual problems about the underlying logic of the investigation.
3. Models identified by stepwise methods have an inflated risk of capitalizing on chance features of the data. They often fail when applied to new datasets. They are rarely tested in this way.
4. Since the interpretation of coefficients in a model depends on the other terms included, “it seems unwise,” to quote J and McC, “to let an automatic algorithm determine the questions we do and do not ask about our data”.
5. I quote this last point directly, as it is sane and succinct: 
“It is our experience and strong belief that better models and a better understanding of one’s data result from focussed data analysis, guided by substantive theory,” (p. 204).

They end with a quote from Henderson and Velleman's paper “Building multiple regression models interactively” (1981, Biometrics 37: 391–411): “The data analyst knows more than the computer,” and they add “failure to use that knowledge produces inadequate data analysis”. 

Personally, I would no more let an automatic routine select my model than I would let some best-fit procedure pack my suitcase. 
