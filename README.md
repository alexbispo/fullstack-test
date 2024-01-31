## Insider trading

Insider trading involves trading in a public company's stock or other securities by someone with non-public, material information about the company.
Insider transactions are legal if the insider makes a trade and reports it to the Securities and Exchange Commission.


### Instructions
The idea is to create a process that that will extract the data from the **sec.gov** and **edgar** and analyse it to report inside trading.

The criteria to select the companies is up to you! You can find a list of public tickers in the links below.

The expected response will be the ticker/company, the person who did the transaction, job title, the date and the amount of shares and how much in percentage of the market cap that represents. 

*bonus*: React ui to display the results

*extra bonus*: unit tests and documentation

-----

### Publish your solution
- Fork this repository
- Create a new branch in your github
- Create a pull request to the main branch with your solution and send us the link

-----

#### Useful links:
- https://www.sec.gov/files/forms-3-4-5.pdf
- https://www.sec.gov/files/company_tickers_exchange.json
- https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=000879764&owner=include&count=100&output=atom
- https://www.sec.gov/cgi-bin/browse-edgar?action=getcurrent&CIK=&type=&company=&dateb=&owner=include&start=0&count=100&output=atom
- https://finance.yahoo.com/quote/AAPL?p=AAPL
- https://query2.finance.yahoo.com/v7/finance/options/AAPL
- https://github.com/ranaroussi/yfinance/blob/8975689bd19f96ea4655688611b0d853822eb5ec/yfinance/ticker.py


#### Solution implementation:

![Solution Diagram](fullstack_test_diagram.png)

##### Just to run locally:

###### Requirements:

* Docker version >= 24.0.7
* Docker Compose version >= v2.23.3 (usually it already is builtin in Docker)

###### Run

In the fullstack-test directory run:

        $ docker-compose up --build

After, access to the http://localhost:3000

###### Backlog (improvements):

* Fallback for missing data like market cap and shares amount.

* Implementation of circuit breacker pattern at integration to Yahoo Finance API.

* Implements pagination for the API and handle it at frontend.

* Improve the frontend code, breaking things in more components.

* Write more tests.
