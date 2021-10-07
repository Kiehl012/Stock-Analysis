# Stock-Analysis

## Overview
The purpose of this assignment was to create a vba macro that takes daily stock data and calculates annual trade volume as well as yearly returns for each stock. The project called for hard-coding the array in the subroutine. This works great for the given data set, but if the data is changed, the code will need to be updated. Therefore, I decided to create a for loop that would identify each unique ticker and build the array dynamically. This will allow it to work seamlessly if stocks are added or taken away.

## Macro Functionality

### Building an Array of Tickers Dynamically
Before looping through the stock data to collect total daily volumes and the yearly return for each ticker, this subroutine loops through the data to identify each unique ticker and adds it to an array, inceasing the array dimension with each new ticker. These means that the size of the array does not need to be defined, nor do the tickers need to be coded manually. This makes the program more user friendly. No code changes will need to be made if the combinations of tickers is different in years before or after 207-2018. See the for loop here:

### Gathering/Calculating Data for Total Daily Volumes and Yearly Returns
