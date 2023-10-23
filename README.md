# Phase 3 Project

# TANZANIA WATER WELL CLASSIFICATION PROJECT
## AUTHOR: 
*1. Leonard Gachimu*<br>

Flatiron School Data Science Program

Due date: 23/10/2023

Technical Mentor: **Stella Waithera**

![Maasai women fetching water at a well in Tanzania](https://winrock.org/wp-content/uploads/2016/11/ARStory-Maasai.jpg)

## PROJECT OVERVIEW

This project seeks to build a Machine Learning classifier algorithm that can predict the condition of a water well (functional, functional-but-needs-repair, and non-functional), using data such as the kind of pump, when it was installed, the installer, the region, and so on.

## BUSINESS UNDERSTANDING
>Tanzania is a country in East Africa. The World Bank estimates its population at [65 million as of 2022](https://thedocs.worldbank.org/en/doc/bae48ff2fefc5a869546775b3f010735-0500062021/related/mpo-tza.pdf) and its land size is about 947,303 km2 (365,756 sq mi).

>The country comprises many lakes, national parks, and in fact, [Africa's highest point, Mount Kilimanjaro (5,895 m or 19,341 ft)](https://en.wikipedia.org/wiki/Geography_of_Tanzania).

>However, like many other sub-Saharan African countries, Tanzania is a developing country struggling to provide adequate clean water for its bulging population that is [growing at 3% per annum](https://www.worldometers.info/world-population/tanzania-population/).

>[Extreme poverty rate was 44% in 2022](https://thedocs.worldbank.org/en/doc/bae48ff2fefc5a869546775b3f010735-0500062021/related/mpo-tza.pdf) which means an increasing population is not affording the basic quality of life.
### GROUND WATER SITUATION IN TANZANIA
>Ground water development has concentrated mainly on shallow wells for domestic purposes over a wide part of the country. [Up to 90% of pumps and other equipment](https://gw-africa.iwmi.org/wp-content/uploads/sites/23/2018/10/Country_Report-Tanzania.pdf) used for water extraction fail due to a lack of repair and maintenance.

>Various actors, such as the national and regional governments, religious organizations, and foreign cooperation agencies have established many water points around the country but they are hardly enough. What is worse is that a significant number of the water points are in need of repair while others have failed altogether.

## BUSINESS PROBLEM

With the ongoing global climate change, [water scarcity has become an increasing problem in Tanzania](https://en.wikipedia.org/wiki/Geography_of_Tanzania), as some regions experience either intense and destructive rainfall or long dry spells.

According to the World Bank, [only 61% of households in Tanzania currently have access to a basic water-supply](https://www.worldbank.org/en/country/tanzania/publication/tanzania-economic-update-universal-access-to-water-and-sanitation-could-transform-social-and-economic-development), 32% have access to basic sanitation, and 48% have access to basic hygiene. About 31,000 deaths each year emanate from lack of or poor quality water and sanitation, which is costly to the economy.

The [average water project in Tanzania about USD 6,000 to USD 8,000](https://water4.org/solution/tanzania/) for a hand pump water point, impacting 600-700 lives per well. For mechanized systems, the cost is atleast USD 12,000.

The above cost is too high for a developing country, and thus, the country can only provide water to more millions of its people by following effective installation methods and proper maintenance of existing water projects.

I intend to partner with the Government of Tanzania in solving the clean and safe water crisis.

## BUSINESS OBJECTIVES
My main objectives in this project will be:

1. To build a Machine Learning classifier that will predict the condition of a water well (functional, functional-but-needs-repair, and non-functional), using data such as the kind of pump, when it was installed, the installer, the region, and so on.
2. To help the Government of Tanzania find patterns in functional and non-functional wells, to help influence how new wells are built.
3. To find the most important factors that influence whether a pump is functional, functional-but-needs-repair, or non-functional. This can guide the management of new and existing water wells.
4. To find out the geographical distribution of the three classes of water pumps, to help inform which regions need more attention in terms of repair, maintenance, and replacement.

## STUDY QUESTIONS
1. Is it possible to correctly predict whether a pump is functional, functional-but-needs-repair, or non-functional given data such as the kind of pump, when it was installed, the installer, the region, and so on?
2. Which are the 20 most important factors that influence whether a pump is functional, functional-but-needs-repair, or non-functional?
3. What is the geographical distribution of pumps in terms of the three classes of functional, functional-but-needs-repair, and non-functional?
4. Is there a relationship between a pump's total static head and its reliability?
5. What is the relationship between installation year and a pump's functionality?
6. What is the relationship between population and a pump's functionality?

## DATA UNDERSTANDING
The relevant datasets for have been provided on the Driven Data website which is hosting a competition for this project.
Data for the dependent variable in the test dataset has not been provided, therefore, I will make use of Training set values and Training set labels datasets.
**Training Data Features**
The training dataset contains 59,400 waterpoints in Tanzania and the following 39 features:

| Column           | Description                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------|
| amount_tsh       | Total static head (amount water available to waterpoint)                                      |
| date_recorded    | Date on which the row was recorded                                                       |
| price            | Individual or organization that funded installation of the well                                   |
| gps_height       | The altitude at which the water pump is located                                                   |
| installer        | Individual or organization that installed the well                                                |
| longitude        | Longitude coordinates of the water point                                                          |
| latitude         | Latitude coordinates of the water point                                                           |
| wpt_name         | Name of the waterpoint if there is one                                                            |
| num_private      | Information about this feature is unavailable                                                     |
| basin            | Name of the geographic water basin                  |
| subvillage       | Geographic location                                                                    |
| region           | Geographic location                     |
| region_code      | Coded geographic location                                              |
| district_code    | Coded geographic location                                                                    |
| lga              | Geographic location                                                                          |
| ward             | Geographic location                       |
| population       | Population around the well                                                                     |
| public_meeting   | Boolean data whether public meeting for the water pump was conducted                              |
| recorded_by      | Name of agency which recorded the water pump data                                                 |
| scheme_management| Name of scheme that manages the waterpoint                    |
| scheme_name      | Name of scheme under which the water point was established                                       |
| permit           | Boolean data describing whether the water point has permit available or not                  |
| contruction_year | Year in which the water point was constructed                                             |
| extraction_type  | The kind of extraction the waterpoint uses                       |
| extraction_type_group        | The kind of extraction the waterpoint uses                               |
| extraction_type_class      | The kind of extraction the waterpoint uses                                            |
| management       | Name of organization/authority that manages the water point                    |
| managememt_group | Category of organization/authority that manages the water point                       |
| payment          | Describes how residents pay for water                                       |
| payment_type     | Describes how residents pay for water                  |
| water_quality    | The quality of water                                                                    |
| quality_group    | The quality of water                     |
| quantity         | The quantity of water                                               |
| quantity_group   | The quantity of water                                                                    |
| source           | The source of water                                                                          |
| source_type      | The source of water                       |
| source_class     | The source of water                                                                     |
| waterpoint_type  | The nature of water point                           |
| waterpoint_type_group  | The nature of water point                        |  

## METHODOLOGY
Execution of the project involved the following:

### Data Understanding and Cleaning
I explored the datasets to understand their schema, size, data types, and examine the presence of invalid or inconsistent data such as missing values, duplicates, placeholders, and outliers.

### Data Analysis 
I analyzed the relationship between the continuous and categorical predictor variables and pump condition, which is the response variable.

### Data Visualization
I used various visualization methods such as bar plots, histograms, scatter plots, and Folium maps to display descriptive statistics and facilitate interpretation.

### Machine Learning Modelling
I built different machine learning models and evaluated their performance to pick the best based on performance scores and whether it was fitting the data appropriately (without underfitting or overfitting).  

## THE FINDINGS
### 1. Relationship Between Pump Functionality and Continuous Variables
![density_of_target_class_vs_continuous_features](https://github.com/leogachimu/Practice/assets/122081776/6ecfe0b0-013d-434a-9348-20c4cce3a4ca)

i.) For the total static head feature (amount_tsh), waterpoints with zero static head have the highest density of pumps overall. Also, among the three pump classes at this point, non-functional pumps have the highest density followed by functional pumps. Functional-needs-repair pumps are the least. Functional-needs-repair pumps are the least. However, the dataset has a high number (59.2%) of pumps with zero static head and there is no information about the high occurrence.<br>

ii.) For GPS height, functional and non-functional pumps are fairly equal when the GPS height is zero, at which point the functional-needs-repair pumps are much fewer.<br>

iii.) For the population features, waterpoints located in areas with zero population have the highest density of non-functional pumps. This is followed by functional pumps while functional-needs-repair pumps are the least. However, there is no information about whether the wells have been abandoned or the population has relocated.<br>

iv.) The density of functional pumps is higher among the newest pumps while non-functional pumps are higher among the older pumps, from around 1965 to 1990.<br>

**Geographical distribution of pump condition**

![distribution_of_filtered_wells_in_tz](https://github.com/leogachimu/Practice/assets/122081776/42bd3e96-082d-4e7a-9590-f852ceafcffc)

From the geographical map of pumps, we observe the following:

i.) There is a higher density of functional pumps in the Northern regions of Mwanza and Shinyanga, as well as the Southern region of Njombe.<br>
ii.) There is a higher density of functional-needs-repair pumps in the Northern regions of Bukoba and Arusha, as well as the Western region of Kigoma.<br>
iii.) There is a higher density of non-functional pumps in the Central region of Dodoma and the South West region of Mtwara.<br>

**total_static_head vs. pump condition**

![Box_Plot_of_Total_Static_Head_by_Pump_Condition](https://github.com/leogachimu/Practice/assets/122081776/bb4daa84-78b0-47bf-98ad-5db7e8ba27d6)

From the box plot of total_static_head vs. pump condition, we can see that the pumps having tsh above approx.125,000 are all functional. Therefore, the higher the tsh the higher the probabilty of a pump being functional.

### 2. Relationship Between Pump Functionality and Categorical Variables
![histograms_of_categorical_features](https://github.com/leogachimu/Practice/assets/122081776/a0fad8b9-f2ae-4c6f-a484-99355d513346)

From the different visualizations of categorical variables, we notice that some classes of categories are more popular than others. For example, Iringa and Kilimanjaro regions have the highest number of pumps. The never-pay payment scheme is most popular and over 40,000 out of 59,400 wells have soft water quality.
![distribution_of_target_class_vs_categorical_features](https://github.com/leogachimu/Practice/assets/122081776/40e5ed37-96da-4e7c-9799-9a70b3b2bedf)

From the distribution of pump functionality class for each class of a categorical variable, we notice that the functional pumps are more frequent than functional-needs-repair and non-functional pumps. 

A notable deviation from this trend is the never-pay class of the payment-type category, where non-functional pumps are more than the other classes of pumps.

### 3. Predictive Modelling Results

<img width="327" alt="performance_scores_of_different_machine_learning_models" src="https://github.com/leogachimu/Practice/assets/122081776/5714beec-b010-46f5-9001-9af840c75df6">

From the predictive section, I conclude that it's possible to correctly predict the condition of a pump given the data features from the Ministry of Water in Tanzania.

The XGBoost model is the best for predicting whether a pump is functional, functional-needs-repair or non-functional given the different data features provided. It has an **accuracy score of 0.800 (80%)**, an **F1-score of 0.788**, a **precision of 0.797**, and a **recall of 0.800**. Even though the Random Forest model has slightly higher scores, the train scores show that it is overfitting the data while the XGBoost is a good fit (not underfitting or overfitting).

**Classification Report of XGBoost Model:**

                         precision    recall  f1-score   support

             functional       0.78      0.91      0.84      5465
functional needs repair       0.62      0.21      0.31       662
         non functional       0.85      0.74      0.79      3920

               accuracy                           0.80     10047
              macro avg       0.75      0.62      0.65     10047
           weighted avg       0.80      0.80      0.79     10047
           
**Confusion Matrix**

![Confusion_matrix_for_xgbboost](https://github.com/leogachimu/Practice/assets/122081776/1373ca61-7030-41bf-99c6-a9de7bf15920)

To save on the cost of attending to pumps whose condition has been erroneously predicted, or ignoring faulty pumps predicted to be in good condition, I started with the intention of minimizing both False Positives (high precision) and False Negatives (high recall). The XGBoost model has high scores for both precision and recall, at 0.797 and 0.8 respectively.

However, the XGBoost model has high prediction scores for both functional and non-functional pump conditions but low scores for the functional-needs-repair condition. I attribute this to the low count of the functional-needs-repair condition, which makes up only 4.42% of the dataset.

### 4. ROC-AUC Analysis

![ROC_curves_for_machine_learning_models](https://github.com/leogachimu/Practice/assets/122081776/b62a6e53-6bc0-44f5-8688-c588a544aab6)

The XGBoost model is the best in terms of performance metrics and goodness of fit, and ROC curves show that it has the best combined AUC scores for the three classes of outcome.

### 5. Feature Importances

![Top_20_Most_Important_Features_in_Final_XGBoost_Model](https://github.com/leogachimu/Practice/assets/122081776/ef94553a-a1aa-443d-90f6-b433c164e928)

Some of the top features influencing a prediction include:<br>
i.) quantity-group (the quantity of water)<br>
ii.) The water point type<br>
iii.) The extraction type class<br>
iv.) The basin<br>
v.) scheme management<br>
vi.) The installer<br>
vii.) payment type<br>

## CONCLUSION
1. Waterpoints with zero static head have the highest density of non-functional pumps but I could not determine the reason for this fact.<br>
2. Pumps having total static head (tsh) above approx. 125,000 are all functional. This could be an indicator that the higher the tsh, the higher the likelihood of a pump lasting longer.<br>
3. Waterpoints located in areas with zero population have the highest density of non-functional pumps. However, there is no information about whether the wells have been abandoned or the population has relocated.<br>
4. The density of functional pumps is higher among the newest pumps while non-functional pumps are higher among the older pumps, from around **1965 to 1990.**<br>
5. From the geographical map of pumps, we observe the following:<br>
    a.) There is a higher density of functional pumps in the Northern regions of Mwanza and Shinyanga, as well as the Southern region of Njombe.<br>
    b.) There is a higher density of functional-needs-repair pumps in the Northern regions of Bukoba and Arusha, as well as the Western region of Kigoma.<br>
    c.) There is a higher density of non-functional pumps in the Central region of Dodoma and the South West region of Mtwara.<br>
