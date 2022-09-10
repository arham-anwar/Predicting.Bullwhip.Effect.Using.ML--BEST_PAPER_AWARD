# Mitigating_the_bullwhip_effect_using_ML

###

CONTENTS

# Table of contents
1. [What is the bullwhip effect?] (#Sec1)
2. [Quantifying Bullwhip Effect] (#sec2) 
3. [Creating the dataset] (#sec3) 
4. [Selecting the ML algorithm] (#sec4) 
5. [Results] (#sec5) 
6. [Findings] (#sec6) 
6. [Best Paper Award] (#sec7) 


## What is the bullwhip effect? <a name="Sec1"></a>
The bullwhip effect is a distribution channel phenomenon in which demand forecasts yield supply chain inefficiencies. 
It refers to increasing swings in inventory in response to shifts in consumer demand as one moves further up the supply chain.
The bullwhip effect is caused by: 
-Demand forecast updating: Members of the supply chain updating their demand forecasting
-Order batching: Members of the supply chain rounding up or down the quantity of orders
-Price fluctuations: Usually driven by discounting resulting in larger quantities of purchases
-Rationing and gaming: Buyers and sellers delivering over or under their order quantities

![image](https://user-images.githubusercontent.com/64707681/189498685-e1707058-67e7-4588-ad3d-1a07987f4088.png)

## Quantifying Bullwhip Effect <a name="sec2"></a>
-Operational research formulates the problem as a differential equation. The mathematical solution attempts to minimize a cost function subject to operation conditions. In many cases, the ratio between orders variance and demand variance is employed.
![image](https://user-images.githubusercontent.com/64707681/189498759-4ce95a46-48f8-4c51-b0ad-6bcf80878560.png)
-It describes the existing ratio between variance and the arithmetic mean. A ratio higher than one indicates variance amplification, and below one implies an isolation effect. 


## Creating the dataset <a name="sec3"></a>
The data is generated using the bullwhip game. This section shows plots of demand of customer in  supply chain. To implement variability in the demand, the customer demand is simulated using a sinusoidal curve as shown in the figure below.
Consequently, The following graphs for demand for the following are obtained and displayed below :
![image](https://user-images.githubusercontent.com/64707681/189498825-51e8a243-b605-4bc5-aa18-72ec2a2d96cd.png)

## Selecting the ML Algorithms <a name="sec4"></a>
The following algorithms were chosen:
-KNN
-Multi Layer Perceptron Regressor
-Decision Tree

The split between training and testing data is 75% and 25%
The proposed machine learning model has nine inputs namely Cost, Order, OUT, SS, LTD, NS, Forecast, Receive and Demand. Bullwhip will be the forecasted output of the model. The computed output, is the numerical value of the bullwhip effect.


## Results <a name="sec5"></a>
-A correlation Matrix was constructed to understand the correlation between bullwhip and the various inputs. 

![image](https://user-images.githubusercontent.com/64707681/189498866-8730667c-d2bf-4bb2-a544-0354f0db5f34.png)
![image](https://user-images.githubusercontent.com/64707681/189498877-4e5e67ab-d26a-4e27-a4f7-c8ef0802367d.png)

-Accuracy of MLP: The given dataset had a small resolution of upto 2 decimal places. Due to this small resolution, the algorithm is unable to differentiate and predict the bullwhip effect with a high degree of accuracy.
-Accuracy of KNN: Since the projection of the 9 input variables were plotted against the numerical value of bullwhip. The machine found the most accurate result at K=5 or 5 clusters.  The algorithm dealt with multi collinearity easily
-Accuracy of Decision Tree: Due to high multi-collinearity between the input data points. The Regressors failed to model the bullwhip. Certain variables need to be removed to get a higher prediction score. 

## Findings <a name="sec6"></a>
-The objective was to study the bullwhip effect, underlying causes and
possible remedies of the bullwhip effect in supply chains. Coordination and collaboration among partners of a supply chain with time bound information sharing is a possible remedy to the demand amplification phenomenon. However, the full integration of the organizations of a supply chain is not possible due to difference of strategies and goals existing among them. 
-In absence of integration among partners the increase in accuracy of demand information will help to reduce the bullwhip effect. Hence, the appropriateness and effectiveness of bullwhip forecasting using artificial intelligence technique, artificial neural networks is a valid and practical approach to mitigate the inefficiencies due to the amplification in variance of demands. 
-The results of this project show that the artificial intelligence technique, artificial neural network forecasts accuracy can be achieved with further investigation into the phenomenon. Future research could be directed towards applications of other artificial intelligence techniques like genetic algorithms and fuzzy logic in Bullwhip forecasting.

### BEST PAPER AWARD <a name="sec7"></a>
![image](https://user-images.githubusercontent.com/64707681/189498952-53a0c66d-4d99-4550-9964-1be0bdc07986.png)
