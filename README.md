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

<h3>Refactoring</h3>

  <p>
  While the second and third items under <b>Purpose</b> could have been accompished via the original code, the length of time it took to run the script would not have scaled well if Steve were to, say, add thousands of stocks to the analysis.  <i>Exhibit 1.1</i> and <i>Exhibit 1.2</i> show the performance of the original code vs. refactored code, respectively, while accomplishing the same tasks.
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