6. Some classes of categorical variables are more frequent than others. For example, Iringa and Kilimanjaro regions have the highest number of pumps. The never-pay payment scheme is the most popular and over **40,000 out of 59,400 wells have soft water quality**.<br>
7. Functional pumps are the most frequent among almost all classes of predictor but a notable deviation from this trend is the **never-pay class** of the payment-type category, where non-functional pumps are more than the other classes of pumps.<br>
8. From the predictive section, I conclude that it's possible to correctly **predict at least 80% accuracy**, the condition of a pump given the data features from the Ministry of Water in Tanzania.<br>

The XGBoost model is the best for predicting whether a pump is functional, functional-needs-repair or non-functional given the different data features provided. It has an **accuracy score of 0.800 (80%)**, an **F1-score of 0.788**, a **precision of 0.797**, and a **recall of 0.800**. Even though the Random Forest model has slightly higher scores, the train scores show that it is overfitting the data while the XGBoost is a good fit (not underfitting or overfitting).

## RECOMMENDATIONS TO THE GOVERNMENT OF TANZANIA
1. I advise the Goverment of Tanzania to apply my final model in predicting the condition of well pumps across Tanzania. It will help them to correctly predict the actual condition of each pump at at least **80% success rate**.

2. The government needs to give more attention to the Northern regions of Bukoba and Arusha where there is the highest density of functional-needs-repair pumps, as well as the regions of Dodoma and Mtwara, where there is the highest density of non-functional pumps.

