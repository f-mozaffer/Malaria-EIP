# Malaria-EIP
The rate of malaria parasite transmission and intensity of infection is strongly determined by the extrinsic incubation period (EIP: also known as the duration of sporogony), the inverse of parasite development rate. The extrinsic incubation period is highly sensitive to temperature. The thermodynamic model proposed by Briére et al is supposed to provide a nonlinear relationship between temperature and parasite development.

PDR (T) = c * T * (T – Tmin) * √ (Tmax – T)

Parameter estimation using STAN

The above thermodynamic model has three unknown parameters namely

Maximum temperature (Tmax)
Minimum temperature (Tmin)
Scaling parameter (c)
To estimate these unknown parameter values we have used STAN (https://mc-stan.org/), a platform for statistical modelling and high-performance statistical computation. STAN performs Bayesian statistical inference with Markov Chain Monte Carlo (MCMC) sampling.

One can estimate unknown parameter for all the malaria parasites listed in the paper by using data for parasite development rate against temperature and prior values provided in the paper.

Pystan2 is being used to simulate the code.

EIP calculation using mean temperature

Temperature for all the four site is available at an hour interval. Mean daily temperature is calculated for each day. Using mean daily temperature one has to calculate EIP using thermodynamic model due to Briére equation for each day. Take mean of per day EIP values to get EIP per month.

The code provided here is for the Anusuya (2000 m) for the month of May. One can simulate the code for other site and malaria parasite as well as for other months of the year as mentioned in the main text by using temperature data and Briére equation for the respective site and malaria parasites.
