**Project is not ready, avoid opening issues**

# ML-IDS

Applying machine learning principles to the information security field through intelligent intrusion detection systems.

This is a three phases project that can roughly described as

- Dataset
- Model Developement
- Advesarial Machine Learning

## Dataset

* **General Dataset Information**
  * Used the CSE-CIC 2018 which was made by using CIC-FlowMeter V2 which tracked the features of IP packets throughout the day while there was generic and malicous traffic flow
  * 81 Features were tracked total
  * 10 different days, with one attack per day
  * Seven different attacks: DDoS, Brute Force, SQL Injection, DoS, Botnet (Bot), Infiltration
  * Total of 16 million+ rows when merging all days into one big dataset
* **Preprocessing**
  * Cut down data from 81 to 31 features because of irrelevance of some features, inability to preprocess, and because those features did not affect the accuracy of the models
    * Utilized research of features and heatmap to determine which features were important
  * Merged all days into one big dataset and ran models based off that
  * Standarized all rows to ensure no outliers could affect the results and because each features had different statistical ranges which could potentially affect model results

## Model Development

* Used four models
  * Logistic Regression
  * Random Forest
  * Support Vector Machines
  * Neural Network (Multi-Layer Perceptron)
* Results
  * Logistic Regression
    * Results
  * Random Forest
    * Results
  * Support Vector Machines
    * Results
  * Neural Network
  * Results
* Achieved around ~99% accuracy on models, which matched studies out in real world

## Advesarial Machine Learning Implementation

* Advesarial machine learning is where you take the input data and slightly tweak it to test the robustness of the model
* Impleneted by adjusting all the attack data
* Dataset Adjustments
  * Pulled out all attack data
  * Determined that only 11 of the 31 features could be changed
    * Researched which features could be adjusted
  * Randomly adjusted 3 of the 11 features on each row
  * Each feature was adjusted by a random percent between 1 and 5 (inclusive)
    * Also changed features that were related to the original feature
    * Determined which features were interconnected to the feature and also changee those from a random percent between 1 and 5 (inclusive)
    * Determined the interconnections through research and heatmap analysis
  * Repeated the last two steps five times for each row
  * Turned 2.7 million attack rows into 13.75 million augemented attack rows
* Results

## References

All consulted papers & documentation is available in the "papers" folder.
