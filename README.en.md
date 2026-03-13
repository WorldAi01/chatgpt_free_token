<p align="center">
  <a href="https://github.com/WorldAi01/chatgpt_free_token"><img src="./images/logo.png" width="125" height="125" alt="free-chatgpt-api logo"></a>
</p>

<div align="center">

# WorldAi

Use ChatGPT API for free with standard OpenAI format

</div>

<p align="center">
  <a href="./README.md">中文</a> | 
  <strong>English</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/FREE-100%25-green_blue" alt="free">
</p>

> [!NOTE]
> The API endpoint of this project has been updated to `https://worldai.hk`, please be aware!

> [!IMPORTANT]
> Users must use this service in compliance with OpenAI's [Terms of Use](https://openai.com/policies/terms-of-use) and applicable **laws and regulations**. Illegal use is strictly prohibited.
>
> In accordance with the *Interim Measures for the Administration of Generative Artificial Intelligence Services*, do not provide any unregistered generative AI services to the public in mainland China.
>
> This API is for **non-commercial use only**, including learning, research, and scientific testing. Commercial or illegal usage is forbidden; violators shall be held fully responsible.

## Project Introduction

1. Standard OpenAI-compatible API format (also supports native Claude/Gemini request formats).
2. Supports streaming response.
3. Fully compatible with most open-source GPT projects/applications/software.

## Free Usage

1. First, go to [🚀 **Get your free API KEY**](https://worldai.hk). Register to receive free credits, and keep your API KEY safe.
2. API Base URL: `https://worldai.hk` (direct access, no proxy needed).
3. In supported applications, set your API KEY and API Base URL (`BASE_URL`), then you are ready to go.

As the user base grows, we will improve service quality and provide better free services.
If you encounter any problems, please submit an [issue](https://github.com/WorldAi01/chatgpt_free_token/issues), and we will assist you as soon as possible.

### API Features

1. Low latency, high performance, high availability, high concurrency. Direct connection to official API (no reverse engineering, no multi-layer proxies, not Azure).
2. Supports all OpenAI models, including web search, image generation, chat, fine-tuning, vision, GPTs, etc. Over 600+ models supported.
3. GPT-4 priced at only **28%–30%** of official OpenAI price.
   GPT-3.5 series priced at only **14%–20%** of official price.
4. Fully transparent pricing. Model pricing ratios are consistent with or lower than official rates. No hidden markup or price traps.
5. No time limit, pay-as-you-go, usage details visible. Every consumption is clear and transparent.
6. This API is for non-commercial learning, research, and scientific testing only. Do not use it for illegal purposes or provide unregistered generative AI services to the public in mainland China. Violators shall be held fully responsible.

## Supported Applications

> [!NOTE]
> Theoretically supports all GPT applications that allow custom API endpoints. Below are common examples.
>
> For all applications, use API Base URL: `https://worldai.hk`
> Please replace the API prefix in tutorial images with `https://worldai.hk`.

### 1. WorldAi Official Web Client
Official web client provided by WorldAi: [https://worldai.hk/chat](https://worldai.hk/chat)
Supports 600+ AI models, including chat, image generation, video, music.

### 2. ChatGPT Buddy Plugin (uTools)

A plugin for uTools that supports custom models, one‑key invocation, system‑wide quick access, and super panel.
Supports AI chat, image generation, voice dialogue, multi‑API management, multi‑KEY binding, independent chat history for roles, one‑key balance check.
Great desktop tool, but not available on mobile.

[ **View App**](https://u.tools/plugins/detail/ChatGPT.%E5%A5%BD%E5%8F%8B/)

### 3. Open‑Source Chatgpt‑next‑web (ChatGPT‑Midjourney)

> [Open‑Source Chatgpt‑next‑web](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)
> Open‑source web chat tool, chat only.
>
> [Open‑Source ChatGPT‑Midjourney](https://github.com/Licoy/ChatGPT-Midjourney)
> Forked version with Midjourney support.

### 4. Lobe-chat

> [Lobe-chat](https://github.com/lobehub/lobe-chat)
> Open‑source chat application supporting chat, image generation, voice dialogue.

### 5. BotGem

> [BotGem](https://botgem.com/)
> Non‑open‑source tool, supports PC and mobile, simple chat only.

Configuration: API Base URL `https://worldai.hk` + your API KEY.

### 6. ChatBox

> [ChatBox](https://github.com/Bin-Huang/chatbox)
> Supports desktop app and web version. Configure in settings.

Configuration: API Base URL `https://worldai.hk` + your API KEY.

### 7. FastGPT

> [FastGPT](https://github.com/labring/FastGPT)
> Chat application with knowledge base support.

Set host to `https://worldai.hk` during deployment and use your API KEY.

### More Applications

To be updated...

### Official OpenAI Python Library

Set base URL and API KEY when using the official OpenAI Python library.

> [openai-python](https://github.com/openai/openai-python)

Example: append `/v1/` suffix. Upgrade openai library to latest version.

```python
import os
import openai

# optional; defaults to `os.environ['OPENAI_API_KEY']`
openai.api_key = "YOUR_API_KEY"

# all client options can be configured just like the `OpenAI` instantiation counterpart
openai.base_url = "https://worldai.hk/v1/"
openai.default_headers = {"x-foo": "true"}

completion = openai.chat.completions.create(
    model="gpt-4o-mini",
    messages=[
        {
            "role": "user",
            "content": "Hello world!",
        },
    ],
)
print(completion.choices[0].message.content)

# Should output: Hello there! How can I assist you today?
```

### OpenAI Official Node Library

> [openai-node](https://github.com/openai/openai-node)

Using the official `node` library as an example: Note that you need to pass the /v1 suffix.

```js
const { Configuration, OpenAIApi } = require("openai");

const configuration = new Configuration({
  apiKey: "Your apikey",
  basePath: "https://worldai.hk/v1"
});
const openai = new OpenAIApi(configuration);

const chatCompletion = await openai.createChatCompletion({
  model: "gpt-3.5-turbo",
  messages: [{role: "user", content: "Hello world"}],
});

console.log(chatCompletion.data.choices[0].message.content);
```