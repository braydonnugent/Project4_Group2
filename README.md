### Overview and Purpose 
The aim of this investigation is to implement machine learning on a dataset orientated on heart disease & see how possible it is to predict the presence or absence of heart disease.

As well as Age, Sex & Patient ID's, the fields within this dataset include:
  Chest pain type: selection of 4 forms of chest pain.
  BP (Blood Pressure)
  Cholesterol.
  FBS over 120- fasting blood sugar > 120 mg/dl
  EKG results: electrocardiographic results 0: normal -- Value 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV)
  -- Value 2: showing probable or definite left ventricular hypertrophy by Estes' criteria
  Max HR (Heart Rate)
  Exercise Angina: 1 = yes; 0 = no (Chest pain when you exercise)
  ST Depression: ST depression induced by exercise relative to rest
  Slope of ST: difference between ECG highest elevation & lowest depression
  Number of vessels fluro:
  Thallium: 0 = normal; 1 = fixed defect; 2 = reversable defect
  
  Heart Disease: used to train the data

Utilising the fields that would be considered valuable information (based on visualisations created on Tableau) for the process of machine learning, they will be used to predict the outcome of heart disease as accurately as possible.

### Data Analysis
Link to Tableau: https://public.tableau.com/app/profile/braydon.nugent/viz/Project4_Group2_Explatory_Visualisations/ExplatoryAnalysis?publish=yes
![image](https://github.com/braydonnugent/Project4_Group2/assets/142481554/292e90b7-881b-41ad-a626-03b810eb1fda)


### Building ML Models 
Using previous examples of machine learning models learned throughout the course, four different ML models were created: decision tree, KNN model, Random forest and Neural Network Model.
For every model preprocessing was conducted on the data to convert the outcome varibale (presence of heart disease) into a binary variable. The patient ID column was also dropped before scaling the dataset, splitting into training and testing sets and then creating the models. 

### Optimising Neural  Network Model 
We set out to make our neural network super accurate by combining insights from Random Forest analysis and Tableau visualizations to figure out the best data columns to test.

First, we prepped our dataset, making sure all the data in our columns were integers and cutting out any unnecessary ones. Then, we tweaked the setup of our neural network, adjusting the hidden node layers to use "relu" and the outer layer to use "sigmoid".

To make sure our model was performing at its best, we ran it through a bunch of tests. We kept an eye on metrics like accuracy and loss, using "binary crossentropy" to measure loss. We used the "adam" optimizer to help train the model, and we played around with the number of epochs to fine-tune its performance.

This whole process was all about finding the sweet spot for our neural network, making sure it was as accurate as possible by tinkering with different settings and configurations.
![image](https://github.com/braydonnugent/Project4_Group2/assets/142481554/07e0e2dc-a22e-46dd-bc39-aed377910040)


### Discussion 
In Summary, despite the limited entries within the dataset, it’s possible to implement machine learning to predict the status of heart disease with a high performing accuracy such as 88%
Among the multiple attempts made to create the machine learning model with the best performing accuracy, we followed what was suggested by the hypothesis, which was to include the four most significant fields based on the Tableau visualisations. (3 of those 4 were further supported as the most significant fields through the chart produced on the random forest tree).
Despite this method producing an admirable accuracy of 83%, the highest performing model of 88% came from filtering out the 3 fields providing the least significance to the machine learning (the noise), based on the chart from the random forest.

Ultimately, contrast to what was stated in the hypothesis, it is necessary to provide the machine learning model with as much information as necessary, even if there appears to be no significant correlation in the data.


### what is the challenge and how your group overcome it? What is the limitation of the data/model? 
The challenge was having deep understanding on the dataset information. Initial research was conducted to properly understand the variable columns present within the dataset, and how they are related to the prescence of heart disease within the patient. Tableau visualizations as well as creating a random forest features graph also helped in overcoming the differences in understanding.

The main limitation was the sample size of the dataset. Records of around 270 patients were present within the dataset. If the numer of records were increased, the corresponding machine learning model could have the potential to be better optimised and have a higher overall accuracy.
Other limitations such as time constrained the number of attempts the model could be optimized. Around ten different optimising attempts were achieved with the neural network model over the past two weeks. More varied attemtps could have been achieved if this time limitation was extended.
