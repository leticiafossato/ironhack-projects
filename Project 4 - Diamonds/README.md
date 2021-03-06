<p align="center"><a href="https://imgbb.com/"><img src="https://i.ibb.co/s5zqxjj/DIAMOND3.png" alt="DIAMOND3" border="0"></a><br /><a target='_blank' href='https://pt-br.imgbb.com/'></a></p>
<h1 align="center">📈 Project 04 | Linear Regression </h1>

## Project Status
:heavy_check_mark: Complete

## Table of Contents 
- [Objective](#objective)
- [Resources](#Resources)
- [Process](#Process)
- [Results](#Results)
- [Learning Process](#Learning-Process)
- [Authors](#Authors)

## Objective
The objective of this project is to create a model to predict prices of diamonds, practicing linear regression.<br>
To acess complete objective informations click <a href="https://drive.google.com/file/d/1SR_lkpSamfoPeFckpfvM4PskhPhkzA3l/view?usp=sharing">here</a>.

### Problem Statement
> The price predicted needs to have a root mean squared error lower than 900 dollars.

## Resources
Datasets was provided by IronHack. <br>
00-diamonds.csv<br>
00-rick_diamonds.csv<br>

## Process
- Import the dataframe;
- Create a first baseline predicting the price by the mean;
- Start to Explore and Clean the Data:
     - Check null values;
     - Search for outliers - comparing mean and median;
     - Calculate values to correct x,y and z;
     - Check correlations.
- Apply the linear regression to predict the prices of diamonds;
- Improve the model until RMSE (root mean squared error) < 900.

## Results
After a lot of attempts, we obtained:

<a href="https://ibb.co/SBP2gFW"><img src="https://i.ibb.co/yqXDCHG/resultado-reg-lin.jpg" alt="resultado-reg-lin" border="0"></a><br /><a target='_blank' href='https://pt-br.imgbb.com/'></a>
 ### Image summary:
|    R²   |  RMSE  |
|  -----  | -------|
| 95.38%  |    853 |
     
## Learning Process

### Theory Applied
- [x] Numpy
- [x] Pandas
- [x] MatplotLib and Seaborn
- [x] Linear Regression

### Challenges
- Apply the model for two non-linear variables;
- Decrease the RMSE for the amount requested.

 ### Improvements
 - Use target encoder on categorical variables;
 
## Authors
Letícia Fossato <br>
[Gabriela Nakasato](https://github.com/gabrielanakasato)
