# Stock-Analysis

## Overview
The purpose of this assignment was to create a VBA macro that takes daily stock data and calculates annual trade volume as well as yearly returns for each stock. The project called for hard-coding the array in the subroutine, but while that works great for the given data set, it will not run properly if the data is changed. Therefore, I created a for loop that would identify each unique ticker and build the array dynamically. This allows the program to identify and work with any number, or combination, of tickers.

## Macro Functionality

### Building an Array of Tickers Dynamically
Before looping through the stock data to collect total daily volumes and the yearly return for each ticker, this subroutine loops through the data to identify each unique ticker and adds it to an array, increasing the size of the array with each new ticker. These means that the size of the array does not need to be defined ahead of time, nor do the tickers need to be assigned to indexes manually. This makes the program more user-friendly because there's no need to update the code if the tickers change. See the code block here:

![For_Loop_Build_Array](https://user-images.githubusercontent.com/90878911/136427196-ba677a13-ade6-43a2-85ac-09fb0a010911.png)

### Gathering/Calculating Data for Total Daily Volumes and Yearly Returns
With the array from above, the program now loops through the data again to: 1. find total daily volume of each ticker, 2. identify the first close price and last close price of each ticker (used to calculate yearly returns), and 3. populate said data on the analysis tab. I factored these two calculations (total daily volume and yearly returns) into one for loop from the very beginning, so I did not need to refactor the code, nor do I have before and after run-times. The code I used is shown here:

![For_Loop_Stock_Data](https://user-images.githubusercontent.com/90878911/136428703-5d1dc1e8-2d79-4df4-9a30-42625fde7631.png)

## Results

               2017                      2018
![Stocks_2017](https://user-images.githubusercontent.com/90878911/136429492-b5ad8916-d187-4e27-a525-b906c0eb5c9b.png)   ![Stocks_2018](https://user-images.githubusercontent.com/90878911/136429496-bfb75d76-9774-4784-8faf-07def561b91c.png)

At a glance, it's clear that this particular group of stocks performed much better in 2017 than in 2018. While this is useful information, there are other factors that play into a stock's performance other than past data, so I would reccomend this be used as a tool to supplement a broader analysis. I'd also reccommend looking at more than just 2 years of data, especially when choosing long-term investments. 

## Summary

### Advantages and Disadvantages of Refactoring Code
Refactoring code is good for a number of reasons. First, it makes the code simpler to read and understand. This is especially important if the program is going to be passed off or maintained by someone other than the original author(s). Secondly, it can improve performance, reducing the time it takes to run and the memory it uses. However, refactoring takes time and money. While refactoring is generally a good practice, it should be approached thoughtfully. For example, if a program or script is only going to be used a couple of times, it might not make sense to spend hours refactoring just to shave a minute off the run-time or clean up the code. Using this project as an example, suppose the user is never going to use data sets larger than ~3,000 rows by ~10 columns. In that case, they probably won't notice or care if the program runs in 0.6 seconds vs 1.06 seconds. So, it's important to do a cost-benefit analysis before refactoring.

### Advantages and Disadvantages of Building an Array Dynamically
As I explained above, I did not have to refactor my code, so I'll to use this section to analyze the benefits of using a for loop to build an array vs. hard-coding the array like the project called for. The biggest advantage of building the array dynamically, is the added flexibility. Yes, there are 12 stocks in the data sets provided, but perhaps that won't always be the case. Maybe Steve decides that he wants to look at a different set of stocks in 2019. With this program, he will be able to do that. Had I hard-coded the array, the code would need to be altered to accommodate the new data set. However, building the array with a for loop required a second loop, which means the program has to run through 3,000+ rows one additional time. This slows down the program and could become an issue with larger data sets. Most importantly, I dont know for certain that building a dynamic array was necessary. If Steve is never going to look at any other stocks, it would have actually been more efficient to hard-code each ticker into the array.
