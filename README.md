# 🚀 MCP Perplexity Proxy Server

This Node.js server proxies OpenAI-compatible or MCP-native requests to Perplexity AI's Sonar models with streaming support.

## 🔧 Run locally
```bash
docker-compose up --build
```

## 🔁 Supported APIs
- POST `/v1/chat/completions` (OpenAI-compatible)
- POST `/mcp-stream` (MCP-native)
- GET `/` (Swagger UI)

## ✅ Usage in CLine / Cursor / RooCode
```json
{
  "provider": "openai",
  "api_base": "http://localhost:3000/v1",
  "api_key": "dummy"
}
```

## 🧪 Local Testing
```bash
curl -X POST http://localhost:3000/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{"model":"sonar-reasoning-pro","messages":[{"role":"user","content":"Was ist JSON.stringify?"}]}'
```