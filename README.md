With the identified capabilities afforded by `jugaad_data` and `yfinance` Python Packages, we're equipped to create a "Dashboard making program" to study individual company's financial performance, undervalued or overvalued, buy or no buy, configure the policies for buy and no-buy.



# Analyze Data


```python
from jugaad_data.nse import NSELive
n = NSELive()
```


```python
n.stock_quote("JIOFIN")
```




    {'info': {'symbol': 'JIOFIN',
      'companyName': 'Jio Financial Services Limited',
      'industry': 'Investment Company',
      'activeSeries': ['EQ'],
      'debtSeries': [],
      'isFNOSec': True,
      'isCASec': False,
      'isSLBSec': True,
      'isDebtSec': False,
      'isSuspended': False,
      'tempSuspendedSeries': [],
      'isETFSec': False,
      'isDelisted': False,
      'isin': 'INE758E01017',
      'slb_isin': 'INE758E01017',
      'listingDate': '2023-08-21',
      'isMunicipalBond': False,
      'isHybridSymbol': False,
      'isTop10': False,
      'identifier': 'JIOFINEQN'},
     'metadata': {'series': 'EQ',
      'symbol': 'JIOFIN',
      'isin': 'INE758E01017',
      'status': 'Listed',
      'listingDate': '21-Aug-2023',
      'industry': 'Investment Company',
      'lastUpdateTime': '19-Feb-2025 16:00:00',
      'pdSectorPe': 118.72,
      'pdSymbolPe': 118.72,
      'pdSectorInd': 'NIFTY NEXT 50',
      'pdSectorIndAll': ['NIFTY NEXT 50',
       'NIFTY SERVICES SECTOR',
       'NIFTY 200',
       'NIFTY 500',
       'NIFTY100 EQUAL WEIGHT',
       'NIFTY LARGEMIDCAP 250',
       'NIFTY100 ENHANCED ESG',
       'NIFTY RURAL',
       'NIFTY FINANCIAL SERVICES EX-BANK',
       'NIFTY TOTAL MARKET',
       'NIFTY500 EQUAL WEIGHT',
       'NIFTY500 LARGEMIDSMALL EQUAL-CAP WEIGHTED',
       'NIFTY500 MULTICAP 50:25:25',
       'NIFTY100 ESG',
       'NIFTY INDIA SELECT 5 CORPORATE GROUPS (MAATR)',
       'NIFTY 100']},
     'securityInfo': {'boardStatus': 'Main',
      'tradingStatus': 'Active',
      'tradingSegment': 'Normal Market',
      'sessionNo': '-',
      'slb': 'Yes',
      'classOfShare': 'Equity',
      'derivatives': 'Yes',
      'surveillance': {'surv': None, 'desc': None},
      'faceValue': 10,
      'issuedSize': 6353141623},
     'sddDetails': {'SDDAuditor': '-', 'SDDStatus': '-'},
     'currentMarketType': 'NM',
     'priceInfo': {'lastPrice': 228.59,
      'change': 7.569999999999993,
      'pChange': 3.4250294091032454,
      'previousClose': 221.02,
      'open': 221.02,
      'close': 228.92,
      'vwap': 226.33,
      'stockIndClosePrice': 0,
      'lowerCP': '198.91',
      'upperCP': '243.12',
      'pPriceBand': 'No Band',
      'basePrice': 0,
      'intraDayHighLow': {'min': 219.26, 'max': 229.7, 'value': 228.59},
      'weekHighLow': {'min': 217.01,
       'minDate': '18-Feb-2025',
       'max': 394.7,
       'maxDate': '23-Apr-2024',
       'value': 228.59},
      'iNavValue': None,
      'checkINAV': False,
      'tickSize': 0.01,
      'ieq': ''},
     'industryInfo': {'macro': 'Financial Services',
      'sector': 'Financial Services',
      'industry': 'Finance',
      'basicIndustry': 'Investment Company'},
     'preOpenMarket': {'preopen': [{'price': 220.75, 'buyQty': 500, 'sellQty': 0},
       {'price': 220.85, 'buyQty': 300, 'sellQty': 0},
       {'price': 220.9, 'buyQty': 10, 'sellQty': 0},
       {'price': 220.95, 'buyQty': 36, 'sellQty': 0},
       {'price': 221, 'buyQty': 1692, 'sellQty': 0},
       {'price': 221.02, 'buyQty': 0, 'sellQty': 2556, 'iep': True},
       {'price': 221.1, 'buyQty': 0, 'sellQty': 1},
       {'price': 221.25, 'buyQty': 0, 'sellQty': 500},
       {'price': 221.4, 'buyQty': 0, 'sellQty': 550},
       {'price': 221.48, 'buyQty': 0, 'sellQty': 400}],
      'ato': {'buy': 0, 'sell': 0},
      'IEP': 221.02,
      'totalTradedVolume': 43990,
      'finalPrice': 0,
      'finalQuantity': 0,
      'lastUpdateTime': '19-Feb-2025 09:07:34',
      'totalBuyQuantity': 343724,
      'totalSellQuantity': 310802,
      'atoBuyQty': 0,
      'atoSellQty': 0,
      'Change': 0,
      'perChange': 0,
      'prevClose': 221.02}}




