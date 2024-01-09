# Numerical-Methods-Model-Training

## Developing Vintage Value's Advanced Car Valuation App: Harnessing Historical Data to Drive Accurate and Swift Market Price Predictions for Used Cars

Vintage Value used car sales service is developing an app to attract new customers. In that app, you can quickly find out the market value of your car. You have access to historical data: technical specifications, trim versions, and prices. You need to build the model to determine the value. 

Vintage Value is interested in:

- the quality of the prediction;
- the speed of the prediction;
- the time required for training

### Dataset
The historical data made available for this project is comprehensive. It provides insights into various car attributes, from basic specifications to trim versions, and the prices at which these cars were sold. Leveraging this data effectively is the key to building a robust price prediction model.
  
<h2>Model Performance:</h2>

<table>
  <tr>
    <th>Model</th>
    <th>RMSE</th>
    <th>Comment</th>
  </tr>
  <tr>
    <td>Linear Regression</td>
    <td>3132.14</td>
    <td>Baseline model for comparison</td>
  </tr>
  <tr>
    <td>Random Forest</td>
    <td>2185.05</td>
    <td>Outperformed the baseline model</td>
  </tr>
  <tr>
    <td>XGBoost</td>
    <td>1990.95</td>
    <td> Second lowest RMSE </td>
  </tr>
  <tr>
    <td>LightGBM</td>
    <td>1635.81</td>
    <td>Best performing with the lowest RMSE</td>
  </tr>
</table>

<div class="alert">
  <b>Evaluation:</b><br>
 The progression from the baseline Linear Regression model to the more advanced models. LightGBM has shown to be the most effective in reducing the RMSE in this scenario. It might be useful to consider parameter tuning or feature engineering further to see if the performance can be enhanced even more.
</div>

</body>
</html>
**Linear Regression** had the fastest training time. Given its simplicity and the fact that it doesn't require iterative processes like tree-based models, it typically trains very quickly.

**LightGBM** had a relatively quick training time, especially given that we trained it on a subset of the data. Gradient boosting models, by nature, can take longer due to their iterative approach to building trees. However, LightGBM is optimized for speed and can handle larger datasets more efficiently than traditional gradient boosting.

**XGBoost** although we encountered computational constraints that prevented a full evaluation within this environment, generally has a longer training time than LightGBM, especially on larger datasets. Its performance can be comparable or sometimes better, but it might come at the cost of increased training time.
