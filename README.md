# Python-Financial-Valuation-Engine
An automated financial modeling script using Pandas and yfinance to calculate DCF, Free Cash Flow and estimate intrinsic share prices to name a few.

## 🧮 Core Calculation Pipeline
To estimate the intrinsic value of each company, the script automatically executes the following financial modeling steps:
* **Free Cash Flow (FCF) Projection:** Applies estimated growth rates to current cash flows to project financial performance over a 5-year forecast window.
* **Terminal Value (Gordon Growth Model):** Calculates the continuous perpetuity value of the company beyond the 5-year forecast.
* **Enterprise Value (EV):** Discounts both the 5-year projected FCFs and the Terminal Value back to Present Value (PV) using a defined discount rate.
* **Equity Value Bridge:** Dynamically pulls the company's live balance sheet to add Cash and Cash Equivalents and subtract Total Debt from the Enterprise Value.
* **Intrinsic Value Per Share:** Divides the final Equity Value by the live number of Shares Outstanding to output the true estimated target price.
* **Margin of Safety:** Compares the calculated intrinsic share price against the live market trading price to determine the percentage of upside or downside.

Back in April, I undertook a semi-conductor market analysis following their recent boom as their stock rocketed. At the time I manually pulled all data from Yahoo Finance and input it into CSV files due to Yahoo locking their spreadsheet download option behind a paywall. Fast forward to today, I have decent knowledge of python's capabilities and I have taken it upon myself to write a script that can not only fetch the data for me from Yahoo Finance but also perform valuations, and estimations to mention a few. 

This is a relatively straightforward script, which allows for up to 3 companies at a time to be valuated. Since the script runs on Yahoo Finance, all that is needed is to feed it the ticker symbols (e.g. Apple-AAPL, Microsoft-MSFT) and the extraction and valuation will be underway. The greatest takeaway is that I don't have to manually extract all the info from Yahoo Finance and input the data myself, coupled with the fact that I can command python to load all the data which includes calculations into a spreadsheet, this makes for an effecient script in the long-term. 

Here is the link to my semi-conductor market analysis from April - https://github.com/Harridinho-art/Semiconductor-market-analysis

For my current script, I did not focus on semi-conductor stocks but instead I broadened the scope to include every company on Yahoo's database. The engine is currently being scaled to process up to 10 companies simultaneously.
## 🖥️ Live Terminal Output
Here is an example of the engine dynamically pulling data and valuing in real-time:

<img width="1886" height="1007" alt="Screenshot 2026-09-06 173116" src="https://github.com/user-attachments/assets/3a18f33a-fa6f-4ba3-b9e7-2299075ccb56" />
<img width="1830" height="975" alt="Screenshot 2026-09-06 173101" src="https://github.com/user-attachments/assets/a8957048-9789-4e42-a1d9-fdc8560d160d" />
<img width="1881" height="942" alt="Screenshot 2026-09-06 174809" src="https://github.com/user-attachments/assets/41d287ef-e1f1-427e-980f-70e86e6811eb" />

## ⚙️ How to Run Locally
If you want to test a valuation yourself? 
1. Clone this repository to your local machine.
2. Install the required dependencies by running: `pip install -r requirements.txt`
3. Execute the script in your terminal: `python Valuation_engine.py`
4. Enter any valid stock ticker when prompted!

Install - [requirements.txt](https://github.com/user-attachments/files/31916806/requirements.txt)

For the actual file/script, here's the golden key - [Valuation_engine.py](https://github.com/user-attachments/files/31916824/Valuation_engine.py)
