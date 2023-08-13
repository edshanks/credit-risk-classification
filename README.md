# credit-risk-classification
Overview

This analysis seeks to classify a loan as either healthy or high-risk by using supervised machine learning to analyze historical loan data. The training data for the machine learning model includes information about the loan itself (i.e. loan size and interest rate), as well as data pertaining to the borrower (i.e. borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt). The same parameters are then used as testing data to measure the prediction capability of the model. Ideally, the model should be able to flag a potential loan as high-risk, thereby reducing financial risk for the lender. The model returns a positive result (1) for a high-risk loan and a negative result (0) for a healthy loan. 

The dataset set contains information from 77,536 previous loans. 97% of the loans were healthy, while only 3% were high-risk. The prevalence of healthy loans in the dataset has the potential to skew the model’s overall accuracy because these healthy loans have a larger impact on the accuracy of the model. This analysis, therefore, relies on precision and recall as additional metrics of effectiveness. 

In the context of this analysis, a false negative is a loan that is deemed healthy by the model, but is actually high-risk. Authorizing a high-risk loan carries much more risk for the lender than denying a healthy loan. In the latter case, the lender only misses out on potential revenue. In the former, the lender becomes exposed to potentially large losses. Therefore, the ideal model should minimize the number of false negatives. Recall correlates negatively with the rate of false negatives (i.e. a higher recall means less false negatives) and is therefore the most important metric when evaluating the effectiveness of this model. Precision, although not as crucial of a metric as recall, is important because it measures how often the model flags a loan as high-risk although it is actually healthy (i.e. the false positive rate).



Model Analysis

Accuracy - 99%

This model has an overall accuracy rate of 99%, meaning that it correctly predicts loan status 99% of the time. Given the nature of the dataset, namely the prevalence of healthy loans, this metric alone does not offer a comprehensive evaluation of the model.

Precision - 84%

With a precision rate of 84%, this model exhibits a less than optimal, yet sufficient ability to correctly classify healthy loans. This means that the model has a 16% chance of labeling a loan high-risk, when it is in fact healthy. This is a tolerable false positive rate because false positives represent far less risk to a lender than false negatives. False positives would lead to missed revenue opportunities for a lender, but would not necessarily increase a lender’s risk profile.

Recall - 98%

As mentioned above, recall is the most important metric for evaluating the effectiveness of the model because it indicates how often a model generates false negatives. A high recall indicates a low false negative rate. With a recall of 98%, this model has very low false negative rate. This means that this model is not likely to label a high-risk loan as a healthy loan and is therefore suitable for use by a lender, whose main concern would most likely be avoiding high-risk loans. 



Conclusion

Although this model could mistakenly reject some healthy loans, it would effectively flag high-risk loans and aid lenders greatly with regards to risk management. I would therefore recommend this model for use by lenders.
