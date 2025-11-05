# Site Informant OpenAPI

Official OpenAPI specification for the **[Site Informant](https://siteinformant.com)** public JSON API —  
a simple, developer-friendly interface for website uptime, response time, and SSL expiration data.

---

## 📘 Overview

Site Informant provides affordable uptime and SSL monitoring for websites.  
Our **public JSON API** lets developers, dashboards, and AI tools access live monitoring data for sites that have opted into public visibility.

- **Base URL:** `https://api.siteinformant.com/api/public/`
- **Docs:** [https://siteinformant.com/Developers](https://siteinformant.com/Developers)
- **OpenAPI Spec:** [openapi-public.json](https://api.siteinformant.com/api/public/openapi.json)

---

## 🧠 Example

```bash
GET https://api.siteinformant.com/api/public/status/prudentdev.com
```
```JSON
{
  "domain": "prudentdev.com",
  "uptimePercent": 99.89,
  "isOnline": true,
  "lastCheckUtc": "2025-11-04T07:45:00Z",
  "averageResponseMs": 238,
  "sslExpiresUtc": "2026-01-04T00:00:00Z",
  "sslIssuer": "Let's Encrypt"
}
```
## 💡 Use Cases
Build custom uptime dashboards or client portals

Integrate uptime data into AI agents or chatbots

Automate alerts and reporting pipelines

Enhance DevOps observability systems

## 🛠️ Rate Limits
60 requests / minute

Returns HTTP 429 with Retry-After header when exceeded

Please cache results responsibly (status endpoints ~60s TTL)

## ⚙️ Schema
The openapi-public.json file defines:

/status/{domain} — site uptime & SSL data

/plans — current pricing tiers

/example — sample payload for crawlers/tests

You can import this file directly into Postman, Swagger UI, or any OpenAPI-compatible SDK generator.

## 🔗 Related Resources
[Blog announcement: Free Website Uptime API – JSON for Developers and AI Integrations](https://siteinformant.com/blog/free-website-uptime-api)


Dev.to post: [dev.to/saganmarketing](https://dev.to/saganmarketing/free-website-uptime-api-json-for-developers-and-ai-integrations-519m)

Medium article: [medium.com/@saganmarketing.com](https://dev.to/saganmarketing/free-website-uptime-api-json-for-developers-and-ai-integrations-519m)