Call the following command:

```bash
jq '.servers = [{"url":"https://app-be.thesis.io", "description": "Production API"}]' api-reference/openapi.json > tmp.json && mv tmp.json api-reference/openapi.json
```