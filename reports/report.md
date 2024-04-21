# Predictive maintenance modeling on a wind turbine bearing

By Magnus S. Nordeide, Markus A. Y. Thorsnes, 21.04.2024


# Introduction

Predictive maintenance is an emerging field where the goal is to save resources on maintenance of components by using a conditional maintenance program instead of an interval time based maintenance program. 

Machine learning opens the possibility to predict when a fault is going to happen, before it happens, by using past sensor data and past failure data. 

Some of the issues on predictive maintenance involve applying past data correctly and in an informative manner, and properly understanding and making decisions based on the information given by the outputs of the models. 


# Part 1: Understanding Maintenance

There are three main maintenance programs that are commonly discussed: 1) Preventative maintenance, 2) Reactive maintenance, 3) Predictive maintenance.
Preventive maintenance is the act of replacing before an increased degradation state of the component has started. Its replacing part in advance to their failure. Reactive maintenance is replacing components after failure has occurred. While predictive maintenance aims to make an informed decision on the maintenance event based on the condition of the equipment to avoid failure or prematurely replacing the component without information ideally.
Traditionally the maintenance is done reactively, so the challenge here is to improve this process by seeing the failure in advance and doing maintenance before failure occurs.
Alot of methodology is improving rapidly due to the current focus on machine learning in general. However, as a whole the field does not rely on only machine learning, but utilizes other models such as physical and statistical. In addition hybrid models are researched. Predictive maintenance extends into the field of prognostics health management where the decisions for maintenance is the focus. This is where predictive maintenance metrics are used to actually plan maintenance events.

<img src="../references/figure1.png" alt= “” width="600">
<sub>Figure 1: Cost increase with reactive maintenance [2]</sub>


# Part 2: Predictive maintenance in action: Case studies and experiments



# Part 2: Predictive maintenance in action: Case studies and experiments

```
## Methodology


Our project will be based on a quantitative methodology. For this project we will be using publicly available wind turbine data from a spanish company named EDP. The data consists of six datasets that are structured in the following manner:

2016 sensor readings from 55 different sensors on all wind turbines. 
2017 sensor readings from 55 different sensors on all wind turbines. 
2016 Onsite weather data
2017 Onsite weather data
2016 Failure data
2017 Failure data

The data is formatted so that we have an average, a max and a min value for a certain time interval in the data. So it's not totally raw, and has been pre processed in some way beforehand. The datetime is included in the dataset also. The first step of the project was to get a feel for the data and open it in python. In Notebook_blogpost_tabular_data.ipynb the exploration of the data is done in a systematic way to get a feel for the data, and familiarize it to working with the models. Later separate models were created.

In this project we will use linear regression, random forest, XGBoost and neural networks for modeling of the prediction. This way we get a good feel for the different machine learning models that are often associated with tabular learning. 

* Description of the experimental design and methodology. 
* Specify the criteria for selecting case studies and experiments.
* Data collection and analysis techniques.
```

## Case studies (wind turbine)

For our case study we want to predict the temperature of a bearing in turbine 7. Our goal is to accurately model the bearing temperature using different machine learning models, and then comparing them by using the root mean square metric.


In our case study we are focusing on wind turbine number 7, due to available failure data there. 

One of the sensor data readings in the dataset is temperature data on a bearing. This will be our dependent variable that we want to predict. 






<img src="../references/table1.png" alt= “” width="600">

<sub>Table 1: RMSE of the models on the testset. </sub>


Linear regression and XGBoost was trained for the whole of 2016, and the model was validated on an interval before the failure of the generator occurred. 


```
* Detailed presentation of selected AgTech projects or experiments. (spanish windturbine farm off the coast of africa, turbine 07, etc... )
* Analysis of the data collected.
* Results and findings.
```



# Part 3: Implications and future directions
Future DAT255 projects related to predictive maintenance can implement different types of models. Examples can be to do something with vibration data to use. It would also be interesting to see how many timesteps into the future one could return accurately by returning multiple temperatures rather than one. It's also possible to go further into the models themselves to evaluate why performance differs and how one can leverage for example deep learning as efficiently as possible. This may require domain knowledge though.

