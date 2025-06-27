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
- 🔐 Authenticate securely via Access Token

---

## 🔐 Authentication

All endpoints require **OAuth 2.0 Bearer Token** authentication.

### Step 1: Request an Access Token


## Endpoints

### GET /pets
Retrieve a list of available pets for adoption.

Request 
```
GET /pets?species=dog&page=1
Host: api.pawfectpets.com
Authorization: Bearer {access_token}

```
Response
```
{
  "data": [
    {
      "id": "pet_101",
      "name": "Bella",
      "species": "dog",
      "breed": "Labrador Retriever",
      "age": 2,
      "available": true
    },
    {
      "id": "pet_102",
      "name": "Milo",
      "species": "dog",
      "breed": "Beagle",
      "age": 4,
      "available": true
    }
  ],
  "page": 1,
  "total_pages": 5
}

```


## Status Codes

| HTT Code | Error |    Messaage | 
| -------- | ------- | -----------| 
| 400      | UNAUTHORISED | Request body is missing required fields| 
| 401      | INVALID     |Access token is missing or expired| 
| 500     | SERVER ERROR    |Something went wrong with our servers| 

