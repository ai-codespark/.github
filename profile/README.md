## claude-code

```bash
export ANTHROPIC_BASE_URL="http://localhost:4000"
export ANTHROPIC_AUTH_TOKEN="sk-1234"

npm install -g @anthropic-ai/claude-code@latest
```



## codex

```bash
export LITELLM_API_KEY="sk-1234"

npm install -g @openai/codex@native
```

```toml
model = "gemini-2.5-pro"
model_provider = "litellm"

[model_providers.litellm]
name = "LiteLLM"
base_url = "http://localhost:4000/v1"
env_key = "LITELLM_API_KEY"
wire_api = "chat"
```
> cat $HOME/.codex/config.toml



## gemini-cli

```bash
export GOOGLE_GEMINI_BASE_URL="http://localhost:4000"
export GEMINI_API_KEY="sk-1234"

npm install -g @ai-codespark/gemini-cli@latest
```

```json
{
  "selectedAuthType": "gemini-api-key",
  "theme": "ANSI"
}
```
> cat $HOME/.gemini/settings.json



## gen-cli

```bash
export SILICONFLOW_BASE_URL="http://localhost:4000"
export SILICONFLOW_API_KEY="sk-1234"
export GEMINI_MODEL=gemini-2.5-pro

npm install -g @gen-cli/gen-cli@latest
```

```json
{
  "selectedAuthType": "siliconflow-api-key"
}
```
> cat ~/.gen-cli/settings.json



## qwen-code

```bash
export OPENAI_BASE_URL="http://localhost:4000"
export OPENAI_API_KEY="sk-1234"
export OPENAI_MODEL="gemini-2.5-pro"

npm install -g @qwen-code/qwen-code@latest
```

```json
{
  "selectedAuthType": "openai"
}
```
> cat ~/.qwen/settings.json



## trae-agent

```bash
uv venv
uv sync --all-extras
source .venv/bin/activate
```

```json
{
  "default_provider": "openai",
  "max_steps": 20,
  "enable_lakeview": false,
  "model_providers": {
    "openai": {
      "api_key": "sk-1234",
      "base_url": "http://localhost:4000",
      "model": "gemini-2.5-pro",
      "max_tokens": 120000,
      "temperature": 0.5,
      "top_p": 1,
      "max_retries": 10
    }
  }
}
```
> cat trae_config.json