Further work would also include making conditional functionality based on the deviation of predicted temperature values and actual temperature values. Ultimately, we want to predict when a bearing is going to break. This would require implementing a threshold and some sort of conditional scheme. For example, if the temperature of the bearing is high AND a deviation threshold is met, we want to take action, and quickly maintain the bearing. This would require further planning and work. 


## Discussion
Our results show that even the most basic approaches do work for our one validating failure. However, this is important to note that the models should be tested for multiple scenarios as failures occur on the turbine.

An important result is that the deviation between the measured temperature and the prediction is observable. This is important because it indicates that we are doing the correct method of measuring to capture the degradation. The models could be state of the art, but if the sensors don’t act as a health indicator for what we are trying to analyze we are left with no usable result. 

Improvements to the model are still possible, and there are things that can be further explored. We only used the data from one turbine for training while there are many from the same wind farm available in the same dataset. However, it's not certain that this will lead to better results because it would mean training on a more general basis than if it's the exact same turbine that is the goal of being predicted. If the goal is to have a more robust model though. This can be a good idea.

There was also a hypothesis that the XGBoost model would outperform the other models based on the previous research. However, it performed worse than expected

When it comes to splitters, there may also be a possibility to capture more of the seasonal effects from time series if one trains on more data. Right now the models are  mostly trained on 2016 data and that data is split, so the model was not trained on a full year. In the process of the project, this was tested once, and appeared to actually reduce the accuracy just a little bit, which was opposite of the hypothesis for that scenario.

The plan was also to use a tool called DBScan to clean the data with a domain knowledge standpoint. We don’t want to include data where the sensor was damaged or the wind turbine out of service. As it stands, these factors all impact the accuracy of the model’s predictions. Neural networks are especially sensitive to long tail distributed data, which we see the 2016 training has due to sensor failure.

<img src="../references/figure2.png" alt= “” width="600">
<sub>Figure 2: Actual training data (in blue) and prediction (in orange). From the random forest model. We can see how faulty sensors impact the data that’s being trained on.</sub>

While cleaning the data for the random forest implementation slightly worsened the RMSE of the training and validation set, it should make the model more robust to timesseries changes and variations. As a result, predictions made about the bearing temperature as time goes will be more accurate relative to predictions made when not cleaning the data.







```
* Interpretation of results. (RMSE differences and which model performed best)
* Implications for the future of agriculture and AgTech. (machine learning for maintenance programs)
* Challenges and opportunities. (accuracy & not sufficient quantities of failure data challenges, cost reduction opportunities)
```

## Conclusion
The conclusion of the project is that with implementation of machine learning models it is possible to make a predictor for the temperature for a bearing and validate the model against the sensor. However, it's also important to note that further work must be done to ensure consistency in the result. 

Deep models and more advanced techniques can be utilized to capture specific elements within the data. more specifically non-linear relationships between the data. Domain knowledge can also affect the choice of models because one might use mathematical relationships as a foundation for the choice of data to use to ensure one captures the right data like in [1]. 

```
* Summary of key findings and their significance. (why is e.g. random forests and XGBoost better than neural networks for tabular data?)
* Recommendations for future research and applications in AgTech
```


# Bibliography:

[1] O. T. Bindingsbø, M. Singh, K. Øvsthus, og A. Keprate, «Fault detection of a wind turbine generator bearing using interpretable machine learning», Front. Energy Res., bd. 11, s. 1284676, des. 2023, doi: 10.3389/fenrg.2023.1284676.
[2] R. Siraskar, S. Kumar, S. Patil, A. Bongale, og K. Kotecha, «Reinforcement learning for predictive maintenance: a systematic technical review», Artif Intell Rev, bd. 56, nr. 11, s. 12885–12947, nov. 2023, doi: 10.1007/s10462-023-10468-6.


# Appendices (if applicable)
* Additional data, charts, or information that support the report but are too detailed for the main text.



