# OpenCode Config Generator for Pollinations.ai

A simple web-based tool to generate configuration files for OpenCode with Pollinations.ai provider support.

## Features

- **Model Selection**: Choose from 36+ available models on Pollinations.ai
- **Custom Models**: Add your own custom models with custom IDs and names
- **Config Generation**: Generate `opencode.jsonc` with selected models
- **Auth Generation**: Generate `auth.json` with your API key
- **Download Support**: Download both config files directly from the browser
- **Bilingual UI**: Switch between English and Russian languages
- **Select/Deselect All**: Quickly select or deselect all models

## Usage

1. Open `index.html` in your browser
2. Enter your API key (for auth.json generation)
3. Select the models you want to use from the list
4. Click "Generate opencode.jsonc" to create the config file
5. Click "Generate auth.json" to create the authentication file
6. Download the generated files using the "Download" buttons

## Generated Files

### opencode.jsonc
Contains the provider configuration with selected models:
```json
{
  "$schema": "https://opencode.ai/config.json",
  "disabled_providers": [],
  "provider": {
    "pollinations": {
      "name": "Pollinations",
      "npm": "@ai-sdk/openai-compatible",
      "options": {
        "baseURL": "https://gen.pollinations.ai/v1"
      },
      "models": { ... }
    }
  }
}
```

### auth.json
Contains your API key for authentication:
```json
{
  "pollinations": {
    "type": "api",
    "key": "your-api-key-here"
  }
}
```

## Available Models

The tool includes 36 pre-configured models:
- Kimi K2.5 / K2.6
- MiniMax M2.7
- Qwen3 series (Coder, Guard, VL, Plus)
- GPT-5 series (Nano, 5.4, Audio)
- Gemini 2.5/3.0 series
- Claude 4.5/4.6/4.7 series
- Mistral Small/Large 3
- Grok 4.20 (Reasoning/Non-Reasoning)
- And many more...

## Try Online

[CLICK](https://he6ot.github.io/OpenCode-Config-Generator-for-pollinations.ai/)
