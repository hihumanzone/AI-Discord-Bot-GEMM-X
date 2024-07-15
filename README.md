# AI Discord Bot (GEMM-X)

GEMM-X Discord Bot is a versatile and intelligent Discord assistant leveraging cutting-edge AI technologies from multiple providers. This bot can engage in natural language conversation, generate images, create music, produce speech, and much more, making it an all-in-one solution for your server.

## Features

- **Image Generation:** Generates images based on user prompts using various models.
- **Speech Generation:** Converts text to speech in multiple languages.
- **Music Generation:** Creates music based on textual prompts.
- **Custom Personalities:** Allows users and servers to define custom personality settings.
- **Advanced Interaction:** Offers comprehensive user and server settings, including chat history management and response formatting.

## Getting Started

### Prerequisites

- Node.js (v14 or later)
- Discord Bot account & token ([create a bot on Discord Developer Portal](https://discord.com/developers/applications))

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/hihumanzone/AI-Discord-Bot
    cd AI-Discord-Bot
    ```

2. Install dependencies:

    ```sh
    npm install openai @google/generative-ai url cohere-ai axios cheerio discord.js dotenv eventsource fs node-fetch sharp pdf-parse youtube-transcript node-os-utils ws
    ```

3. Set up environment variables:

    Create a `.env` file in the root directory and add your Discord bot token and API keys for the various providers:

    ```env
    DISCORD_BOT_TOKEN=your_discord_bot_token

    # for prompt enhancer..
    OPENAI_BASE_URL=https://api.openai.com/v1
    # https://api.groq.com/openai/v1
    # for groq ⤴️
    OPENAI_API_KEY=your_openai_api_key
    
    OPENAI_GROQ_API_KEY=your_openai_groq_api_key
    OPENAI_TOGETHER_API_KEY=your_openai_together_api_key
    OPENAI_OPENROUTER_API_KEY=your_openai_openrouter_api_key
    OPENAI_KRAKENAI_API_KEY=your_openai_krakenai_api_key
    
    GOOGLE_API_KEY=your_google_gemini_api_key
    COHERE_API_KEY=your_cohere_api_key
    ```

4. Configure the bot:

    Edit the `config.json` file to modify settings as per your preferences.

5. Start the bot:

    ```sh
    npm start
    ```

## Commands

### Image Generation
- `/imagine [prompt] [model] [resolution]`: Generate an image using a selected model and resolution.

### Chat Management
- `/respond_to_all`: Enable the bot to respond to all messages in the current channel.
- `/clear_memory`: Clear the conversation history.
- `/settings`: Open user settings.
- `/server_settings`: Open server settings.

### Speech & Music Generation
- `/speech [language] [prompt]`: Generate speech from text in the specified language.
- `/music [prompt]`: Generate music based on a prompt.

### Admin Commands
- `/blacklist [user]`: Blacklist a user from using interactions.
- `/whitelist [user]`: Remove a user from the blacklist.
- `/status`: Display bot's CPU and RAM usage in detail.

## Configuration 

### `config.json`

Contains various settings for the bot:

- **defaultResponseFormat:** The default response format (`embedded` or `normal`).
- **hexColour:** The default hex color for embeds.
- **defaultPromptEnhancerPreference:** Whether prompt enhancement is enabled by default.
- **defaultImgModel:** The default model for image generation.
- **defaultTextModel:** The default model for text generation.
- **defaultUrlReading:** Default URL reading preference (`ON` or `OFF`).
- **workInDMs:** Whether the bot should respond in DMs (`true` or `false`).
- **shouldDisplayPersonalityButtons:** Whether to display personality buttons (`true` or `false`).
- **shouldDisplayTextModelButton:** Whether to display text model selection button (`true` or `false`).
- **SEND_RETRY_ERRORS_TO_DISCORD:** Whether to send retry errors to Discord channel (`true` or `false`).
- **activities:** An array of activities for the bot to display.

### NSFW Word Filtering (`nsfwWords.json`)

Contains an array of words that should be filtered from prompts.

## Community & Support

- Join the [Discord Community](https://discord.com/invite/Gxpw7XF3Mj) for support, updates, and discussions.

### API Key Providers

- **Groq:** [Get API Key](https://console.groq.com/keys)
- **Together AI:** [Get API Key](https://api.together.xyz/settings/api-keys)
- **OpenRouter:** [Get API Key](https://openrouter.ai/keys)
- **Kraken AI:** [Join Discord](https://discord.gg/krakenai) to get access
- **Google:** [Get API Key](https://aistudio.google.com/app/apikey)
- **Cohere:** [Get API Key](https://dashboard.cohere.com/api-keys)

### Models

1. Cohere Command R Plus (Web)
2. Groq Llama 3 70B
3. Groq Llama 3 8B
4. Groq Gemma 2 9B
5. Together Qwen 2 72B
6. Together Llama 3 70B
7. Together DBRX
8. OpenRouter Phi-3 Medium 128K
9. OpenRouter Gemma 2 9B
10. OpenRouter Llama 3 8B
11. KrakenAI Gemini 1.5 Flash
12. KrakenAI Claude 3.5 Sonnet
13. Google Gemini 1.5 Flash
14. Google Gemini 1.5 Pro

> **`NOTE`**: All of them have a free plan and work without a credit card. They don't have a lifetime usage limit, except for `Together AI`, but it provides $25 in credits, which will probably last a long time because they are cheap. All of them, except for `Kraken AI`, appear to have good rate limits. For `Kraken AI`, we get 500 credits per day, which equates to about 25 `Claude 3.5 Sonnet` messages per day.

## Contributions

We welcome contributions! Feel free to fork the repository, create a new branch, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License.

---

Happy Discording with *GEMM-X*!

If you find this bot useful, don't forget to ⭐star the repository!
