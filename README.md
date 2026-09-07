# Python-Financial-Valuation-Engine
An automated financial modeling script using Pandas and yfinance to calculate DCF, Free Cash Flow and estimate intrinsic share prices.
Back in April, I endertook a semi-conductor market analysis follwing their recent boom as their stock rocketed. At the time I manually pulled all data from Yahoo Finance and input it into CSV files due to Yahoo locking their spreadsheet downlaod option behind a paywall. Fast forward to today, I have been blessed with the decent knowledge of python's capabilities and I have undertook a challenge to write a script that can not only fetch the data for me from Yahoo Finance but also perform valuations, and estimations to mention a few. 

This is a reletively straightforward script, but I am making progress to pull and valuate up to 10 companies at once. The greatest takeaway is that I don't have to manually extract all the infor from Yahoo Finance and input the data myself, coupled with the fact that I can command python to load all the data into a spreadhseet, this makes for an effecient script in the long-term. 

By the way, here is the link to my semi-conductor market analysis from April - https://github.com/Harridinho-art/Semiconductor-market-analysis

For my current script, I did not focus on semi-conductor stocks but instead just random companies in the S&P 500, limited to 3 of course. ## 🖥️ Live Terminal Output
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
