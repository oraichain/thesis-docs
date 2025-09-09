## POST /api/v1/integration/conversations

```json
"x-codeSamples":[
  {
    "lang": "bash",
    "label": "Create new conversation",
    "source": "curl -X POST 'https://app-be.thesis.io/api/v1/integration/conversations' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN' \\\n  -H 'Content-Type: application/json' \\\n  -d '{\n    \"initial_user_msg\": \"Whats the new DeFi meta recently that I can ape in?\",\n    \"research_mode\": \"deep_research\",\n    \"system_prompt\": \"You are a DeFi gigachad who is always ahead of the new DeFi meta.\"\n  }'"
  },
  {
    "lang": "python",
    "label": "Create new conversation",
    "source": "import requests\n\nurl = 'https://app-be.thesis.io/api/v1/integration/conversations'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n}\ndata = {\n    'initial_user_msg': 'Whats the new DeFi meta recently that I can ape in?',\n    'research_mode': 'deep_research',\n    'system_prompt': 'You are a DeFi gigachad who is always ahead of the new DeFi meta.'\n}\n\nresponse = requests.post(url, headers=headers, json=data)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Create new conversation",
    "source": "const response = await fetch('https://app-be.thesis.io/api/v1/integration/conversations', {\n  method: 'POST',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n  },\n  body: JSON.stringify({\n    initial_user_msg: 'What\\'s the new DeFi meta recently that I can ape in?',\n    research_mode: 'deep_research',\n    space_id: 123,\n    system_prompt: 'You are a DeFi gigachad who\\'s always ahead of the new DeFi meta.'\n  })\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## GET /api/v1/integration/conversations/{conversation_id}

```json
"x-codeSamples":[
  {
    "lang": "bash",
    "label": "Get conversation details",
    "source": "curl -X GET 'https://app-be.thesis.io/api/v1/integration/conversations/conv_abc123def456' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN'"
  },
  {
    "lang": "python",
    "label": "Get conversation details",
    "source": "import requests\n\nconversation_id = 'conv_abc123def456'\nurl = f'https://app-be.thesis.io/api/v1/integration/conversations/{conversation_id}'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n}\n\nresponse = requests.get(url, headers=headers)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Get conversation details",
    "source": "const conversationId = 'conv_abc123def456';\nconst response = await fetch(`https://app-be.thesis.io/api/v1/integration/conversations/${conversationId}`, {\n  method: 'GET',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n  }\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## POST /api/v1/integration/conversations/join-conversation

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Join existing conversation",
    "source": "curl -X POST 'https://app-be.thesis.io/api/v1/integration/conversations/join-conversation' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN' \\\n  -H 'Content-Type: application/json' \\\n  -d '{\n    \"conversation_id\": \"conv_abc123def456\",\n    \"system_prompt\": \"Continue as an expert software architect\",\n    \"user_prompt\": \"Please review the code we discussed earlier\",\n    \"research_mode\": \"deep_research\"\n  }'"
  },
  {
    "lang": "python",
    "label": "Join existing conversation",
    "source": "import requests\n\nurl = 'https://app-be.thesis.io/api/v1/integration/conversations/join-conversation'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n}\ndata = {\n    'conversation_id': 'conv_abc123def456',\n    'system_prompt': 'Continue as an expert software architect',\n    'user_prompt': 'Please review the code we discussed earlier',\n    'research_mode': 'deep_research'\n}\n\nresponse = requests.post(url, headers=headers, json=data)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Join existing conversation",
    "source": "const response = await fetch('https://app-be.thesis.io/api/v1/integration/conversations/join-conversation', {\n  method: 'POST',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n  },\n  body: JSON.stringify({\n    conversation_id: 'conv_abc123def456',\n    system_prompt: 'Continue as an expert software architect',\n    user_prompt: 'Please review the code we discussed earlier',\n    research_mode: 'deep_research'\n  })\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## GET /api/v1/integration/spaces

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Get list of spaces",
    "source": "curl -X GET 'https://app-be.thesis.io/api/v1/integration/spaces?offset=0&limit=10&title=AI%20Research' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN'"
  },
  {
    "lang": "python",
    "label": "Get list of spaces",
    "source": "import requests\n\nurl = 'https://app-be.thesis.io/api/v1/integration/spaces'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n}\nparams = {\n    'offset': 0,\n    'limit': 10,\n    'title': 'AI Research'\n}\n\nresponse = requests.get(url, headers=headers, params=params)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Get list of spaces",
    "source": "const params = new URLSearchParams({\n  offset: '0',\n  limit: '10',\n  title: 'AI Research'\n});\n\nconst response = await fetch(`https://app-be.thesis.io/api/v1/integration/spaces?${params}`, {\n  method: 'GET',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n  }\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## GET /api/v1/integration/spaces/{space_id}

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Get space details",
    "source": "curl -X GET 'https://app-be.thesis.io/api/v1/integration/spaces/space_123' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN'"
  },
  {
    "lang": "python",
    "label": "Get space details",
    "source": "import requests\n\nspace_id = 'space_123'\nurl = f'https://app-be.thesis.io/api/v1/integration/spaces/{space_id}'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n}\n\nresponse = requests.get(url, headers=headers)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Get space details",
    "source": "const spaceId = 'space_123';\nconst response = await fetch(`https://app-be.thesis.io/api/v1/integration/spaces/${spaceId}`, {\n  method: 'GET',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n  }\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## GET /api/v1/integration/spaces/{space_id}/sections

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Get space sections",
    "source": "curl -X GET 'https://app-be.thesis.io/api/v1/integration/spaces/space_123/sections' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN'"
  },
  {
    "lang": "python",
    "label": "Get space sections",
    "source": "import requests\n\nspace_id = 'space_123'\nurl = f'https://app-be.thesis.io/api/v1/integration/spaces/{space_id}/sections'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n}\n\nresponse = requests.get(url, headers=headers)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Get space sections",
    "source": "const spaceId = 'space_123';\nconst response = await fetch(`https://app-be.thesis.io/api/v1/integration/spaces/${spaceId}/sections`, {\n  method: 'GET',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN'\n  }\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## POST /api/v1/integration/chat_researchs

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Create chat conversation",
    "source": "curl -X POST 'https://app-be.thesis.io/api/v1/integration/chat_researchs' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN' \\\n  -H 'Content-Type: application/json' \\\n  -d '{\n    \"initial_user_msg\": \"Lets have a casual conversation about DeFi\",\n    \"system_prompt\": \"You are a friendly AI assistant who explains complex topics simply\"\n  }'"
  },
  {
    "lang": "python",
    "label": "Create chat conversation",
    "source": "import requests\n\nurl = 'https://app-be.thesis.io/api/v1/integration/chat_researchs'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n}\ndata = {\n    'initial_user_msg': 'Lets have a casual conversation about DeFi',\n    'system_prompt': 'You are a friendly AI assistant who explains complex topics simply'\n}\n\nresponse = requests.post(url, headers=headers, json=data)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Create chat conversation",
    "source": "const response = await fetch('https://app-be.thesis.io/api/v1/integration/chat_researchs', {\n  method: 'POST',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n  },\n  body: JSON.stringify({\n    initial_user_msg: 'Lets have a casual conversation about DeFi',\n    system_prompt: 'You are a friendly AI assistant who explains complex topics simply'\n  })\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

## POST /api/v1/integration/deep_researchs

```json
"x-codeSamples": [
  {
    "lang": "bash",
    "label": "Create deep research conversation",
    "source": "curl -X POST 'https://app-be.thesis.io/api/v1/integration/deep_researchs' \\\n  -H 'Authorization: Bearer YOUR_SPACE_API_TOKEN' \\\n  -H 'Content-Type: application/json' \\\n  -d '{\n    \"initial_user_msg\": \"Research the latest developments in DeFi\",\n    \"system_prompt\": \"You are a thorough DeFi researcher who provides comprehensive analysis with citations\"\n  }'"
  },
  {
    "lang": "python",
    "label": "Create deep research conversation",
    "source": "import requests\n\nurl = 'https://app-be.thesis.io/api/v1/integration/deep_researchs'\nheaders = {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n}\ndata = {\n    'initial_user_msg': 'Research the latest developments in DeFi',\n    'system_prompt': 'You are a thorough DeFi researcher who provides comprehensive analysis with citations'\n}\n\nresponse = requests.post(url, headers=headers, json=data)\nprint(response.json())"
  },
  {
    "lang": "typescript",
    "label": "Create deep research conversation",
    "source": "const response = await fetch('https://app-be.thesis.io/api/v1/integration/deep_researchs', {\n  method: 'POST',\n  headers: {\n    'Authorization': 'Bearer YOUR_SPACE_API_TOKEN',\n    'Content-Type': 'application/json'\n  },\n  body: JSON.stringify({\n    initial_user_msg: 'Research the latest developments in DeFi',\n    system_prompt: 'You are a thorough DeFi researcher who provides comprehensive analysis with citations'\n  })\n});\n\nconst data = await response.json();\nconsole.log(data);"
  }
]
```

Fill the above x-codeSamples with their corresponding endpoints into openapi.json. The endpoints must match the endpoints in openapi.json.
