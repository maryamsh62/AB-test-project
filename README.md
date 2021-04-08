# Analyze AB test results

## Introduction
In this project, we will be working to understand the results of an A/B test run by an [e-commerce website](https://en.wikipedia.org/wiki/E-commerce). The company has developed a new web page to increase the number of users who "convert," meaning the number of users who decide to pay for its product. Your goal is to work through this notebook to help the company understand if they should implement this new page, keep the old page, or perhaps run the experiment longer to make their decision.

## Conclusion

This project aimed to help the company understand if they should implement this new page, keep the old page, or perhaps run the experiment longer to make their decision.

So, we tried to find out if the landing page significantly influences the converted rate.

In Part II, our null hypothesis was that the new landing page has the same or lower converted rate than the old page, and our alternative hypothesis was that the new landing page has a higher converted rate than the old page. We performed an A/B test by using two different methods: simulating from the Null and calculating the Z-score.

This study concluded that with a p-value of 0.906, we could not reject the null hypothesis. We also calculated the z-score, which also failed to reject the null hypothesis.

In Part III, we used the logistic regression model to calculate the p-value. Although the p-value is different from what we got in the A/B test due to different null and alternative hypotheses, the result provided by the regression model agreed with the results in the A/B test. Finally, to avoid the situation in Simpson's Paradox, we introduced an additional factor in the regression model, which is the country a user lives. We looked at the individual factors and the interaction of country and landing page to see if they have significant effects on conversion.

From the Results, we can see that the coefficient of the interaction variable "UK_new_page" and "CA_new_page" are different from the coefficient of the new_page itself.

Only the intercept's p-value is less than 0.05, which is statistically significant enough for the converted rate. Other variables, in summary, are not statistically significant because all of the p-values are still larger than 0.05. Additionally, Z-score for all X variables is not large enough to be significant for predicting the converted rate. Therefore, the factors of landing page and country do not lead to a significant effect on the converted rate individually as well as interactionally.

Finally, all the result shows we failed to reject the null hypothesis. So, the company should keep the old page.
