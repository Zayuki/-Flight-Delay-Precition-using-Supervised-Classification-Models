# Flight Delay Prediction Using Supervised Classification Model

<img src='https://i1.wp.com/theluxurytravelexpert.com/wp-content/uploads/2014/08/flight-delays1.jpg?ssl=1' width='669'>

## Introduction

There are various factors that can contribute to flight delays, including weather conditions, maintenance issues, and congestion at airports. For example, a study conducted by the Federal Aviation Administration found that in 2020 approximately 33.4% of flight delays were caused by weather-related issues, such as thunderstorms and high winds (United States Department of Transportation, 2022). The consequences of flight delays can be severe for both passengers and the aviation industry. Passengers may miss connections or important events, leading to additional expenses and disruptions to their travel plans. For airlines and airports, flight delays can result in lost revenue, as well as damage to their reputation and customer satisfaction (Efthymiou et al., 2018).

Therefore, analysis of flight delay has become a popular research area. However, most of the previous studies did not focus on identifying main factors of flight delay. Besides, models in these studies were trained with data from single airport which is insufficient to predict flight delay in a long run. By training supervised classification machine learning models with long term flight data, the classifier model will be able to predict flight delay accurate and identify factors that usually cause delay. This helps airlines and airports can take proactive measures to minimize the impact of delays and improve the overall efficiency of the aviation system.

## Objectives

1) To develop supervised classification machine learning models that can predict delayed flight accurately.

2) To compare the performance of different supervised classification models on predicting flight delays.

3) To identify significant factors that causing flight delay.

## Dataset

| Name                                      | 2016 - 2018 Flight Delays and Cancellations  |
|-------------------------------------------|----------------------------------------------|
| File size                                 | 2.18 GB                                      |
| Source                                    | The U.S. Department of Transportation's (DOT) Bureau of Transportation Statistics |
| URL                                       | https://www.kaggle.com/datasets/usdot/flight-delays?select=flights.csv |
| File size                                 | 2.18 GB                                      |
| Year                                      | 2016 - 2018                                 |
| NaN values                                | 115,332,132                                |
| Description                               | This dataset contains a summary information on the number of on-time, delayed, canceled, and diverted flights published by U.S. Department of Transportation's Air Travel Consumer Report from 2016 to 2018. |
| Columns                                   | 27                                           |
| Rows                                      | 1,850,5725                                  |
| NaN values                                | 115,332,132                                |

## Methodology (Flow Chart)

![image](https://github.com/Zayuki/Flight_Delay_Prediction_Using_Supervised_Classification_Model/assets/67309677/abb0a62c-885b-4342-870c-a58b185ea324)


## Results

### Models Performance
From all four models, we can clearly identify that Random Forest outperforms the rest of the models with the highest accuracy, recall, F1-Score and AUC score. Another tree-based ensemble classifier, Decision Tree also shows good performance with the second highest of accuracy, recall, F1-score, and AUC score.

| Model              | Accuracy   | Recall    | Precision | F1-Score  | AUC Score |
|--------------------|------------|-----------|-----------|-----------|-----------|
| Logistic Regression| 86.64%     | 70.56%    | 88.84%    | 78.65%    | 82.91%    |
| Decision Tree      | 86.66%     | 73.41%    | 86.28%    | 79.33%    | 83.58%    |
| Random Forest      | 86.92% (TOP)   | 75.24% (TOP)   | 85.51%    | 80.05% (TOP)   | 84.21% (TOP)   |
| Naïve Bayes        | 79.60%     | 41.88%    | 99.08% (TOP)  | 58.88%    | 70.84%    |


### Identify Top 3 features causing flight delay
Since random forest outperforms the other models, thus we identify the most important feature that is used to predict a flight delay in Random Forest.

![image](https://github.com/Zayuki/Flight_Delay_Prediction_Using_Supervised_Classification_Model/assets/67309677/9e0e6889-9689-4954-b27a-f4d3fb92c78c)

From the chart above, we can conclude that “DEP_DELAY”, “NAS_DELAY” and “TAXI_OUT” are the top three important features in identifying a delayed flight. It is expected that “DEP_DELAY” is ranked as the topmost important feature because there is high probability of the flight is delayed if it is delayed during departure.

## Conclusion
This project performed flight delay prediction by adopting supervised machine learning approach in the form of binary classification. Four supervised classification algorithms were used for flight delay prediction, and five measures were used for algorithms performance evaluation.

The results show that the highest values of accuracy, recall, precision, F1-score, and AUC score are generated by Random Forest. Another tree-based classifier, Decision Tree also shows good performance. Besides, “DEP_DELAY” was ranked as the most important feature in predicting delayed flight.

## References
Efthymiou, M., Njoya, E. T., Lo, P. L., Papatheodorou, A., & Randall, D. (2018). The impact of delays on customers’ satisfaction: An empirical analysis of the British Airways on-time performance at Heathrow Airport. SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3253232

United States Department of Transportation. (2022, January 10). Understanding the reporting of causes of flight delays and cancellations. Understanding the Reporting of Causes of Flight Delays and Cancellations. Retrieved January 9, 2023, from https://www.bts.gov/topics/airlines-and-airports/understanding-reporting-causes-flight-delays-and-cancellations
