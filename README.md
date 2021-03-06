# StocksAI
Stocks + Artificial Intelligence

# Project Details
"Design a CSP that takes as input mutual fund symbols and various attributes of each fund and that constructs configurations of mutual funds (or stocks) as investment portfolios for people. You can download a list of NASDAQ mutual funds with attributes at http://www.nasdaqtrader.com or find a comparable listing for Canadian mutual funds. Create a program that will search through funds in order to create a portfolio that matches a given user's investment goals. For example, some investors want income generation, while others are interested in growth. Some are conservative while others are comfortable with some risk. Some want to avoid high mutual fund management fees. Some wish to have a percentage of their portfolio invested in ethical or green funds. Others maywish to avoid certain sectors of the market. Encode these goals as constraints (i.e. constraints on fund types, pricing agents, et cetera). Evaluate the performance of a variety of CSP based approaches relative to blind or simple depth-first search for building portfolios."

# How to run
You will need two input files: a csv containing stocks data, a csv containing customers and their desired constraints
There are two programs: research.py, stocks_csp.py


Follow Step 0) if you would like to test run the program before generating your own data. 
Step 0) run

        $ python3 stocks_csp.py
 
A stocks data file (quotes.csv) and user constraints files (user_data.csv) are provided by default. Simply run the command above, hit enter twice, and a list of portfolios will be printed on your screen. Also feel free to change the input, and watch its rammifications.


Step 1) run

        $ python3 research.py
        
Enter your stocks data file to perform research on. The program will create a new stocks data.csv supporting additional columns like region, industry, eco friendly etc. The research program uses randomization and limit caps to assign all the companies to a certain region, industry etc. These additional columns allow us to make much more intricate constraints on the stocks portfolio we build.

Step 2) run

        $ python3 stocks_csp.py
        
When prompted, enter the user constraints file and researched stocks file (generated by step 1). The program will go through each user in the user user constraints file and generate a portfolio for them.
