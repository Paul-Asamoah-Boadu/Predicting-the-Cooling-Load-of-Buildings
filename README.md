<h1>Predicting the Cooling Load of Buildings</h1>

<h2>Table of Content</h2>

<ul>
    <li><a href="#intro">Introduction</a></li>
    <li><a href="#data">Data Gathering</a></li>
    <li><a href="#explo">Data Exploration</a></li>
    <li><a href="#tools">Tools Used</a></li>
    <li><a href="#model">Model Building</a></li>
    <li><a href="#metrics">Evaluation Metrics</a></li>
    <li><a href="#selection">Model Selection</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
</ul>

<a id="intro"></a>
<h2>Introduction</h2>

The energy efficiency of buildings is becoming an increasingly important issue, both from an environmental and economic perspective. In this project, I focus on using machine learning to predict the cooling load requirements of buildings as a function of building parameters. Specifically, I aim to use eight building parameters to predict the cooling load. The dataset used for this project is obtained from the UCI Machine Learning repository and contains a total of 768 observations. The dataset is explored, preprocessed, and then used to train and evaluate various machine learning models. The primary objective of this project is to build a robust predictive model for cooling load requirements, which can aid in the design and development of energy-efficient buildings.

<a id="data"></a>
<h2>Data Gathering</h2>

The dataset was obtained from the UCI Machine learning repository [link](https://archive.ics.uci.edu/ml/datasets/energy+efficiency). The dataset includes 768 samples and 9 variables (8 features and 1 target variable). The target variable in this project is the cooling load of a building, and the eight features represent various building parameters. All variables are continuous, and there are no missing values in the dataset.


<center>
    
<table style="margin: 0 auto;">
   <thead>
      <tr>
          <th>Variable</th>
         <th>Attributes</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>X1</td>
         <td>Relative Compactness</td>
      </tr>
      <tr>
         <td>X2</td>
         <td>Surface Area</td>
      </tr>
      <tr>
         <td>X3</td>
         <td>Wall Area</td>
      </tr>
      <tr>
         <td>X4</td>
         <td>Roof Area</td>
      </tr>
      <tr>
         <td>X5</td>
         <td>Overall Height</td>
      </tr>
      <tr>
         <td>X6</td>
         <td>Orientation</td>
      </tr>
      <tr>
         <td>X7</td>
         <td>Glazing Area</td>
      </tr>
      <tr>
         <td>X8</td>
         <td>Glazing Area Distribution</td>
      </tr>
      <tr>
         <td>Y1</td>
         <td>Heating Load</td>
      </tr>
      <tr>
         <td>Y2</td>
         <td>Cooling Load</td>
      </tr>
   </tbody>
</table>
    
</center>

<a id="explo"></a>
<h2>Data Exploration</h2>

- <b>Boxplot</b>: I plotted boxplots for the three groups of independent variables, i.e. `Surface Area`, `Wall Area`, and `Roof Area`; `Overall Height`, `Orientation`, and `Glazing Area Distribution`; and `Glazing Area` and `Relative Compactness`.I also plotted a boxplot for the dependent variable `Cooling Load`. The boxplots show the distribution of the data for each variable and help to identify any potential outliers.

- <b>Correlation Heatmap</b>: I created a correlation heatmap to visualize the pairwise correlations between the features. I found that the `Relative Compactness`, `Surface Area`, `Wall Area`, `Roof Area`, and `Overall Height` have strong negative correlations with the Cooling Load. `Glazing Area` has a strong positive correlation with the Cooling Load, while `Orientation` and `Glazing Area Distribution` have weak correlations with Cooling Load.

- <b>Pairplot</b>: I created a pairplot to visualize the relationships between all pairs of features. This also helps to identify any potential outliers and identify any possible nonlinear relationships between the variables.

<a id="tools"></a>
<h2>Tools Used</h2>

The project was done on the __Jupyter Notebook__ environment, and the required packages and libraries to run this project include:

- NumPy
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib.pyplot
- Seaborn

<a id="model"></a>
<h2>Model Building</h2>

The data was splited into training and testing sets. Where the training set represents 70% and the testing set represents 30% of the dataset.   
Train and evaluate the performance of nine different machine learning models:

1. Linear Regression
2. XG Boost Gegressor
3. Gradient Boosting Regressor
4. Random Forest Regressor
5. Lasso
6. Decision Tree Regressor
7. Ridge
8. AdaBoost Regressor
9. Bagging Regressor

These models were chosen because they are commonly used in regression problems and have proven to be effective in previous studies. All models were trained using the 70/30 train-test split of the data. The models were optimized using the mean squared error (MSE) and R-squared (R2) score as evaluation metrics.

<a id="metrics"></a>
<h2>Evaluation Metrics</h2>

The models are evaluated using the following metrics:

- Root Mean Squared Error <code>RMSE</code>
- R-squared <code>R2</code>

<a id="selection"></a>
<h2>Model Selection</h2>

Out of the 9 models, the best-performing models were optimized by using <b>Grid Search Cross-Validation</b>. Five different models were selected, and the performance of each model was visualized using a custom function `model_perf_visual()` that compares the actual and predicted values. The five models used were:

 <h3>Gradient Boosting Regressor</h3>
<img src="Gradient Boosting.png" alt="Visualization of test and train of Gradient Boosting Regressor">  

 <h3>Random Forest Regressor</h3>
 <img src="Random Forest.png" alt="Visualization of test and train of Random Forest Regressor">
 
 <h3>XG Boost Regressor</h3>
 <img src="XG Boosting.png" alt="Visualization of test and train of XG Booting Regressor">
 
 <h3>Bagging Regressor</h3>
 <img src="Bagging.png" alt="Visualization of test and train of Bagging Regressor">
 
 <h3>AdaBoost Regressor</h3>
<img src="AdaBoost.png" alt="Visualization of test and train of AdaBoost Regressor">

<a id="conclusion"></a>
<h2>Conclusion</h2>

In conclusion, I explored using machine learning to assess the cooling load requirements of buildings. From the results, it is clear that the ensemble methods such as `Random Forest Regressor`, `AdaBoost Regressor`, and `Gradient Boosting Regressor` models performed better than the other models. The `Gradient Boosting Regressor` model has the best performance with a __RMSE score of 0.80__ and __R2 score of 0.99__. This makes the `Gradient Boosting Regressor` the best model for predicting the cooling load of buildings using the energy efficiency dataset from UCI Machine Learning repository.
