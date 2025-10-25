# Moonito JavaScript SDK (`moonito-js`)

> Official JavaScript SDK for [Moonito](https://moonito.net) — a smart analytics and visitor filtering platform designed to protect your website from unwanted traffic, bots, and malicious activity while providing deep visitor insights.

[![CDN](https://img.shields.io/badge/CDN-jsDelivr-orange.svg)](https://cdn.jsdelivr.net/gh/moonito-net/lib/analytics.min.js)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Website](https://img.shields.io/badge/Website-moonito.net-blue)](https://moonito.net)

---

## Overview

`moonito-js` is a lightweight JavaScript snippet for integrating your website with the **Moonito Visitor Analytics and Traffic Filtering API**.

**Key Features:**
- **Real-time bot protection** — Block crawlers, scrapers, and malicious bots
- **Smart analytics** — Track genuine visitors with accurate metrics
- **Automatic filtering** — Redirect unwanted traffic instantly
- **Zero configuration** — Just paste one line of code
- **Universal compatibility** — Works with any website or framework

Compatible with **HTML**, **WordPress**, **React**, **Vue**, **Next.js**, **Angular**, and all static/dynamic websites.

---

## Installation

### Step 1: Sign Up and Get Your API Key

1. Go to [Moonito Analytics](https://moonito.net/analytics)
2. Register your domain
3. Choose your security preferences
4. Click **Submit** to get your integration code

### Step 2: Add the Script to Your Website

Copy the script provided in your dashboard and paste it into **every page** (or your master template) just before the closing `</head>` tag:

```html
<script 
  defer 
  data-public-key="YOUR_PUBLIC_KEY" 
  data-blocked-page="https://example.com/blocked" 
  src="https://cdn.jsdelivr.net/gh/moonito-net/lib/analytics.min.js">
</script>
```

---

## Quick Start

### Basic HTML Integration

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Web Application</title>
  
  <!-- Moonito Analytics Integration -->
  <script 
    defer 
    data-public-key="2Q4FnwYy6gaOY70F9GVxMNxxxxxxxxxx" 
    data-blocked-page="https://google.com" 
    src="https://cdn.jsdelivr.net/gh/moonito-net/lib/analytics.min.js">
  </script>
</head>
<body>
  <main>
    <h1>Welcome to My Website</h1>
    <p>This is an example page with Moonito Analytics protection enabled.</p>
  </main>
</body>
</html>
```

### WordPress Integration

Add the script to your theme's `header.php` file before `</head>`, or use a plugin like **Insert Headers and Footers**.

### React/Next.js Integration

Add to your `pages/_document.js` (Next.js) or `public/index.html` (Create React App):

```jsx
// Next.js: pages/_document.js
import { Html, Head, Main, NextScript } from 'next/document'

export default function Document() {
  return (
    <Html>
      <Head>
        <script 
          defer 
          data-public-key="YOUR_PUBLIC_KEY" 
          data-blocked-page="https://example.com/blocked" 
          src="https://cdn.jsdelivr.net/gh/moonito-net/lib/analytics.min.js">
        </script>
      </Head>
      <body>
        <Main />
        <NextScript />
      </body>
    </Html>
  )
}
```

### Vue.js Integration

Add to your `public/index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <title>Vue App</title>
  
  <!-- Moonito Analytics -->
  <script 
    defer 
    data-public-key="YOUR_PUBLIC_KEY" 
    data-blocked-page="https://example.com/blocked" 
    src="https://cdn.jsdelivr.net/gh/moonito-net/lib/analytics.min.js">
  </script>
</head>
<body>
  <div id="app"></div>
</body>
</html>
```

---

## Configuration Options

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| `data-public-key` | `string` | ✅ Yes | Your Moonito API public key from the dashboard |
| `data-blocked-page` | `string` | ✅ Yes | URL to redirect unwanted visitors (e.g., `https://example.com/blocked`) |
| `defer` | — | Recommended | Loads script asynchronously without blocking page rendering |

---

## How It Works

1. **Script loads** when your page loads (deferred for performance)
2. **Visitor evaluation** happens automatically in the background
3. **Analytics recorded** for legitimate visitors
4. **Unwanted traffic blocked** and redirected to your specified URL
5. **Dashboard updated** with real-time visitor statistics

---

## Testing Your Integration

1. **Install the script** on your website
2. **Visit your website** in a browser
3. **Check the network tab** — You should see a request to Moonito's analytics endpoint
4. **View analytics** at [https://moonito.net/analytics](https://moonito.net/analytics)

---

## Example Use Cases

✅ **E-commerce sites** — Block fake traffic and ad fraud  
✅ **Landing pages** — Get accurate conversion metrics  
✅ **Blogs & content sites** — Filter bot traffic for real engagement data  
✅ **SaaS applications** — Protect signup forms from spam  
✅ **APIs & web apps** — Prevent scraping and abuse  

---

## Performance

- **Lightweight**: ~5KB minified
- **Non-blocking**: Uses `defer` attribute
- **CDN hosted**: Fast global delivery via jsDelivr
- **No dependencies**: Pure JavaScript, no jQuery required

---

## Browser Support

| Browser | Minimum Version |
|---------|----------------|
| Chrome | 60+ |
| Firefox | 60+ |
| Safari | 12+ |
| Edge | 79+ |
| Opera | 47+ |

---

## FAQ

### Q: Does this slow down my website?
**A:** No. The script uses the `defer` attribute, which loads asynchronously without blocking page rendering.

### Q: Can I use this with a Single Page Application (SPA)?
**A:** Yes! It works with React, Vue, Angular, and other SPAs.

### Q: What happens if the script fails to load?
**A:** Your website continues to work normally. The script fails gracefully.

### Q: Where can I see visitor statistics?
**A:** Log in to your [Moonito Analytics Dashboard](https://moonito.net/analytics).

---

## Support

- **Website**: [https://moonito.net](https://moonito.net)
- **Documentation**: [Integration Guide](https://moonito.net/usage-guides/integrate-analytics-with-embedded-code)

---

## License

MIT License © 2025 [Moonito](https://moonito.net)

---

## Keywords

javascript analytics, moonito sdk, visitor filtering, bot protection, traffic analytics, website security, spam prevention, fraud detection, analytics snippet, visitor tracking, real-time analytics, web protection sdk

---

**Moonito — Stop Bad Bots. Start Accurate Web Analytics.**
