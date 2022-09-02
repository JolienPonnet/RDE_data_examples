# RDE_data_examples
R-code accompanying the real data examples of the paper "Robust Inference and Modeling of Mean and Dispersion for Generalized Linear Models".

This directory contains two sub-directories: Data_Analysis and RobGLM.
- RobGLM contains two help functions that, together with the package RdeGlmLassoGam, are necessary to run the data examples in the Data_Analyse directory.
- Data_Analysis contains the analysis of 4 real data sets (as well as the data itself):
	- AdmittanceBerkely.R
	  This is an example on the double binomial model, using UCB admission data. We show the necessity of the RDE estimator, 
	  The classical non-robust estimators (CDE and CEQL) conclude that this data is overdispersed, whereas the RDE estimators (HRDE and TRDE) show that it is underdispersed.
	  The difference can be explained by an extremely high admission percentage for female students in department A (= outlier).
	  Moreover, a robust test shows that there is no significant difference between the admission rates for department A and B.
	  Finally, a Pearson residual plot is constructed.
	- epilepsyMolenbergh.R
	  The analysis of the data in 'epilepsy.sas7bdat' is an illustration of the double Poisson model. According to the non-robust estimators,
 	  the variable 'sex' is significant in the mean model, but a robust test based on the RDE estimator shows that only the variable 'base'
	  is significant. Moreover, a Pearson residual plot is constructed.
	  Finally, the adaptive lasso RDE estimator confirms the conclusion of the robust test (only the variable 'base' is sigificant in the mean model).
	- FishToxicology.R
	  This is another example on the double binomial model, using fish toxicology data. When we create two artificial outliers, 
	  we see that the classical non-robust estimators are heavily influenced, while the RDE estimators hardly change.
	- Example_ili_visits.R
  	  The analysis of the data in 'ili.visits.RData' is an illustration of the GAM RDE estimator.
	  A GLM for the mean model is clearly not flexible enough, whereas GAM RDE returns a good fit.
	  For the dispersion model, the classical RDE estimator gives already a good fit.  
	
