---
Title: Victor Pets API Reference
description: RESTful API documentation for the Victor Pets adoption and veterinary service.
---

# 📘 Victor Pets API – Developer Guide

Welcome to the **Victor Pets API** – your gateway to managing pets and appointments for our virtual pet adoption and veterinary service.

This RESTful API allows partner apps and admin portals to:

- 🐾 Create and manage pet records  
- 📋 View adoption listings  
- 📅 Schedule appointments  
- 🔐 Authenticate securely via OAuth 2.0  

---

## 🔐 Authentication

All endpoints require **OAuth 2.0 Bearer Token** authentication.

### Step 1: Request an Access Token

**POST** `/oauth/token`

```bash
curl -X POST https://api.victorpets.com/oauth/token \
  -H "Content-Type: application/json" \
  -d '{
        "client_id": "your_client_id",
        "client_secret": "your_client_secret",
        "grant_type": "client_credentials"
      }'
```
{
  "access_token": "eyJhbGciOiJIUzI1NiIsIn...",
  "token_type": "Bearer",
  "expires_in": 3600
}
