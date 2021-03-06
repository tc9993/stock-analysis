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
      <th>Return</th>
    </tr>
    <tr>
      <td>2017</td>
      <td>35,796,200</td>
      <td>199.4%</td>
    </tr>
    <tr>
      <td>2018</td>
      <td>107,873,900</td>
      <td>-62.6%</td>
    </tr>
  </table>
  <b>Exhibit 1.1:</b> DQ Stock Data for 2017 and 2018
  </p>
  <p>
  In looking at it over the run of both years, we see that DQ overall increased in value
  
  2017 Start 19.85
  2017 End 59.44
  2018 Start 62.57
  2018 End 23.4

<h2>Summary</h2>

<h3>Refactoring</h3>

  <p>
  While the second and third items under <b>Purpose</b> could have been accompished via the original code, the length of time it took to run the script would not have scaled well if Steve were to, say, add thousands of stocks to the analysis.  <b>Exhibit 1.1</b> and <b>Exhibit 1.2</b> show the performance of the original code vs. refactored code, respectively, while accomplishing the same tasks.
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
  The refactored code shows a decrease in time spent performing the caluclations by 99.2%.  This increase can be attributed to the different approach to looping through the data.  In the original code, a nested For loop ran through 3000+ lines of code 12 times, whereas in the refactored code the For loop only runs through the data set once, reducing the number of cells analyzed from ~36,000 cells to ~3,000 or a 91.6% decrease, pretty closely mirroring the decrease in time spent running the script while achieving identical results.
  </p>
  
  
