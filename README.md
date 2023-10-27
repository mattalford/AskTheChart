## AskTheChart - NinjaTrader 8 Indicator
**Introduction:**
AskTheChart is an experimental AI-powered indicator that showcases the use of a large language model to enhance trading strategies and analysis using agents. Traders can interact with their charts by asking questions such as, 'What is the current trend?' They can give commands like 'Draw horizontal line at the $1500 level,' or instruct the agent to highlight an area on the chart. It's important to note that this is experimental and intended to complement, not replace, traditional trading analysis and strategies. Its main purpose is to demonstrate the potential applications of AI in trading.

**How to Use:**

AskTheChart adds an interactive button 🤖 on the chart toolbar. When clicked, it opens a chat window where you can ask questions or give commands. The AI agent understands your queries and responds accordingly. To configure the indicator, go to the indicator settings and enter the required OpenAI/Azure URL, API key, and Model. You can also set the maximum number of bars allowed for the agent context window.

**URL example:**

```plaintext
OpenAI: https://api.openai.com/v1/chat/completions
Azure OpenAI:https://{name}-east-2.openai.azure.com/openai/deployments/gpt-4/chat/completions?api-version=2023-07-01-preview
```

We utilize ChatGPT functions for tool-switching, requiring the use of one of these Models.
- gpt-3.5-turbo-0613
- gpt-4-0613

```plaintext
0) Indicator settings
URL: https://api.openai.com/v1/chat/completions
API Key: Your OpenAI API key
Model: gpt-4-0613
```

If you are using Azure OpenAI, the model's name should match the one defined in your deployment, and the required model version is 0613
- gpt-4
- gpt-3.5-turbo

```plaintext
0) Indicator settings
URL: https://{name}-east-2.openai.azure.com/openai/deployments/gpt-4/chat/completions?api-version=2023-07-01-preview
API Key: Your OpenAI API key
Model: gpt-4
```

**Cost Implications:**

Please note that using AskTheChart involves making requests to the OpenAI API. These requests are subject to OpenAI's pricing structure, which means that usage of AskTheChart may incur costs. Users are responsible for these costs and should review OpenAI's pricing details before using this indicator.

**Challenges:**

There are numerous tools and libraries available for developing with LLMs. However, integrating them into Ninjascript without relying on DLLs is a significant challenge. Ninjascript employs C# 5.0, which is considered somewhat legacy and lacks many modern features. While it's possible to work around this limitation using compiled assemblies, I opted for an open-source approach to maintain accessibility.

**Change Log:**

```plaintext\n// NT8 AskTheChart by pixel @ nexusfi.com, Version 0.1.0, released 10/19/2023 NT8 8.1.1.7 64-bit
10/22/2023 v0.1.01 - Fix: model variable missing
10/22/2023 v0.1.02 - Removed duplicate declarations
```

I'm eager to discover additional applications for LLMs in trading and explore their use in my own strategies, as well as in others. You can find the discussion [here](https://nexusfi.com/elite-quantitative-genai-llm/60245-askthechart-indicator.html#post)