```python
n.stock_quote("TATAPOWER")
```




    {'info': {'symbol': 'TATAPOWER',
      'companyName': 'Tata Power Company Limited',
      'industry': 'Integrated Power Utilities',
      'activeSeries': ['EQ'],
      'debtSeries': [],
      'isFNOSec': True,
      'isCASec': False,
      'isSLBSec': True,
      'isDebtSec': False,
      'isSuspended': False,
      'tempSuspendedSeries': [],
      'isETFSec': False,
      'isDelisted': False,
      'isin': 'INE245A01021',
      'slb_isin': 'INE245A01021',
      'listingDate': '1996-04-03',
      'isMunicipalBond': False,
      'isHybridSymbol': False,
      'isTop10': False,
      'identifier': 'TATAPOWEREQN'},
     'metadata': {'series': 'EQ',
      'symbol': 'TATAPOWER',
      'isin': 'INE245A01021',
      'status': 'Listed',
      'listingDate': '03-Apr-1996',
      'industry': 'Integrated Power Utilities',
      'lastUpdateTime': '19-Feb-2025 16:00:00',
      'pdSectorPe': 30.01,
      'pdSymbolPe': 31.11,
      'pdSectorInd': 'NIFTY NEXT 50',
      'pdSectorIndAll': ['NIFTY NEXT 50',
       'NIFTY100 ALPHA 30',
       'NIFTY INFRASTRUCTURE',
       'NIFTY SERVICES SECTOR',
       'NIFTY 200',
       'NIFTY 500',
       'NIFTY COMMODITIES',
       'NIFTY INDIA CONSUMPTION',
       'NIFTY HIGH BETA 50',
       'NIFTY INDIA CORPORATE GROUP INDEX - TATA GROUP 25% CAP',
       'NIFTY100 EQUAL WEIGHT',
       'NIFTY INDIA CORPORATE GROUP INDEX - TATA GROUP',
       'NIFTY100 ESG SECTOR LEADERS',
       'NIFTY LARGEMIDCAP 250',
       'NIFTY100 ENHANCED ESG',
       'NIFTY HOUSING',
       'NIFTY TOTAL MARKET',
       'NIFTY500 LARGEMIDSMALL EQUAL-CAP WEIGHTED',
       'NIFTY RURAL',
       'NIFTY INDIA SELECT 5 CORPORATE GROUPS (MAATR)',
       'NIFTY500 EQUAL WEIGHT',
       'NIFTY500 MULTICAP 50:25:25',
       'NIFTY500 MULTICAP INFRASTRUCTURE 50:30:20',
       'NIFTY100 ESG',
       'NIFTY 100',
       'NIFTY ENERGY']},
     'securityInfo': {'boardStatus': 'Main',
      'tradingStatus': 'Active',
      'tradingSegment': 'Normal Market',
      'sessionNo': '-',
      'slb': 'Yes',
      'classOfShare': 'Equity',
      'derivatives': 'Yes',
      'surveillance': {'surv': None, 'desc': None},
      'faceValue': 1,
      'issuedSize': 3195339547},
     'sddDetails': {'SDDAuditor': '-', 'SDDStatus': '-'},
     'currentMarketType': 'NM',
     'priceInfo': {'lastPrice': 347.5,
      'change': 7.899999999999977,
      'pChange': 2.3262661955241395,
      'previousClose': 339.6,
      'open': 337,
      'close': 347.65,
      'vwap': 345.59,
      'stockIndClosePrice': 0,
      'lowerCP': '305.65',
      'upperCP': '373.55',
      'pPriceBand': 'No Band',
      'basePrice': 0,
      'intraDayHighLow': {'min': 334.7, 'max': 350, 'value': 347.5},
      'weekHighLow': {'min': 326.35,
       'minDate': '17-Feb-2025',
       'max': 494.85,
       'maxDate': '27-Sep-2024',
       'value': 347.5},
      'iNavValue': None,
      'checkINAV': False,
      'tickSize': 0.05,
      'ieq': ''},
     'industryInfo': {'macro': 'Utilities',
      'sector': 'Power',
      'industry': 'Power',
      'basicIndustry': 'Integrated Power Utilities'},
     'preOpenMarket': {'preopen': [{'price': 336.2, 'buyQty': 550, 'sellQty': 0},
       {'price': 336.5, 'buyQty': 300, 'sellQty': 0},
       {'price': 336.6, 'buyQty': 2000, 'sellQty': 0},
       {'price': 336.65, 'buyQty': 4, 'sellQty': 0},
       {'price': 336.95, 'buyQty': 481, 'sellQty': 0},
       {'price': 337, 'buyQty': 0, 'sellQty': 5295, 'iep': True},
       {'price': 337.2, 'buyQty': 0, 'sellQty': 17},
       {'price': 337.25, 'buyQty': 0, 'sellQty': 27},
       {'price': 337.4, 'buyQty': 0, 'sellQty': 200},
       {'price': 337.5, 'buyQty': 0, 'sellQty': 1091}],
      'ato': {'buy': 0, 'sell': 0},
      'IEP': 337,
      'totalTradedVolume': 11130,
      'finalPrice': 0,
      'finalQuantity': 0,
      'lastUpdateTime': '19-Feb-2025 09:07:34',
      'totalBuyQuantity': 78835,
      'totalSellQuantity': 90868,
      'atoBuyQty': 0,
      'atoSellQty': 0,
      'Change': -2.6000000000000227,
      'perChange': -0.7656065959952952,
      'prevClose': 339.6}}




