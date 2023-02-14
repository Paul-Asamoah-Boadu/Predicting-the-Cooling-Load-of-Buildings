<h1>Predicting the Cooling Load of Buildings</h1>

<h2>Table of Content</h2>

<ul>
    <li><a href="#intro">Introduction</a></li>
    <li><a href="#data">Data Gathering</a></li>
    <li><a href="#explo">Data Exploration</a></li>
    <li><a href="#tools">Tools Used</a></li>
    <li><a href="#model">Model Building</a></li>
    <li><a href="#selection">Model Selection</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
</ul>

<a id="into"></a>
<h2>Introduction</h2>

The energy efficiency of buildings is becoming an increasingly important issue, both from an environmental and economic perspective. In this project, we focus on using machine learning to predict the cooling load requirements of buildings as a function of building parameters. Specifically, we aim to use eight building parameters to predict the cooling load. The dataset used for this project is obtained from the UCI Machine Learning repository and contains a total of 768 observations. The dataset is explored, preprocessed, and then used to train and evaluate various machine learning models. The primary objective of this project is to build a robust predictive model for cooling load requirements, which can aid in the design and development of energy-efficient buildings.

<a id="data"></a>
<h2>Data Gathering</h2>

The dataset was obtained from the UCI Machine learning repository [link](https://archive.ics.uci.edu/ml/datasets/energy+efficiency). The dataset contains eight attributes (or features, denoted by X1...X8) and two responses (or outcomes, denoted by Y1 and Y2). The aim is to use the eight features to predict the response Cooling Load(Y2). Specifically:

<table>
   <thead>
      <tr>
          <th><b>Variable</b></th>
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
