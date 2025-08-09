📊 CoinMarketCap Gainers & Losers CLI
A lightweight Python command-line tool that fetches and displays the top cryptocurrency gainers or losers over the last 24 hours using the CoinMarketCap API.

This tool is ideal for traders, analysts, or enthusiasts who want quick market insights directly from their terminal.

🚀 Features
Fetches real-time cryptocurrency data from CoinMarketCap.
Displays top gainers or top losers for the last 24 hours.
Customizable number of results.
Supports API key from environment variables or direct CLI input.
Clean, tabular output format for easy reading.

📋 Requirements
Python 3.8+
CoinMarketCap API key (free tier works with this endpoint)
requests Python library

🔑 Getting an API Key
Create a free account at CoinMarketCap Developer Portal.
Navigate to API Key in your dashboard.
Copy your key for later use.

```bash
⚙️ Installation
1. Clone the repository
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
cd <YOUR_REPO>

2. Create a virtual environment
python -m venv .venv
# Activate on Windows
.venv\Scripts\activate

3. Install dependencies
pip install -r requirements.txt

🔧 Configuration
Option 1 — Set as environment variable
setx CMC_API_KEY "your_api_key_here"

Option 2 — Pass API key directly in command
python cmc_trending.py --api-key your_api_key_here --mode gainers --limit 10

🖥 Usage
View top 10 gainers
python cmc_trending.py --mode gainers --limit 10
View top 20 losers
python cmc_trending.py --mode losers --limit 20
Specify API key at runtime
python cmc_trending.py --mode gainers --limit 15 --api-key your_api_key_here

📌 Example Output
Top 20 losers (24h)
#   Name             Symbol      Price($)    %24h
--------------------------------------------------
1   Story            IP           6.4355    -2.83
2   Flare            FLR          0.0236    -1.78
3   Stellar          XLM          0.4549    -1.24
...

📂 Project Structure
cmc_trending.py      # Main script
requirements.txt     # Dependencies
README.md            # Documentation

🛠 Troubleshooting
401 Unauthorized → API key is missing or invalid. Verify it’s set correctly.

Empty results → Check your API tier supports the endpoint used.

SSL / network errors → Ensure you have internet access and requests library is up to date.
