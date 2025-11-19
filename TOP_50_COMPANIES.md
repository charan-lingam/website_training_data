# Top 50 Most Valuable Global Companies 2025

## Collection Status: 0/50 (0%)

## Top 50 Companies List with Websites

### Rank | Company | Website | Country | Market Cap | Status |
---|---|---|---|---|---
1 | Apple | https://www.apple.com | USA | $3.5T | Pending
2 | Microsoft | https://www.microsoft.com | USA | $3.4T | Pending
3 | Nvidia | https://www.nvidia.com | USA | $3.3T | Pending
4 | Alphabet (Google) | https://www.google.com | USA | $2.2T | Pending
5 | Amazon | https://www.amazon.com | USA | $2.1T | Pending
6 | Meta Platforms | https://www.meta.com | USA | $1.8T | Pending
7 | Saudi Aramco | https://www.aramco.com | Saudi Arabia | $1.8T | Pending
8 | Tesla | https://www.tesla.com | USA | $1.1T | Pending
9 | Broadcom | https://www.broadcom.com | USA | $1.1T | Pending
10 | TSMC | https://www.tsmc.com | Taiwan | $1.1T | Pending
11 | Berkshire Hathaway | https://www.berkshirehathaway.com | USA | $1.1T | Pending
12 | JPMorgan Chase | https://www.jpmorganchase.com | USA | $0.7T | Pending
13 | Visa | https://www.visa.com | USA | $0.7T | Pending
14 | Eli Lilly | https://www.lilly.com | USA | $0.7T | Pending
15 | Walmart | https://www.walmart.com | USA | $0.6T | Pending
16 | ExxonMobil | https://www.exxonmobil.com | USA | $0.5T | Pending
17 | UnitedHealth | https://www.unitedhealthgroup.com | USA | $0.5T | Pending
18 | Johnson & Johnson | https://www.jnj.com | USA | $0.5T | Pending
19 | Mastercard | https://www.mastercard.com | USA | $0.5T | Pending
20 | Procter & Gamble | https://www.pg.com | USA | $0.4T | Pending
21 | Oracle | https://www.oracle.com | USA | $0.4T | Pending
22 | Chevron | https://www.chevron.com | USA | $0.4T | Pending
23 | Coca-Cola | https://www.coca-cola.com | USA | $0.3T | Pending
24 | HSBC | https://www.hsbc.com | UK | $0.3T | Pending
25 | Shell | https://www.shell.com | UK | $0.3T | Pending
26 | Bank of China | https://www.bankofchina.com | China | $0.3T | Pending
27 | Taiwan Semiconductor | https://www.tsmc.com | Taiwan | $0.3T | Pending
28 | AMD | https://www.amd.com | USA | $0.3T | Pending
29 | Accenture | https://www.accenture.com | Ireland | $0.3T | Pending
30 | Saudi National Bank | https://www.snb.com.sa | Saudi Arabia | $0.2T | Pending
31 | Nike | https://www.nike.com | USA | $0.2T | Pending
32 | McDonald's | https://www.mcdonalds.com | USA | $0.2T | Pending
33 | Wells Fargo | https://www.wellsfargo.com | USA | $0.2T | Pending
34 | Bank of America | https://www.bankofamerica.com | USA | $0.2T | Pending
35 | Goldman Sachs | https://www.goldmansachs.com | USA | $0.2T | Pending
36 | Nestle | https://www.nestle.com | Switzerland | $0.2T | Pending
37 | IBM | https://www.ibm.com | USA | $0.2T | Pending
38 | Intel | https://www.intel.com | USA | $0.2T | Pending
39 | Costco | https://www.costco.com | USA | $0.2T | Pending
40 | Samsung Electronics | https://www.samsung.com | South Korea | $0.2T | Pending
41 | Toyota Motor | https://www.toyota.com | Japan | $0.2T | Pending
42 | Volkswagen | https://www.volkswagen.com | Germany | $0.2T | Pending
43 | Ping An Insurance | https://www.pingan.com | China | $0.2T | Pending
44 | Alibaba | https://www.alibaba.com | China | $0.2T | Pending
45 | Tencent | https://www.tencent.com | China | $0.2T | Pending
46 | ICBC | https://www.icbc.com.cn | China | $0.2T | Pending
47 | Agricultural Bank of China | https://www.abchina.com | China | $0.2T | Pending
48 | Industrial and Commercial Bank | https://www.icbc.com.cn | China | $0.2T | Pending
49 | China National Petroleum | https://www.cnpc.com.cn | China | $0.2T | Pending
50 | State Grid Corporation | https://www.sgcc.com.cn | China | $0.2T | Pending