```python

```


```python
example_data = {'info': {'symbol': 'NTPCGREEN',
  'companyName': 'NTPC Green Energy Limited',
  'industry': 'Power Generation',
  'activeSeries': ['EQ'],
  'debtSeries': [],
  'isFNOSec': False,
  'isCASec': False,
  'isSLBSec': True,
  'isDebtSec': False,
  'isSuspended': False,
  'tempSuspendedSeries': [],
  'isETFSec': False,
  'isDelisted': False,
  'isin': 'INE0ONG01011',
  'slb_isin': 'INE0ONG01011',
  'listingDate': '2024-11-27',
  'isMunicipalBond': False,
  'isTop10': False,
  'identifier': 'NTPCGREENEQN'},
 'metadata': {'series': 'EQ',
  'symbol': 'NTPCGREEN',
  'isin': 'INE0ONG01011',
  'status': 'Listed',
  'listingDate': '27-Nov-2024',
  'industry': 'Power Generation',
  'lastUpdateTime': '13-Feb-2025 12:27:50',
  'pdSectorPe': 'NA',
  'pdSymbolPe': 'NA',
  'pdSectorInd': 'NIFTY IPO',
  'pdSectorIndAll': ['NIFTY IPO']},
 'securityInfo': {'boardStatus': 'Main',
  'tradingStatus': 'Active',
  'tradingSegment': 'Normal Market',
  'sessionNo': '-',
  'slb': 'Yes',
  'classOfShare': 'Equity',
  'derivatives': 'No',
  'surveillance': {'surv': '-', 'desc': ''},
  'faceValue': 10,
  'issuedSize': 8426329669},
 'sddDetails': {'SDDAuditor': '-', 'SDDStatus': '-'},
 'currentMarketType': 'NM',
 'priceInfo': {'lastPrice': 108.05,
  'change': 0.5699999999999932,
  'pChange': 0.5303312244138381,
  'previousClose': 107.48,
  'open': 108.5,
  'close': 0,
  'vwap': 108.31,
  'stockIndClosePrice': 0,
  'lowerCP': '85.98',
  'upperCP': '128.97',
  'pPriceBand': '20',
  'basePrice': 107.48,
  'intraDayHighLow': {'min': 107.77, 'max': 109.84, 'value': 108.05},
  'weekHighLow': {'min': 104.81,
   'minDate': '12-Feb-2025',
   'max': 155.35,
   'maxDate': '04-Dec-2024',
   'value': 108.05},
  'iNavValue': None,
  'checkINAV': False,
  'tickSize': 0.01,
  'ieq': ''},
 'industryInfo': {'macro': 'Utilities',
  'sector': 'Power',
  'industry': 'Power',
  'basicIndustry': 'Power Generation'},
 'preOpenMarket': {'preopen': [{'price': 108, 'buyQty': 3458, 'sellQty': 0},
   {'price': 108.01, 'buyQty': 209, 'sellQty': 0},
   {'price': 108.05, 'buyQty': 100, 'sellQty': 0},
   {'price': 108.2, 'buyQty': 60, 'sellQty': 0},
   {'price': 108.48, 'buyQty': 500, 'sellQty': 0},
   {'price': 108.5, 'buyQty': 0, 'sellQty': 330, 'iep': True},
   {'price': 108.6, 'buyQty': 0, 'sellQty': 100},
   {'price': 108.7, 'buyQty': 0, 'sellQty': 100},
   {'price': 108.8, 'buyQty': 0, 'sellQty': 120},
   {'price': 108.9, 'buyQty': 0, 'sellQty': 190}],
  'ato': {'buy': 0, 'sell': 0},
  'IEP': 108.5,
  'totalTradedVolume': 28483,
  'finalPrice': 108.5,
  'finalQuantity': 28483,
  'lastUpdateTime': '13-Feb-2025 09:07:37',
  'totalBuyQuantity': 212378,
  'totalSellQuantity': 235858,
  'atoBuyQty': 0,
  'atoSellQty': 0,
  'Change': 1.019999999999996,
  'perChange': 0.9490137700037179,
  'prevClose': 107.48}}
```


