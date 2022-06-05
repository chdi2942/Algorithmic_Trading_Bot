# Algorithmic_Trading_Bot

# Machine Learning Trading Bot

In this program we will assume the role of a financial advisor at one of the top five financial advisory firms in the world. 

The steps for this program are divided into the following sections:

* Establish a Baseline Performance

* Tune the Baseline Trading Algorithm

* Evaluate a New Machine Learning Classifier

* Create an Evaluation Report

#### Establish a Baseline Performance

In this section, we'll run the provided starter code to establish a baseline performance for the trading algorithm. 

1. Import the OHLCV dataset into a Pandas DataFrame.

2. Generate trading signals using short- and long-window SMA values. 

3. Split the data into training and testing datasets.

4. Use the `SVC` classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. Review the predictions.

5. Review the classification report associated with the `SVC` model predictions. 

6. Create a predictions DataFrame that contains columns for “Predicted” values, “Actual Returns”, and “Strategy Returns”.

7. Create a cumulative return plot that shows the actual returns vs. the strategy returns. Save a PNG image of this plot. This will serve as a baseline against which to compare the effects of tuning the trading algorithm.

8. Write your conclusions about the performance of the baseline trading algorithm in the `README.md` file that’s associated with your GitHub repository. Support your findings by using the PNG image that you saved in the previous step.

#### Tune the Baseline Trading Algorithm

In this section, we’ll tune, or adjust, the model’s input features to find the parameters that result in the best trading outcomes. (You’ll choose the best by comparing the cumulative products of the strategy returns.):

1. Tune the training algorithm by adjusting the size of the training dataset. To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your `README.md` file. Answer the following question: What impact resulted from increasing or decreasing the training window?

2. Tune the trading algorithm by adjusting the SMA input features. Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your `README.md` file. Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?

3. Choose the set of parameters that best improved the trading algorithm returns. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your `README.md` file.

#### Evaluate a New Machine Learning Classifier

In this section, we’ll use the original parameters and apply them to the performance of a second machine learning model:

1. Import a new classifier, such as `AdaBoost`, `DecisionTreeClassifier`, or `LogisticRegression`. (For the full list of classifiers, refer to the [Supervised learning page](https://scikit-learn.org/stable/supervised_learning.html) in the scikit-learn documentation.)

2. Using the original training data as the baseline model, fit another model with the new classifier.

3. Backtest the new model to evaluate its performance. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns for this updated trading algorithm, and write your conclusions in your `README.md` file. Answer the following questions: Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?

## Evaluation Report

### Our findings show that the standard SVC model outperformed the LogisticRegression model.  The SVC had a cumulative return of 1.52 compared to the actual return of 1.39.  This demonstrates that the SVC model outperformed a simple "buy and hold" strategy for the asset over the time period that we tested.  The LogisticRegression model had a cumulative return of 1.15 versus the actual return of 1.39.  This means that it did not outperform the "buy and hold" strategy or the regular SVC model.  We can also see, however, that the LogisticRession model had a greater accuracy in its predictions than the SVC model, which is shown in the tables below.

## SVC Model
![image](https://user-images.githubusercontent.com/96210633/172035241-ba27e021-9dae-4556-84ba-db2d8f5d767c.png)

## LogisticRegression Model
![image](https://user-images.githubusercontent.com/96210633/172035261-405607b6-5966-4189-8b5d-1f427fcf4cb0.png)

## SVC Cumulative Returns vs. Actual Returns
![image](https://user-images.githubusercontent.com/96210633/172035297-ac20ab3a-0d8c-4b48-80d6-cb56909fe672.png)

## LogisticRegression Returns vs. Actual Returns
![image](https://user-images.githubusercontent.com/96210633/172035319-93a9d424-0eb6-4e97-9823-64cf638fe29f.png)