## How to Collect HTML/CSS Code

### Method 1: Using Browser Developer Tools (Manual)
1. Open the company website in your browser
2. Press `F12` or right-click → "Inspect" to open Developer Tools
3. Go to the "Elements" or "Inspector" tab
4. Right-click on the `<html>` tag → "Copy" → "Copy Element" or "Copy Outer HTML"
5. Save the HTML in a file named `index.html`
6. For CSS:
   - Look for `<link>` tags in `<head>` section
   - Right-click each CSS file → "Open Link in New Tab"
   - Copy the content and save to `styles.css`

### Method 2: Using Wget (Command Line)
```bash
cd companies/Apple
wget -p -k https://www.apple.com -O index.html
```

### Method 3: Using Curl (Command Line)
```bash
curl -o index.html https://www.apple.com
curl -o styles.css https://www.apple.com/path/to/styles.css
```

### Method 4: Using Python (Automated)
```python
import requests
from bs4 import BeautifulSoup
import os

def scrape_website(url, company_name):
    # Create company folder
    os.makedirs(f"companies/{company_name}", exist_ok=True)
    
    # Get HTML
    response = requests.get(url)
    with open(f"companies/{company_name}/index.html", "w") as f:
        f.write(response.text)
    
    # Extract and save CSS
    soup = BeautifulSoup(response.text, 'html.parser')
    css_files = soup.find_all('link', {'rel': 'stylesheet'})
    
    for idx, css in enumerate(css_files):
        css_url = css.get('href')
        if css_url:
            # Handle relative URLs
            if not css_url.startswith('http'):
                css_url = url.rstrip('/') + '/' + css_url.lstrip('/')
            
            try:
                css_response = requests.get(css_url)
                with open(f"companies/{company_name}/styles_{idx}.css", "w") as f:
                    f.write(css_response.text)
            except:
                pass

# Example usage
scrape_website('https://www.apple.com', 'Apple')
```

## File Structure for Each Company

```
companies/
├── Apple/
│   ├── index.html        # Main HTML file
│   ├── styles.css        # Combined or primary CSS
│   ├── styles_1.css      # Additional CSS files if needed
│   └── metadata.json     # Collection info
├── Microsoft/
│   ├── index.html
│   ├── styles.css
│   └── metadata.json
└── ... [48 more companies]
```

## Metadata Template (metadata.json)

```json
{
  "company_name": "Apple",
  "official_url": "https://www.apple.com",
  "collection_date": "2025-11-19",
  "collection_method": "automated_scraping",
  "verified": true,
  "https_valid": true,
  "response_code": 200,
  "html_file": "index.html",
  "css_files": ["styles.css", "styles_1.css"],
  "html_size_bytes": 123456,
  "total_css_size_bytes": 456789,
  "collection_duration_seconds": 5.2,
  "notes": "Successfully collected homepage HTML and CSS"
}
```

## Progress Tracking

- **Target**: 50 companies
- **Collected**: 0 companies (0%)
- **In Progress**: 0 companies
- **Failed**: 0 companies
- **Last Updated**: November 19, 2025

## Important Notes

1. **Respect robots.txt**: Check if websites allow scraping
2. **Terms of Service**: Verify TOS allows archival
3. **Legal Notice**: This data is for educational purposes only
4. **Rate Limiting**: Don't overwhelm servers - add delays between requests
5. **User-Agent**: Identify your scraper properly
6. **JavaScript**: Some websites may need Puppeteer/Selenium for full rendering

## Useful Tools

- [Puppeteer](https://pptr.dev/) - Headless browser automation
- [Selenium](https://selenium.dev/) - Browser automation
- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) - HTML/XML parsing
- [Requests](https://requests.readthedocs.io/) - HTTP library
- [Wget](https://www.gnu.org/software/wget/) - Download utility
- [Curl](https://curl.se/) - Data transfer utility

## Next Steps

1. ✅ List created
2. ⏳ Begin collecting from Top 1: Apple
3. ⏳ Collect from companies 2-50 sequentially
4. ⏳ Verify all HTML/CSS files
5. ⏳ Create metadata for each company
6. ⏳ Final validation and commit

---

**Last Updated**: November 19, 2025
**Status**: Ready for collection
**Contact**: Open an issue for questions
