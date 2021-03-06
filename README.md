<h1>VBA of Wall Street</h1>

<h2>Overview of Project</h2>

<h3>Background</h3>

  <p>
  A friend, Steve, has reached out for some assistance analyzing data on "Green Stocks" for his parents.  His parents have not done much research, but decided to invest in DAQO Stock.  To ensure this is a smart choice, Steve has compiled a list of data on various "Green Stocks" and requested assitance analyzing daily volumes and returns on each. After sending an initial analysis to Steve on the sample he submitted, he noted that the code worked well for 12 stocks, but would be too slow for thousands should he analyse a larger data set.
  </p>

<h3>Purpose</h3>

  <p>
  The purpose of this project is to determine whether or not DAQO is a good investment by:
    <ol>
      <li>Refactoring existing code to increase performance, making it more practical, at scale, for larger analyses than the original 12 stocks</li>
      <li>Looking at the Total Daily Volume and Returns for DQ for 2017 and 2018</li>
      <li>Looking at and comparing the Total Daily Volume and Returns for the 11 other stocks Steve has compiled data for against DQ for 2017 and 2018</li>
    </ol>
  </p>

<h2>Results</h2>

<h3>DQ Standalone Performance</h3>
  
  <p>DQ's performance from 2017 and 2018 tells two stories as depicted in <b>Exhibit 1.1</b>.  In 2017 DQ saw a return of 199.4% with a Total Daily Volume of 35,796,200 meaning if you owned this stock and held it for the entirety of 2017 you would have just about tripled your investment.  In 2018 DQ's Total Daily Volume more than doubled to 107,873,900 but saw the returns drop to -62.6%, meaning buying and holding the stock from the start of 2018 until the end would have resulted in a loss on the investment.
  </p>
  
  <p align="center">
  <table>
    <tr>
      <th>Year</th>
      <th>Total Daily Volume</th>
      <th>Starting Amount</th>
      <th>Ending Amount</th>
      <th>Return</th>
    </tr>
    <tr>
      <td>2017</td>
      <td>35,796,200</td>
      <td>$19.85</td>
      <td>$59.44</td>
      <td>199.4%</td>
    </tr>
    <tr>
      <td>2018</td>
      <td>107,873,900</td>
      <td>$62.57</td>
      <td>$23.40</td>
      <td>-62.6%</td>
    </tr>
  </table>
  <b>Exhibit 1.1:</b> DQ Stock Data for 2017 and 2018
  </p>
  
  <p>
  In looking at it over the run of both years, we see that DQ had an overall increase in value of 17%, however the volatility of this stock seems very high given a near 200% increase followed by a near 63% decline.  This makes examining the performance of other "Green Stock" worthwhile when looking for the optimal investment.
  </p>
  
<h3>DQ Compared</h3>
  
  <p>
  To put DQ's volatiltiy into context, it is important to examine the other stocks Steve provided.  In reviewing 2017's performance, <a href="https://github.com/tc9993/stock-analysis/blob/main/VBA_Challenge.xlsm" target="_blank">via the "Run Analysis for All Stocks (Refactored)" button on sheet "All Stocks Analysis" and entering "2017" when prompted</a>, for all 12 provided stocks, we see that 11 of them yielded positive returns with 5 of those 11 seeing a return of over 100%.  Overall, it is evident that 2017 was a good year for investing in "Green Stocks," with DQ leading the way in percent returns while having the smallest Total Daily Volume.
  </p>
  <p>
  When reviewing the 2018 performance of all 12 stocks, right away we see that 10 out of 12 had negative returns, making 2018 a less than desirable year to invest in "Green Stocks."  The exceptions to this were "ENPH" and "RUN" which saw an increase in return in both 2017 and 2018.  The most desirable of the stocks provided for this analysis was ENPH having a 2017 return of 129.5% followed by a 81.9% return in 2018.
  </p>
  <p>
  My recommendation to Steve's parents would be to look at investing in, or more closely monitor the performance of, "ENPH."  This is based on looking at the data across both years and seeing that it was consistently generating high returns.
  </p>

<h2>Summary</h2>

<h3>Refactoring the Code</h3>
  <p>
  While the old code performed the task it needed, the new code does it exponentially quicker which is one of many reasons to refactor code.  A few other reasons to refactor code include making the program run faster, more organized/easier to read, and it even gives yourself a chance to re-format it to make it more uniform.  While refactoring has it's upsides, you should also tread cautiously so as not to introduce any bugs via rearrangring or changing it's structure (you know how the old adage goes "if it ain't broke, don't fix it").
  </p>

<h3>Code Then Vs. Code Now</h3>
  <p>
  While the second and third items under <b>Purpose</b> could have been accompished via the original code, the length of time it took to run the script would not scale well if Steve were to, say, add thousands of new stocks, with hundreds of lines or more of data each, to the analysis.  <b>Exhibit 1.1</b> and <b>Exhibit 1.2</b> show the performance of the original code vs. refactored code in analzying the 2017 data, respectively, while performing the same analytical tasks.
  </p>
  <p align="center">
  <img src="https://github.com/tc9993/stock-analysis/blob/main/Resources/Original_Code_2017.png?raw=true" alt="Original Code Performance for 2017"><br>
  <b>Exhibit 1.1:</b> Original Code Performance for 2017
  </p>
  <p align = "center">
  <img src="https://github.com/tc9993/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png?raw=true" alt="Refactored Code Performance for 2017"><br>
  <b>Exhibit 1.2:</b> Refactored Code Performance for 2017
  </p>
  <p>
  The refactored code shows a decrease in time spent performing the caluclations by 99.2%.  This increase can be attributed to a different approach for looping through the data.  In the original code, a nested For loop ran through 3000+ lines of code 12 times, whereas in the refactored code the For loop only runs through the data set once, reducing the number of cells analyzed from ~36,000 cells to ~3,000 or a 91.6% decrease, pretty closely mirroring the decrease in time spent running the script while achieving identical results.
  </p>
  <p>
  After putting it through a few tests and coming to that the data all turned out the same, it took about an hour to 90 minutes to refactor this code so that it ran 16 seconds faster than before.  Given that this was a simple, straightforward application that investment of time was not too crucial, however had it been a massive application, this refactoring could have been costly from a time to money conversion, however since Steve's such a good friend and I support his parents endeavor to help save the planet, I feel as though these tweaks were well worth my time.
  </p>
