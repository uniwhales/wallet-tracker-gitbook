# Errors

Errors use the same envelope as successful responses, with `status` set to `"error"`:

```json
{
  "status": "error",
  "message": "Your API key is not valid. Please check your API key and try again."
}
```

Failed calls do not spend credits.

| HTTP | When                                                                                                                                    | What to do                                                                |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| 400  | A parameter is missing or invalid, e.g. an unknown chain or a malformed address. `message` names the problem.                           | Fix the request.                                                          |
| 402  | The subscription behind the key has expired.                                                                                            | Renew the plan.                                                           |
| 403  | No `X-API-KEY` header, an invalid key, an endpoint your plan does not include, or a trading endpoint while trading via API is disabled. | Check the key and the plan — see [Credits & plans](credits-and-plans.md). |
| 404  | Unknown path.                                                                                                                           | Check the path against the API Reference.                                 |
| 408  | The request took too long, or the client closed the connection first.                                                                   | Retry, ideally with a narrower query.                                     |
| 429  | The plan's credits are spent.                                                                                                           | Wait for the quota to reset or upgrade.                                   |
| 500  | An unexpected server error.                                                                                                             | Retry with backoff; if it persists, contact support.                      |
| 504  | An upstream timed out.                                                                                                                  | Retry with backoff.                                                       |

### Retries

Retry `408`, `500` and `504` with exponential backoff. Do not retry `400`, `402`, `403`, `404` or `429` unchanged — they fail the same way until the request, key or plan changes.
