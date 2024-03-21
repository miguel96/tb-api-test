---
description: All these endpoints are common to all APIs
---

# Basic Endpoints

## Login

This endpoint provides an authorization token needed by the rest of the endpoints. The Postman request will store the token in the environment, you won’t need to add it manually.&#x20;

Use this endpoint to get your API access token by sending your email and password. If you don't have your email/password please contact [APPLY NOW](../../apply-for-the-api.md) for our API and in a few hours you will be able to get your login credentials.

## Check balance

It lets you check your plan's balance. There are some important properties in the response:

* plans.renewDate: Unix time when your plan will be renewed and your balance will reset
* balances: Each item has total and balance. After the plan is renewed the balance property will be set to total.

Every client in Tweet Binder has a **Plan** (subscription) with associated **Balances**. You can check your total balances info and how much have you consumed using this endpoint. Balances show the number of reports or profiles remaining in the current month.

##
