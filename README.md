# Module14_Challenge

**Initial Variable Values:**

- Train Begin = 4/2/2015, Train End = 7/2/2015
- Test Begin = 7/6/2015, Test End = 1/22/2021
- Short Window = 4
- Long Window = 100
- (Final Actual Return = 1.39, Final Strategy Return = 1.52)
![Module14_Chart1](https://user-images.githubusercontent.com/35455504/133687140-125a97b1-387a-4435-8a28-9fef48733b3e.png)


**Modified Dates # 1**

- Train Begin = 1/1/2019, Train End = 12/31/2019
- Test Begin = 1/1/2020, Test End = 1/22/2021
- (Final Actual Return = 1.311, Final Strategy Return = 1.221)
![Module14_Chart2](https://user-images.githubusercontent.com/35455504/133690462-a9f0e32e-6d70-4faf-87be-37df06ffe656.png)


**Modified Dates # 2:**
- Train Begin = 1/1/2018, Train End = 12/31/2019
- Test Begin = 1/1/2020, Test End = 1/22/2021
- (Final Actual Return = 1.320, Final Strategy Return = 1.373)
![Module14_Chart3](https://user-images.githubusercontent.com/35455504/133690789-0a0f6bf6-340c-4a1d-b978-14f1aa071d8f.png)


**Modified SMA Fast #1 (Original Dates):**
- Short Window = 25
- (Final Actual Return = 1.60, Final Strategy Return = 1.12)
![Module14_Chart4](https://user-images.githubusercontent.com/35455504/133692203-2e6155e3-5218-4d77-b4d5-6be25ae8a496.png)


**Modified SMA Fast #2 (Original Dates):**
- Short Window = 50
- (Final Actual Return = 1.60, Final Strategy Return = 1.25)
![Module14_Chart5](https://user-images.githubusercontent.com/35455504/133692452-f8b727c0-1167-41cf-97fa-6c278525615e.png)

**Change ML Classifier to LinearRegression (Original Settings):**
- (Final Actual Return = 1.40, Final Strategy Return = 1.16)
![Module14_Challenge Chart 6](https://user-images.githubusercontent.com/35455504/133891010-35bd6e2f-d8ae-44a5-909f-94870b0948af.png)


The original settings produced a favorable Strategy Returns versus Actual Returns (1.52 versus 1.39). 

Change # 1 involved looking only more recent dates for both training and testing data, with the training data starting in 2019. This version yielded poor results for the Strategy Returns versus the Actual Returns (1.221 versus 1.311).

Change # 2 expanded the training dates by a year, starting in 2018 and going thru the end of 2019. The testing dates remained the same. This version yielded better and more favorable results for the Strategy Returns versus the Actual Returns (1.373 versus 1.320).

Change # 3 used the original settings, but changed the Short Window from 4 to 25. The change produced horrible results, as the Strategy Returns were considerably less than the Actual Returns (1.12 versus 1.60). Oddly enough, for Change # 4, increasing the Short Window from 25 to 50 produced slightly better results (1.25 versus 1.60)

Change # 5 retained the original settings but switched the Machine Learning Classifier to Logistic Regression. This change produced interesting results. By mid-2020, the Algorithm Returns were on track to significantly exceed the Actual Returns (1.5 versus 1.12). However, the Actual Returns continued to rise, while the Algorithm Returns completed a Bart formation and ended at 1.16, while the Actual Returns climbed to 1.4.

In summary, the SVC classifier model was better at maintaining a fairly parallel relationship between the Actual Returns and the Strategy Returns, while the Logistic Regression classifier exhibited periods of crossover between the two. Changing the short window was definitely not the way to improve Strategy Returns. Tweaking the training and testing dates provided mixed returns. In all, based upon the changes that were implemented, the best results came from the original settings. More teating would be needed to find something better.