3. The government will need to find out more about why there are more non-functional pumps among the pumps recorded as having zero static head and in areas recorded as having zero population.

4. The government will need to implement and operationalize a payment scheme for the water points, having observed that the sites where people never pay for water had the highest frequency of non-functional pumps.

## STUDY LIMITATIONS
1. About half of the dataset has zero population, gps height, total static head, and construction year values and there is no information about why this is the case. This has only resulted in unresolved dilemmas. For example, wells with zero population have the highest frequency of non-functional pumps, but there is no information about whether the wells have been abandoned or the population has relocated. Therefore, I cannot accurately answer questions such as the relationship between population or construction year and a pump's functionality.

2. There is a high number of pumps with zero static head, the majority of which are non-functional. It is not possible to conclude whether the pumps are actually faulty or they are in good condition but the wells have run dry.

3. Tuning the Machine Learning models was computationally intensive and some of them took a couple of hours to execute. Therefore, I could not tune combinations of all possible parameters in due time.

4. The target classes were highly imbalanced and oversampling the minority class did not improve prediction scores.

## RECOMMENDATIONS FOR FUTURE RESEARCH AND MACHINE LEARNING MODELLING
1. Finding out more information about the high count of zero values in the population, GPS height, total static head, and construction year columns may lead to better analysis, prediction, and recommendations.

2. Finding out if there is more data that can balance the target classes. The current classes are imbalanced with the most frequent class comprising 37.2% of the data while the least class comprises only 4.42%. This affected the prediction score of the least class compared to the other classes. Availability of more data that can balance the classes would realize much better prediction scores.

3. The use of a more robust computer or cloud server would enable tuning to be done for all parameters of the different classifier models.

## FOR MORE INFORMATION
For further analysis and the highlights, kindly visit the following:
1. My Jupyter notebook file titled student.ipynb in this repository.
2. My presentation pdf in this repository. Kindly, if the pdf does not open the first time, please reload it and it will be rendered.
3. Alternatively, you can visit my presentation page at this link [https://arcg.is/9LDnb](https://storymaps.arcgis.com/stories/c47175e5d59247498a819c67d2508252/)

