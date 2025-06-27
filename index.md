---
title: Account Balance API Reference
description: Retrieve real-time balances for JPMorgan accounts.
---

# 📘 Account Balance API – Reference

The **Account Balance API** allows you to retrieve real-time balances for JPMorgan-held accounts. Use it to query current and available balances for domestic and international accounts, useful for treasury dashboards, ERP systems, and finance apps.

---

## 🔗 Endpoint

`GET /v1/accounts/{account_id}/balances`

---

## 🧾 Request

### Path Parameters

| Name         | Type   | Required | Description                            |
|--------------|--------|----------|----------------------------------------|
| `account_id` | string | ✅ Yes   | Unique identifier of the bank account. |

### Query Parameters

| Name          | Type   | Required | Description                                                  |
|---------------|--------|----------|--------------------------------------------------------------|
| `as_of_date`  | string | ❌ No    | Date in `YYYY-MM-DD` format. Defaults to current date.       |
| `currency`    | string | ❌ No    | ISO 4217 currency code (e.g., `USD`, `GBP`). Optional.       |

### Headers

| Header             | Required | Description                              |
|--------------------|----------|------------------------------------------|
| `Authorization`    | ✅ Yes   | `Bearer {access_token}`                  |
| `Content-Type`     | ✅ Yes   | `application/json`                       |
| `x-request-id`     | ❌ No    | Optional ID for request traceability.    |

---

## 📥 Example Request
tested ok
