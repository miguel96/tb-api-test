---
method: POST
---

# Login

**Endpoint:** {{apiRoute}}/authorize/email/login

To start using the Tweet Binder API, login is required. We will provide one user and password, so if you do not have one, contact us now. After logging in you will receive a user token that will be the one you will use to make requests to the API.

{
	"email": "{{email}}",
	"password": "{{password}}"
}

