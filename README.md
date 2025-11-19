# Website Training Data Repository

## Overview

This repository collects and organizes HTML and CSS code from the top global companies' websites. The data is intended for machine learning training, web design analysis, and architectural pattern recognition.

## Objective

- Collect HTML/CSS code from the top 500 global companies
- Verify legitimacy of each website
- Organize code in company-specific folders
- Build a comprehensive dataset for web design AI models

## Repository Structure

```
website_training_data/
├── README.md
├── COMPANY_WEBSITES.md
├── companies/
│   ├── Apple/
│   │   ├── index.html
│   │   ├── styles.css
│   │   └── metadata.json
│   ├── Google/
│   │   ├── index.html
│   │   ├── styles.css
│   │   └── metadata.json
│   ├── Microsoft/
│   │   ├── index.html
│   │   ├── styles.css
│   │   └── metadata.json
│   └── [500+ more companies]
└── VERIFICATION_LOG.md
```

## Data Collection Process

### Step 1: Company Identification
- Source: Fortune 500, Global 500, Tech Companies Lists
- Data will be curated from multiple authoritative sources

### Step 2: Website Verification
Before adding any website data, verify:
- ✓ Official domain (check via WHOIS or company official sources)
- ✓ HTTPS security certificate
- ✓ Company registration confirmation
- ✓ Terms of Service compliance

### Step 3: Data Collection
For each verified company:
1. Visit the homepage
2. Extract HTML source
3. Download all CSS files
4. Create company folder: `companies/[CompanyName]/`
5. Save: `index.html` and `styles.css`
6. Document metadata

### Step 4: Organization
- Each company gets its own folder
- Files are named: `index.html`, `styles.css`
- Add `metadata.json` with:
  - Company name
  - URL
  - Collection date
  - File sizes
  - Verification status

## Metadata Template (metadata.json)

```json
{
  "company_name": "Company Name",
  "official_url": "https://www.example.com",
  "collection_date": "YYYY-MM-DD",
  "verified": true,
  "verification_method": "WHOIS + Official Website",
  "html_size_bytes": 12345,
  "css_size_bytes": 5678,
  "total_files": 2,
  "notes": "Collected from homepage"
}
```

## Verification Checklist

- [ ] Company exists in official registry (Fortune 500, Global 500, etc.)
- [ ] Official website URL confirmed
- [ ] HTTPS certificate is valid
- [ ] Website loads without errors
- [ ] No malware/phishing indicators
- [ ] Terms of Service allows archival
- [ ] Content is publicly accessible

## Quality Assurance

- All URLs must be official company domains
- HTML files must be well-formed
- CSS files must be properly linked
- No external CDN links included (download locally)
- Metadata must be complete and accurate
- Regular verification of file integrity

## Contributing Guidelines

1. Create a new branch: `add/company-name`
2. Follow the folder structure exactly
3. Verify website legitimacy before adding
4. Include complete metadata.json
5. Test HTML files for validity
6. Submit pull request with verification evidence

## Current Progress

- Status: Repository initialized
- Companies collected: 0
- Target: 500 companies
- Verification rate: 0%

## Useful Resources

- [Fortune Global 500](https://fortune.com/ranking/global500/)
- [WHOIS Lookup](https://www.whois.net/)
- [SSL Certificate Checker](https://www.sslshopper.com/ssl-certificate-checker.html)
- [HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

## Legal Notice

- Data is collected for educational and research purposes
- All websites are publicly accessible
- Respect robots.txt and Terms of Service
- No sensitive data is included
- Archive created for archival purposes only

## License

MIT License - See LICENSE file for details

## Contact

For questions about this repository, please open an issue.

---

**Last Updated:** November 19, 2025
**Maintained by:** Website Training Data Team