```python
example_data
```




    {'info': {'symbol': 'NTPCGREEN',
      'companyName': 'NTPC Green Energy Limited',
      'industry': 'Power Generation',
      'activeSeries': ['EQ'],
      'debtSeries': [],
      'isFNOSec': False,
      'isCASec': False,
      'isSLBSec': True,
      'isDebtSec': False,
      'isSuspended': False,
      'tempSuspendedSeries': [],
      'isETFSec': False,
      'isDelisted': False,
      'isin': 'INE0ONG01011',
      'slb_isin': 'INE0ONG01011',
      'listingDate': '2024-11-27',
      'isMunicipalBond': False,
      'isTop10': False,
      'identifier': 'NTPCGREENEQN'},
     'metadata': {'series': 'EQ',
      'symbol': 'NTPCGREEN',
      'isin': 'INE0ONG01011',
      'status': 'Listed',
      'listingDate': '27-Nov-2024',
      'industry': 'Power Generation',
      'lastUpdateTime': '13-Feb-2025 12:27:50',
      'pdSectorPe': 'NA',
      'pdSymbolPe': 'NA',
      'pdSectorInd': 'NIFTY IPO',
      'pdSectorIndAll': ['NIFTY IPO']},
     'securityInfo': {'boardStatus': 'Main',
      'tradingStatus': 'Active',
      'tradingSegment': 'Normal Market',
      'sessionNo': '-',
      'slb': 'Yes',
      'classOfShare': 'Equity',
      'derivatives': 'No',
      'surveillance': {'surv': '-', 'desc': ''},
      'faceValue': 10,
      'issuedSize': 8426329669},
     'sddDetails': {'SDDAuditor': '-', 'SDDStatus': '-'},
     'currentMarketType': 'NM',
     'priceInfo': {'lastPrice': 108.05,
      'change': 0.5699999999999932,
      'pChange': 0.5303312244138381,
      'previousClose': 107.48,
      'open': 108.5,
      'close': 0,
      'vwap': 108.31,
      'stockIndClosePrice': 0,
      'lowerCP': '85.98',
      'upperCP': '128.97',
      'pPriceBand': '20',
      'basePrice': 107.48,
      'intraDayHighLow': {'min': 107.77, 'max': 109.84, 'value': 108.05},
      'weekHighLow': {'min': 104.81,
       'minDate': '12-Feb-2025',
       'max': 155.35,
       'maxDate': '04-Dec-2024',
       'value': 108.05},
      'iNavValue': None,
      'checkINAV': False,
      'tickSize': 0.01,
      'ieq': ''},
     'industryInfo': {'macro': 'Utilities',
      'sector': 'Power',
      'industry': 'Power',
      'basicIndustry': 'Power Generation'},
     'preOpenMarket': {'preopen': [{'price': 108, 'buyQty': 3458, 'sellQty': 0},
       {'price': 108.01, 'buyQty': 209, 'sellQty': 0},
       {'price': 108.05, 'buyQty': 100, 'sellQty': 0},
       {'price': 108.2, 'buyQty': 60, 'sellQty': 0},
       {'price': 108.48, 'buyQty': 500, 'sellQty': 0},
       {'price': 108.5, 'buyQty': 0, 'sellQty': 330, 'iep': True},
       {'price': 108.6, 'buyQty': 0, 'sellQty': 100},
       {'price': 108.7, 'buyQty': 0, 'sellQty': 100},
       {'price': 108.8, 'buyQty': 0, 'sellQty': 120},
       {'price': 108.9, 'buyQty': 0, 'sellQty': 190}],
      'ato': {'buy': 0, 'sell': 0},
      'IEP': 108.5,
      'totalTradedVolume': 28483,
      'finalPrice': 108.5,
      'finalQuantity': 28483,
      'lastUpdateTime': '13-Feb-2025 09:07:37',
      'totalBuyQuantity': 212378,
      'totalSellQuantity': 235858,
      'atoBuyQty': 0,
      'atoSellQty': 0,
      'Change': 1.019999999999996,
      'perChange': 0.9490137700037179,
      'prevClose': 107.48}}




