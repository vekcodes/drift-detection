# Marketing Tools Scraper API

A comprehensive API that detects 400+ marketing tools, analytics platforms, and integrations from any website.

## 🚀 Quick Deploy to Vercel

1. Clone or upload this project
2. Run `vercel` in the project directory
3. Your API is live!

## 📡 API Endpoints

### Scrape Marketing Tools
```
GET /api/scrape?url=https://example.com
```

### Get API Info
```
GET /api/info
```

## 📊 Categories Detected

| Category | Examples |
|----------|----------|
| **Chatbots** | Intercom, Drift, Zendesk, Crisp, Tawk.to |
| **Analytics** | Google Analytics, Mixpanel, Amplitude, Heap |
| **Heatmaps** | Hotjar, Microsoft Clarity, Crazy Egg |
| **A/B Testing** | Optimizely, VWO, Google Optimize |
| **Advertising** | Facebook Pixel, Google Ads, LinkedIn |
| **Email Marketing** | Mailchimp, Klaviyo, ActiveCampaign |
| **CRM & Sales** | HubSpot, Salesforce, Pipedrive |
| **Marketing Automation** | Marketo, Pardot, Eloqua |
| **CDP** | Segment, mParticle, Tealium |
| **Push Notifications** | OneSignal, PushEngage, WebEngage |
| **Surveys** | Typeform, SurveyMonkey, Qualtrics |
| **Social Proof** | Trustpilot, Yotpo, Judge.me |
| **Popups** | OptinMonster, Sumo, Privy |
| **Customer Success** | Pendo, WalkMe, Appcues |
| **Payments** | Stripe, PayPal, Klarna |
| **E-commerce** | Shopify, WooCommerce, BigCommerce |
| **CMS** | WordPress, Webflow, Wix |
| **Video** | YouTube, Vimeo, Wistia |
| **Affiliate** | ShareASale, Impact, Rakuten |
| **Scheduling** | Calendly, Cal.com, Chili Piper |
| **Customer Support** | Zendesk, Freshdesk, Help Scout |
| **SEO & Performance** | Cloudflare, Fastly, Akamai |
| **Accessibility** | UserWay, accessiBe, AudioEye |
| **Consent & Privacy** | OneTrust, CookieBot, TrustArc |
| **Translation** | Weglot, Google Translate |
| **Forms** | Typeform, JotForm, HubSpot Forms |

## 📝 Example Response

```json
{
  "success": true,
  "url": "https://example.com",
  "meta": {
    "title": "Example Website",
    "description": "Website description"
  },
  "summary": {
    "total_tools": 12,
    "categories_found": ["analytics", "chatbots", "advertising"],
    "tools_by_category": {
      "analytics": ["Google Analytics 4", "Mixpanel"],
      "chatbots": ["Intercom"],
      "advertising": ["Facebook Pixel", "Google Ads"]
    }
  },
  "detected_tools": {
    "analytics": [
      {
        "name": "Google Analytics 4",
        "matched_pattern": "gtag",
        "confidence": "high"
      }
    ]
  },
  "scripts": ["https://www.googletagmanager.com/gtag/js?id=G-XXX"],
  "html_length": 125000,
  "analysis_timestamp": "2024-01-15T10:30:00Z"
}
```

## 🛠 Local Development

```bash
# Test locally with Python
python -m http.server 3000

# Or use Vercel dev
vercel dev
```

## 📁 Project Structure

```
├── api/
│   └── scrape.py      # Main API handler
├── vercel.json        # Vercel configuration
├── requirements.txt   # Dependencies (none needed)
└── README.md          # This file
```

## ⚡ Features

- **400+ tools detected** across 26 categories
- **Confidence scoring** (high/medium based on multiple pattern matches)
- **No dependencies** - uses Python standard library only
- **Fast response** - typically under 3 seconds
- **CORS enabled** - use from any frontend

## 🔒 Notes

- The scraper uses a standard browser User-Agent
- SSL certificate verification is disabled for broad compatibility
- Response is limited to prevent timeout issues
- Some SPAs may not show all tools (they load dynamically)

## 📄 License

MIT
"# drift-detection" 
