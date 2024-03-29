---
layout: page
title: Code
permalink: /Code/
---


## [DFM Nowcaster](https://github.com/genekindberg/DFM-Nowcaster)


A nowcasting dynamic factor model estimated using Bayesian methods, implemented in Python. As far as I know this is the only code available to implement a Bayesian version of a nowcasting DFM (most people use the EM algorithm made available from Giannone, Reichlin and Small 2008). The model can accommodate multiple factors, a choice of lags in the observation and transition equations, and can include an MA term in the errors in the observation equation. Also provides quasi out-of-sample mean squared errors to assess nowcasting performance. Roughly based on my work in [Gauging the Globe: The Bank's Approach to Nowcasting World GDP](https://www.bankofengland.co.uk/quarterly-bulletin/2018/2018-q3/gauging-the-globe-the-banks-approach-to-nowcasting-world-gdp).

## [SVAR Toolbox](https://github.com/genekindberg/SVAR_tools)
A matlab toolbox for running BVARs with long-run restrictions, the Max Share approach, and a standard Cholesky identification. In addition, sign restrictions, zero restrictions and forecast error variance magnitude restrictions have now been added. The latter set of identifications can be imposed in tandem (i.e. sign and zero restrictions can be imposed simultaneously). Spectral and Limited Spectral identifications will be added in due course. The toolbox also produces, IRFs, FEVD, historical decompositions, and structural shocks. It can be easily modified to add new identifications. 

## [MIDAS Nowcaster](https://github.com/genekindberg/MIDAS_Nowcaster)
A tool to nowcast quarterly data with monthly indicators: US consumption example. Pulls data directly from FRED from a list of codes - any target quarterly variable or monthly high frequency indicator can be used. Also works with Haver if available. Calculates the optimal lag length to minimize out-of-sample root mean squared error (RMSE) for each indicator and whether the specification improves with an AR term included. Changes the specification for the optimal lag length in each month of the quarter. Optimally combines the predicted nowcast using either the mean squared error or the root mean squared error to weight together each indicator. Displays the nowcast for each indicator and the optimally combined set of indicators. Displays the RMSE of each indicator and the RMSE of the optimally-combined nowcast. This allows the user to apply judgement if they believe a particular indicator is giving a poor steer in that quarter. Currently set up to nowcast US consumption using monthly PCE data, non-farm payrolls, and real retail sales. Other indicators or a different target variable (such as GDP) can be easily switched by changing the FRED code.