```python
def calculate_stock_metrics(stock_data):
    metrics = {}
    
    # Price-to-Earnings Ratio - Not possible without earnings data
    metrics['P/E Ratio'] = 'N/A'
    
    # Dividend Yield - Not possible without dividend data
    metrics['Dividend Yield'] = 'N/A'
    
    # Earnings Per Share - Not possible without earnings or shares outstanding data
    metrics['EPS'] = 'N/A'
    
    # Return on Equity - Not possible without net income or shareholders' equity
    metrics['ROE'] = 'N/A'
    
    # Market Capitalization
    # Assuming 'issuedSize' is the number of shares outstanding
    metrics['Market Cap'] = stock_data['priceInfo']['lastPrice'] * stock_data['securityInfo']['issuedSize']
    
    # Price to Book Ratio - Not possible without book value data
    metrics['P/B Ratio'] = 'N/A'
    
    # Debt to Equity Ratio - Not possible without liabilities or equity data
    metrics['Debt/Equity Ratio'] = 'N/A'
    
    # Revenue Growth Rate - Not possible without revenue data
    metrics['Revenue Growth Rate'] = 'N/A'
    
    # Additional Metrics we can calculate from the data:
    
    # Change in Price
    metrics['Price Change'] = stock_data['priceInfo']['change']
    
    # Percentage Change in Price
    metrics['Percentage Price Change'] = stock_data['priceInfo']['pChange']
    
    # 52-Week High and Low
    metrics['52-Week High'] = stock_data['priceInfo']['weekHighLow']['max']
    metrics['52-Week Low'] = stock_data['priceInfo']['weekHighLow']['min']
    
    # Volume Weighted Average Price (VWAP)
    metrics['VWAP'] = stock_data['priceInfo']['vwap']
    
    return metrics

# Example usage with the provided data:
# example_data = {
#     # ... (your provided data structure)
# }

# Extracting the necessary data for our function
extracted_data = {
    'priceInfo': example_data['priceInfo'],
    'securityInfo': example_data['securityInfo']
}

# Calculate metrics
metrics = calculate_stock_metrics(extracted_data)
for key, value in metrics.items():
    print(f"{key}: {value}")
```

    P/E Ratio: N/A
    Dividend Yield: N/A
    EPS: N/A
    ROE: N/A
    Market Cap: 910464920735.45
    P/B Ratio: N/A
    Debt/Equity Ratio: N/A
    Revenue Growth Rate: N/A
    Price Change: 0.5699999999999932
    Percentage Price Change: 0.5303312244138381
    52-Week High: 155.35
    52-Week Low: 104.81
    VWAP: 108.31


