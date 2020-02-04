# Lasso_Ridge_ElasticNet_Model_R

## Lasso Regrssion: 
    
    This will eliminate many features, and reduce overfitting in linear model. 
    (This model is well suited for variable selection/parameter elimination.)
## Ridge Regression:
This will reduce the impact of features that are not important in predicting your y values. Dataset has multicollinearity (correlations between predictor variables).
## Elastic Net Regression:
This combines feature elimination from Lasso and feature coefficient reduction from the Ridge model to improve your model's predictions (like Multicollinearity)
Ridge regression belongs a class of regression tools that use L2 regularization. The other type of regularization, L1 regularization, limits the size of the coefficients by adding an L1 penalty equal to the absolute value of the magnitude of coefficients. 

Y= mX+b
Y = Dependent Variable (Target Variable)
X= Independent Variable (Predictor Variable)
m= slope 
b =intercept

Target Variable "TotalRevenueGenerated"

R conversion
Model.matrix
numeric_Variables

fit1=glmnet(train,y,alpha=1)  #LASSO
fit2=glmnet(train,y,alpha=0)  #Ridge
fit2=glmnet(train,y,alpha=0.5)  #ElasticNet


 	             mae	   mse	    rmse	       mape
LASSOtrain	31.24457	1864.676	43.18189	0.188977
LASSOtest	31.46629	1941.09	44.0578	0.187351
RIDGEtrain	31.2463	1864.622	43.18127	0.189043
RIDGEtest	31.48535	1944.837	44.1003	0.187471
Elastictrain	31.24521	1864.636	43.18144	0.189008
Elastictest	31.47587	1942.972	44.07916	0.187411
