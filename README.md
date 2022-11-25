# Machine_Learning_Trading_Bot
Creating an algorithmic trading bot that learns and adapts to new data and evolving markets by enhancing existing trading signals with machine learning

# Part 1 - Establish a Baseline Performance

This first graph shows a cumulative return plot that shows the actual returns vs. the strategy returns for the SVM model

## Actual returns vs. Strategy returns for SVM
![](/Images/actual_vs_strategy_SVM.png)

### Classification Report for SVM
![](/Images/report_1_SVM.png)

## Actual returns vs. Strategy returns for chosen model Logistic Regression (LR)
![](/Images/actual_vs_strategy_LR.png)

### Classification Report for LR
![](/Images/report_1_LR.png)

*The SVM model had a better accuracy score and as can be seen by the chart is a better fit overall*

# Part 2 - Tune the Baseline Trading Algorithm
Tune the training algorithm by adjusting the size of the training dataset.

## PART 2a

*I adjusted the training window by increasing it from 3 months to 9months*

## Actual returns vs. Strategy returns for SVM - 9 months
![](/Images/SVM_9months_offset.png)

### Classification Report for SVM - 9 months
![](/Images/report_SVM_9months_offset.png)

## Actual returns vs. Strategy returns for  Logistic Regression (LR) - 9 months
![](/Images/LR_9months_offset.png)

### Classification Report for LR - 9 months
![](/Images/report_LR_9months_offset.png)

**Answer the following question: What impact resulted from increasing or decreasing the training window?

*The accuracy of the SVM model went down to 53 where as the accuracy for the Logistic Regression increased to 56.  It can also be seen visually from the chart above that the Linear Regression model has a better 'fit' in this case.  However the accuracy of the original SVM model has been reduced*

## PART 2b 
*I adjusted the SMA's by by incresing the short window to 5, and increasing the long window to 200*

## Actual returns vs. Strategy returns for SVM - SMA increase
![](/Images/SVM_5MA200.png)

### Classification Report for SVM - SMA increase
![](/Images/report_SVM_5MA200.png)

## Actual returns vs. Strategy returns for  Logistic Regression (LR) - SMA increase
![](/Images/LR_5MA200.png)

### Classification Report for LR - SMA increase
![](/Images/report_LR_5MA200.png)

**Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?

*The accuracy of the SVM increased to 56, and Logistic regression decreased.  Looking at the charts we can see the LR model looks 'off' whereas the SVM looks like an excellent 'fit' until about early 2020, and then is a bit off from actual returns afterwards*

# Part 3 - Evaluate a New Machine Learning Classifier
Backtest the new model to evaluate its performance

**Answer the following questions: Did this new model perform better or worse than the provided baseline model? --->WORSE

*The new model (Logistic Regression) actually did perform worse as can be seen from the charts and from the classification report in Part 1 above where the new model has an accuracy score of 52, and the original a 55*


**Did this new model perform better or worse than your tuned trading algorithm?

*The new model (Logistic Regression) performed worse than the tuned algorithm on all accounts except when we increased the training window to 9 months.  Only then did it have better accuracy and a better fitting chart*















