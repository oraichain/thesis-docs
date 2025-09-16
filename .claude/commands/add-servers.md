Call the following command:

```bash
jq '.servers = [{"url":"https://app-be.thesis.io", "description": "Production Thesis APIs"}]' api-reference/openapi.json > tmp.json && mv tmp.json api-reference/openapi.json
```