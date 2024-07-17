> LI <-c(8,8,10,10,12,12,12,14,14,14,16,16,16,18,20,20,20,22,22,24,26,28,32,34,38,38,38)
> y <-c(0,0,0,0,0,0,0,0,0,0,0,0,0,1,1,1,0,1,0,0,1,1,0,1,1,1,0)
> summary(glm(y~LI,family =binomial))

Coefficients:
            Estimate Std. Error z value Pr(>|z|)   
(Intercept) -3.77714    1.37862  -2.740  0.00615 **
LI           0.14486    0.05934   2.441  0.01464 *
Null deviance: 34.372  on 26  degrees of freedom
Residual deviance: 26.073  on 25  degrees of freedom
> confint(glm(y~LI,family=binomial))
Waiting for profiling to be done...
                 2.5 %     97.5 %
(Intercept) -6.9951909 -1.4098443
LI           0.0425232  0.2846668

4.2
Refer to the previous exercise.Using information from Table 4.5：

a. Conduct a Wald test for the LI effect and construst a 95% Wald confidence interval for the odds ratuin corresponding to a 1-unit increase in LI.Interprt.

b.Conduct a likelihood-ratio test and construct a 95% profile likelihood interval.Interpret.