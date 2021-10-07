# Stock-Analysis

## Overview
The purpose of this assignment was to create a vba macro that takes daily stock data and calculates annual trade volume as well as yearly returns for each stock. The project called for hard-coding the array in the subroutine. This works great for the given data set, but if the data is changed, the code will need to be updated. Therefore, I decided to create a for loop that would identify each unique ticker and build the array dynamically. This will allow it to work seamlessly if stocks are added or taken away.

## Macro Functionality

### Building an Array of Tickers Dynamically
Before looping through the stock data to collect total daily volumes and the yearly return for each ticker, this subroutine loops through the data to identify each unique ticker and adds it to an array, inceasing the array dimension with each new ticker. These means that the size of the array does not need to be defined, nor do the tickers need to be coded manually. This makes the program more user friendly. No code changes will need to be made if the combinations of tickers is different in years before or after 2017-2018. See the for loop here:

![For_Loop_Build_Array](https://user-images.githubusercontent.com/90878911/136427196-ba677a13-ade6-43a2-85ac-09fb0a010911.png)

### Gathering/Calculating Data for Total Daily Volumes and Yearly Returns
With the array from above, the program now loops through the data again to: A. find total daily volume of each ticker, B. identify the first close price and last close price of each ticker (used to calculate yearly returns), and c. populate said data on the analysis tab. I factored these two calculations (totaly daily volume and yearly returns) into one  for loop from the very beginning, so I did not need to refactor the code, nor do I have before and after run-times. The code I used is shown here:

![For_Loop_Stock_Data](https://user-images.githubusercontent.com/90878911/136428703-5d1dc1e8-2d79-4df4-9a30-42625fde7631.png)

## Results

           2017            |           2018
:-------------------------:|:-------------------------:
![](https://...Dark.png)  |  ![](https://...Ocean.png)
