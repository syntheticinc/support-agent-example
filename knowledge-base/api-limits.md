# Acme API Rate Limits

The Acme REST API enforces a rate limit of **1000 requests per minute** per workspace. Short bursts are allowed up to 100 requests per second.

Responses are paginated at 100 items per page. Exceeding the rate limit returns HTTP 429 with a `Retry-After` header.

The API is available on the Pro and Business plans. The Free plan does not include API access.
