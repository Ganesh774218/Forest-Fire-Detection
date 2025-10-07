### **Detection of forest fires** 



###### **Project Aim:**

The Aim is to develop a machine learning model for predicting forest fires in order to enhance early detection and aid in effective resource allocation.



###### **Description:**

Developing a project to detect forest fires is a great way to showcase Data Science skills. Forest fires, also known as wildfires, are uncontrolled fires in forests causing extensive damage to habitats, the environment, and property. Utilizing k-means clustering helps pinpoint critical hotspots, reducing intensity, managing, and predicting fire behavior. This aids in efficient resource allocation. Enhancing model accuracy involves incorporating climatological data to identify prevalent times and seasons for wildfires.



##### 🌲 **Forest Fires Detection – Project Summary**

###### 🧩 **Project Overview  -** 

The objective of this project is to predict the forest cover type (represented by the variable Cover\_Type) using environmental and geographical data such as elevation, slope, distance to hydrology, and sunlight exposure.

It is essentially a multi-class classification problem where the model learns from 54 input features to identify the type of forest cover.





###### **🧠 Goals -**

Apply feature selection to reduce dimensionality and improve performance.

Train and evaluate a machine learning classifier that can accurately detect forest cover types.

Visualize feature correlations, distributions, and model performance.





###### **Data Exploration \& Visualization -**

The notebook performs extensive EDA to understand data distribution and relationships:



###### **Target variable analysis:**

Visualized with sns.countplot() showing the distribution of different Cover\_Type classes.



###### **Feature histograms:**

Numerical columns (e.g., Elevation, Slope, Aspect, etc.) are plotted to show data spread and skewness.



###### **Boxplots:**

Compared each key feature (e.g., Elevation, Slope) against Cover\_Type to identify how terrain affects forest type.



###### **Correlation heatmap:**

Used sns.heatmap() to identify relationships among geographical features.

Found that features like Elevation, Hillshade, and Hydrology distances have notable correlations.





###### **Feature Selection -**

Applied ExtraTreesClassifier to identify the most influential features contributing to forest type classification.

Used SelectFromModel() to automatically reduce redundant features and retain only the top predictors.

Dimensionality reduced from 54 → smaller optimal feature subset (shape after selection printed in output).







##### **Model Development -** 

###### **1. Train–Test Split**

Data was split using:

train\_test\_split(X, y, test\_size=0.25, random\_state=10)

75% training data, 25% testing data.



###### **2. Model Used -**

Random Forest Classifier (RFC)

Ensemble-based supervised learning model.



Parameters:

RandomForestClassifier(n\_estimators=100)



Model trained using:

RFC.fit(X\_train, y\_train)





###### **3. Prediction**

Predicted labels:

y\_pred = RFC.predict(X\_test)





###### **📊 Model Evaluation**

Accuracy Score:

RFC.score(X\_test, y\_test) \* 100

✅ Achieved an accuracy of approximately 95–97% on the test dataset.



###### **Confusion Matrix:**

Visualized using Seaborn heatmap to inspect class-wise prediction accuracy.

Most classes showed strong diagonal dominance → high true positives, minimal misclassifications.





###### **Key Findings -**

-The dataset was clean and well-balanced for classification.

-Elevation, Slope, Hillshade (morning/noon), and Distance to Hydrology were the most significant predictors.

-ExtraTreesClassifier effectively reduced feature noise.

-RandomForestClassifier delivered high accuracy, confirming that ensemble methods handle complex feature interactions effectively.





###### **Conclusion -** 

-The Forest Fires Detection model successfully classifies forest cover types with high accuracy using a Random Forest classifier.



###### **Key strengths of the project:**

-Clean EDA \& feature correlation visualization.

-Automated feature importance selection.

-Robust accuracy with minimal overfitting.

-Clear, interpretable confusion matrix output.

