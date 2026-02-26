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
base_url = "https://litellm.example.com"
env_key = "LITELLM_API_KEY"
wire_api = "responses"
```
> $HOME/.codex/config.toml

## gemini

```bash
export GOOGLE_GEMINI_BASE_URL="https://litellm.example.com"
export GEMINI_API_KEY="sk-1234"
export GEMINI_MODEL=gemini-2.5-pro

npm install -g @ai-codespark/gemini-cli@latest
```

```json
{
  "selectedAuthType": "gemini-api-key",
  "theme": "ANSI"
}
```
> $HOME/.gemini/settings.json

## gen

```bash
export SILICONFLOW_BASE_URL="https://litellm.example.com"
export SILICONFLOW_API_KEY="sk-1234"
export GEMINI_MODEL=gemini-2.5-pro

npm install -g @gen-cli/gen-cli@latest
```

```json
{
  "selectedAuthType": "siliconflow-api-key"
}
```
> $HOME/.gen-cli/settings.json

## opencode

```bash
BUN_INSTALL="$HOME/.bun"
PATH="$BUN_INSTALL/bin:$PATH"
XDG_DATA_HOME="$HOME/.local/share"
XDG_CACHE_HOME="$HOME/.cache"
XDG_CONFIG_HOME="$HOME/.config"
XDG_STATE_HOME="$HOME/.local/state"

mkdir -p \
    $HOME/.local/share/opencode/bin \
    $HOME/.local/share/opencode/log \
    $HOME/.cache/opencode \
    $HOME/.config/opencode \
    $HOME/.local/state/opencode

bun install -g @ai-sdk/openai-compatible && \
bun install -g opencode-ai

mkdir -p /tmp/test-opencode && \
    cd /tmp/test-opencode && \
    git init && \
    (echo "hello" | opencode "$PWD" > /tmp/opencode.log 2>&1 &) && \
    OPENCODE_PID=$! && \
    sleep 5 && \
    kill $OPENCODE_PID 2>/dev/null || true && \
    rm -rf /tmp/test-opencode

echo "export TERM=xterm-256color" >> /home/$NAME/.bashrc
```

```json
{
  "$schema": "https://opencode.ai/config.json",
  "model": "litellm/ollama-kimi-k2.5",
  "provider": {
    "litellm": {
      "npm": "@ai-sdk/openai-compatible",
      "name": "LiteLLM",
      "options": {
        "baseURL": "https://litellm.example.com",
        "apiKey": "sk-1234"
      },
      "models": {
        "ollama-kimi-k2.5": {
          "name": "Ollama Kimi K2.5"
        }
      }
    }
  }
}
```
> $HOME/.config/opencode/opencode.jsonc

## qwen

```bash
export OPENAI_BASE_URL="https://litellm.example.com"
export OPENAI_API_KEY="sk-1234"
export OPENAI_MODEL="gemini-2.5-pro"

npm install -g @qwen-code/qwen-code@latest
```

```json
{
  "selectedAuthType": "openai"
}
```
> $HOME/.qwen/settings.json

## trae

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
      "base_url": "https://litellm.example.com",
      "model": "gemini-2.5-pro",
      "max_tokens": 120000,
      "temperature": 0.5,
      "top_p": 1,
      "max_retries": 10
    }
  }
}
```
> trae_config.json
