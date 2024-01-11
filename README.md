# Market-Return-Predictability
This following project aims to recreate Welch and Goyal's prediction of the equity premium in their paper "A Comprehensive Look at The Empirical Performance of Equity Premium Prediction". Data was sourced from Amit Goyal's website and includes monthly data from January 1950 until December 2022.

In order to predict the following months excess market return, data from the previous 10 years was used in a linear regression. The following variables were included in the linear regression:

- D/P
- Term Spread
- Default Spread
- Net Stock Issuance

The returns were then weighted using the following logic, where w(t) is the weight and m(t) is the predicted excess market return utilizing values from the previous 10 years:

w(t) = min{1.5, max{0.5, 100×m(t)}}

As a final result, the portfolio generated an average monthly excess return of 0.00598 and a monthly Sharpe Ratio of 0.14. This outperformed a 100% weighted market portfolio during this time period, which had an average monthly excess return of 0.00544 and a monthly Sharpe Ratio of 0.13. The higher Sharpe ratio of the portfolio that utilized return predictability weighting indicates that the higher excess returns were not due to additional risk. Overall, this strategy shows potential to be a useful alternative to 100% market weighting.
