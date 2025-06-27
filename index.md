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


## Endpoints

### GET /pets
Retrieve a list of available pets for adoption.

GET /pets?species=dog
Host: api.victorpets.com
Authorization: Bearer {access_token}



## Status Codes

| HTT Code | Error |    Messaage | 
| -------- | ------- | -----------| 
| 400      | UNAUTHORISED | Request body is missing required fields| 
| 401      | INVALID     |Access token is missing or expired| 
| 500     | SERVER ERROR    |Something went wrong with our servers| 