# How to get EPS : Earning Per Share?

We have these two responses:

To find the exact Earnings Per Share (EPS) for NTPC Green Energy Limited (NTPCGREEN), you would typically need to look at:

Company's latest quarterly or annual financial statements, which report net income and number of shares outstanding. 
Financial news or analysis websites that compile and report this data.

Unfortunately, the data you've provided doesn't include the necessary financial figures to calculate EPS. Here's what you can do:

Method 1: Direct Lookup
Check financial news or stock market analysis websites like:
Moneycontrol.com
Screener.in
BSE/NSE official websites (bseindia.com, nseindia.com)
Financial sections of business news sites like economictimes.indiatimes.com or livemint.com.

You might search for "NTPC Green Energy Limited EPS" or look for their financial results announcements.

Method 2: Use Financial Data APIs or Services
APIs like Alpha Vantage, Yahoo Finance API, or paid services like Refinitiv or Bloomberg might provide EPS data. Here's how you might do this with Python using yfinance as an example (assuming NTPCGREEN is listed with a symbol you can query):

```python
import yfinance as yf

# Fetching data for NTPCGREEN - replace with the actual ticker if different
stock = yf.Ticker('NTPCGREEN.NS')  # Using .NS for NSE stocks
financials = stock.financials
trailing_eps = stock.info.get('trailingEps')

print(f"Trailing EPS: {trailing_eps}")
```
Note: yfinance might not have data for every listed company, especially new ones like NTPCGREEN, which was listed in November 2024 according to your data.

Method 3: Check Company Announcements
Look for NTPC Green Energy's investor relations section on their official website or announcements on stock exchange websites for the latest earnings reports.

Current Information from Web Results:
Based on the web results provided earlier:

From web:9: There's no direct mention of EPS, but NTPC Green Energy Limited's financial performance is discussed, including a net profit for a six-month period in 2024, but without specifying the number of shares for EPS calculation.
From web:12: Similarly, there's mention of quarterly results, but specific EPS isn't stated.

Since I cannot invent or improvise information not supported by references, and none of the provided web results give a precise EPS figure, I suggest:

Use a current web search or check the mentioned sources directly for the latest financial data to get the exact EPS for NTPCGREEN. If you want to do that:
Would you like me to help you perform a web search for the current EPS of NTPCGREEN?


