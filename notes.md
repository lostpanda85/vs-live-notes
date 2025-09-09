# VS Live! Notes

## Monday

### Dev Ops Agent (CoPilot)

#### Local

[Repository](https://github.com/lostpanda85/vs-live-lab)

##### Local App

* ASP.Net Blazor Front End (locally/kestrel)
* Aspire-enabled
  * Framework for C#
  * Better Refresh (F5) Experience
  * Vector DB
  * AI-Chat Web App
    * Ollama
    * Text-only, not multi-modal
  * PDF links for "Source of Truth", most likely will train on it??
* Generates output with links to "Source of Truth" using a [RAG (Retrieval Augmented Generation)](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview?tabs=docs) pattern and Vector DB
* MCP
  * Reaches out to GitHub to take action
  * Uses natural language processing
  * Can also generate GitHub issues for feature requests

##### Lab Notes

4o mini seems faster than Nemo
Nemo does better with explanation, code clarity and advice

I would use 4o in places where I need a fast result. I would use Nemo when I want a clearer result or if I'm doing a code review.

Prompt seemed to impact overall tone and in-depth analysis. Temperature seemed to impact accuracy.

Nemo Compared to DeepSeek R1 -> nemo was faster and more concise
DeepSeek displayed its thought process and was much more verbose.

##### General

* Fun Fact - DeepSeek needs 671 GB of RAM to run fully locally.
* Ollama - Open source runtime environment for AI.
* Small chunks = better.
* Model stays in memory until cleared, makes subsequent requests faster.
* MCP (Model Context Protocol) a way for clients and services to communicate, either agent to agent or person to agent.
  * Gets us away from tightly coupled solutions.
  * Server side manages things.
  * Client role consumes the model context.
  * Simplifies context management.
  * Improves model responsiveness.
  * Opens the door to multi-model orchestration.
* Cloud version of the app does pretty much the same, except computation is done in the cloud. It was much faster by comparison.
* Azure Search used to be Cognitive services, has competitive edge since its very mature.
* [GitHub models let you try different models to find the right fit and gets it setup in AzureAI.](https://github.com/marketplace?type=models)
* NLP (Natural Language Processing) is for computers to understand human language.
* LM (Language Models) use probability distributions to generate sequences of words.
* LLM (Large Language Models) are just really really really big language models.
* All use tokens to process requests. Tokens are not words, but they are pieces of the request/response.
* Real time search outside of the sandboxed training data is now possible. Asking about newer things like stocks and game outcomes should work. Newer language syntax may not be.
* LoRAs can be used to fine-tune models to reduce bias, add diversity, and adjust the 'style' as desired for images or other modes.
* [HuggingFace](https://huggingface.co) is a Model community that lists all models.
* Ollama is equivalent to Azure AI Services, but its self-host. Turbo sends it out to the cloud.

[Stephen Wolfram's What is ChatGPT doing???](https://bri.gd/swchatgpt).

## Tuesday

## Wednesday

## Thursday
