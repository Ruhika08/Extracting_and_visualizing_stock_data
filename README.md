# Graphing Stock Data and Revenue

## Overview
This project is designed to visualize the stock price and quarterly revenue data of a company. The script retrieves stock data using the `yfinance` library and scrapes quarterly revenue data from an HTML file or a website. The data is then plotted using `plotly` for interactive visualization.

## Features
- Retrieve historical stock price data for any publicly traded company using its ticker symbol.
- Scrape quarterly revenue data from an HTML file or directly from the [Macrotrends](https://www.macrotrends.net/) website.
- Visualize both stock prices and revenue data in a single interactive graph with easy-to-use date filters.

## Prerequisites
To run this script, you need the following:
- Python 3.7 or later installed on your system.
- The following Python libraries installed:
  ```bash
  pip install yfinance pandas requests beautifulsoup4 plotly
  ```

## Usage

### Steps to Run
1. **Stock Data Retrieval**  
   Update the `ticker` variable in the script with the desired company's ticker symbol (e.g., `AAPL` for Apple or `TSLA` for Tesla). This will fetch the company's historical stock price data using the `yfinance` library.

2. **Revenue Data Scraping**  
   - If the Macrotrends website allows access, you can directly provide the URL to the `webscraping` function.
   - If access is blocked, download the webpage's source code (right-click on the webpage, select "Save Page As"), and update the `url` variable in the script to point to the saved HTML file.

3. **Run the Script**  
   Execute the script to generate an interactive graph displaying the company's stock prices and quarterly revenue data.

### Example
The default configuration is set to retrieve data for Tesla (TSLA). To test this:
1. Update the `url` variable to the path of the provided HTML snippet for Tesla's revenue data.
2. Run the script.

### Customization
- To analyze a different company, update the following:
  - Change the `ticker` variable to the desired company's ticker symbol.
  - Provide the URL or downloaded HTML file corresponding to the company's quarterly revenue data from Macrotrends.

### Example Code
```python
ticker = "AAPL"  # Replace with desired ticker symbol
url = "<path_to_saved_html>"  # Replace with the path to the downloaded HTML file
data = extract_data(ticker)
revenue = webscraping(url)
make_graph(data, revenue, ticker)
```

### Testing
- To test the script, an HTML snippet containing Tesla's revenue data has been included. Update the `url` variable with the path to this snippet and run the script.

## File Structure
- **main.py**: The main script containing the functions for stock data retrieval, revenue scraping, and graph generation.
- **HTML Snippet**: A sample HTML file containing Tesla's revenue data for testing the `webscraping` function.

## Notes
1. If access to the Macrotrends website is blocked, save the webpage locally and provide its path in the `url` variable.
2. Ensure the downloaded HTML file is up-to-date to maintain accurate data.

## Author
This project was developed by **Ruhika Joshi**.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contributions
Contributions are welcome! If you find a bug or have a suggestion, feel free to open an issue or submit a pull request.
