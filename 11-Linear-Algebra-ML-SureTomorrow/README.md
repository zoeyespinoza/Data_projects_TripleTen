# Linear-Algebra-SureTomorrow
## Project Description

The Sure Tomorrow insurance company is exploring the potential of leveraging machine learning to address several crucial tasks and enhance its operations. As an evaluator, assess the feasibility and effectiveness of implementing machine learning solutions for the following tasks:

**Task 1:** Customer Segmentation for Targeted Marketing

- Objective: Identify customers who exhibit similarities to a given customer.
- Benefit: Empower company agents with the ability to conduct more effective and personalized marketing campaigns.

**Task 2:** Insurance Benefit Prediction

- Objective: Develop a prediction model to determine whether a new customer is likely to receive an insurance benefit.
- Challenge: Evaluate if the prediction model outperforms a baseline dummy model.

**Task 3:** Insurance Benefit Estimation

- Objective: Create a linear regression model to predict the expected number of insurance benefits a new customer is likely to receive.
- Outcome: Assess the accuracy and reliability of the regression model.

**Task 4:** Secure Data Transformation

- Objective: Develop a data transformation algorithm, such as data masking or data obfuscation, to safeguard clients' personal information while maintaining the quality and utility of machine learning models.
- Challenge: Prove the algorithm's effectiveness in protecting personal data without adversely affecting model quality.

This project aims to demonstrate the potential of machine learning in optimizing marketing, improving decision-making, and enhancing data security within the insurance industry. It involves a multifaceted approach, from customer profiling and predictive modeling to advanced data protection techniques, all aimed at ensuring the future of Sure Tomorrow Insurance is both data-driven and secure.
## Conclusions
In this project, we explored the significance of data scaling in the k-Nearest Neighbors (kNN) algorithm and found that scaling ensures that all features contribute uniformly to distance calculations. We applied the kNN classification algorithm to predict insurance benefits and experimented with various k-values to evaluate their impact on performance. The results demonstrated that kNN performance can be sensitive to the choice of k, and scaling plays a crucial role in this sensitivity.

We also introduced data obfuscation by multiplying numerical features with an invertible matrix P. The obfuscated data showed values that differ slightly from the original data due to the nature of matrix transformations. We successfully validated that the original data could be recovered from the obfuscated dataset using the knowledge of the invertible matrix P.

When it comes to linear regression, we observed that the obfuscation process did not affect the predicted values or the quality metrics, such as Root Mean Square Error (RMSE) and R-squared. This suggests that linear regression remains robust and consistent in the presence of data obfuscation using invertible matrices.

In conclusion, data scaling is crucial for kNN algorithms, and data obfuscation through invertible matrices does not impact the performance of linear regression.

## Appendix: Properties of Matrices
Matrices have many properties in Linear Algebra. A few of them are listed here which help with the analytical proof in this project.
<table>
<tr>
<td>Distributivity</td><td>$A(B+C)=AB+AC$</td>
</tr>
<tr>
<td>Non-commutativity</td><td>$AB \neq BA$</td>
</tr>
<tr>
<td>Associative property of multiplication</td><td>$(AB)C = A(BC)$</td>
</tr>
<tr>
<td>Multiplicative identity property</td><td>$IA = AI = A$</td>
</tr>
<tr>
<td></td><td>$A^{-1}A = AA^{-1} = I$
</td>
</tr>    
<tr>
<td></td><td>$(AB)^{-1} = B^{-1}A^{-1}$</td>
</tr>    
<tr>
<td>Reversivity of the transpose of a product of matrices,</td><td>$(AB)^T = B^TA^T$</td>
</tr>    
</table>