To find the Earnings Per Share (EPS) of NTPC Green Energy Limited (NTPCGREEN), we need to rely on the company's financial data, specifically its net income (profit) and the number of outstanding shares. Since the provided data from your earlier example does not include financial statements like net income, and jugaad_data primarily provides price data rather than detailed financials, we need to use available public financial data.

Available Information:
From your provided data:
Number of outstanding shares (issuedSize): 8,426,329,669 (from securityInfo).
Current price: 108.05 (from priceInfo['lastPrice']).

However, net income (or profit after tax) is not directly available in the data. To calculate EPS, we need the net profit, which can be sourced from financial reports, such as the company's quarterly or annual results.

Step 1: Find Net Profit for NTPCGREEN
Based on recent public financial data (as of the latest available reports, e.g., from the company's filings on NSE/BSE or financial websites like Moneycontrol, Economic Times, or Screener.in):

For the quarter ended December 31, 2024, NTPC Green Energy reported a net profit of ₹65.61 crore (₹656.1 million) according to the company's financial results (source: NSE filings and financial websites like Moneycontrol).
Annualized net profit data is not directly available, but for EPS, we typically use the trailing twelve months (TTM) net profit. For simplicity, if we need TTM data and it's not available, we can use the latest quarterly data and annualize it (multiply by 4 for an estimate, though this is less precise).

For the latest available TTM data (as of December 2024):
TTM Net Profit: Based on financial reports, NTPC Green Energy's TTM net profit is approximately ₹242.26 crore (₹2,422.6 million) as per available data from financial websites (e.g., Screener.in or Moneycontrol).

Step 2: Calculate EPS
EPS = Net Profit / Number of Outstanding Shares

Net Profit (TTM): ₹2,422.6 million (₹242.26 crore)
Outstanding Shares: 8,426,329,669

Convert net profit to the same unit (e.g., ₹):
EPS = ₹2,422.6 million / 8,426,329,669 = ₹0.287 per share

Final EPS:
The Earnings Per Share (EPS) for NTPCGREEN based on TTM data as of December 2024 is approximately ₹0.29 (rounded).

Step 3: Calculate P/E Ratio (Optional)
Since you previously wanted to calculate the P/E ratio:
Current Price = ₹108.05
P/E Ratio = Current Price / EPS = 108.05 / 0.29 ≈ 373.28

Notes:
The EPS value depends on the accuracy of the net profit figure. The ₹242.26 crore TTM net profit is based on available data from financial websites as of the latest reporting period (December 2024). For the most precise value, refer to NTPC Green Energy's latest quarterly or annual report from NSE/BSE or financial platforms.
The P/E ratio of ~373 is very high, which could indicate overvaluation or expectations of significant future growth, common for newly listed companies in high-growth sectors like renewable energy. However, verify the net profit and EPS from official sources for accuracy.
If you need quarterly EPS instead of TTM, use the quarterly net profit (₹65.61 crore):
Quarterly EPS = ₹656.1 million / 8,426,329,669 = ₹0.078 per share.

Sources:
Financial data sourced from NTPC Green Energy's filings on NSE/BSE, Moneycontrol, and Screener.in as of the latest available reports (December 2024).
Always cross-check with the latest financial statements for the most accurate figures.



```python

```


```python
import yfinance as yf

# Fetching data for M&M.NS - replace with the actual ticker if different
stock = yf.Ticker('M&M.NS')  # Using .NS for NSE stocks
financials = stock.financials
trailing_eps = stock.info.get('trailingEps')

print(f"Trailing EPS: {trailing_eps}")
```

    Trailing EPS: 110.48


Could not get the EPS of NTPCGREEN from yfinance above. However, with `https://www.moneycontrol.com/financials/ntpcgreenenergyltd/profit-lossVI/NGE` got the number : 

EPS_NTPCGREEN =  ₹ 0.78

P/E ratio : P/E Ratio = Current Price / EPS = 107/0.78 = 


```python
107 / 0.78
```




    137.17948717948718




```python

```
