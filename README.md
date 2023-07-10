# langchain-crash-course-python-google-colab-notebook

## LangChain crash course
-  based on PromptEngineering Crash course https://www.youtube.com/watch?v=5-fc4Tlgmro
-  This repo has a Google Colab notebook, hosted at https://colab.research.google.com/drive/1gKpLkqGDFYdcjpK1653r2I13pr1_UKO_#scrollTo=plLzOPNFbJzA
-  This repo doesn't implement secret key management and exposes my OpenAI and HuggingFace secrets, but this account's usage has been capped at $5 (with a $4 soft limit) to prevent abuse

## This Repo contains working examples for the following:

- **Installation**
  - Install LangChain (and other deps) as PyPi
    
- **Integration with Available LLMs**
  - Integrate with OpenAI and HuggingFace
  - LangChain also has integrations with several different LLMs, including Google's LLMs, list is here: https://python.langchain.com/en/latest/modules/models/llms/integrations.html
    
- **Prompt Templates**
  - A prompt template refers to a reproducible way to generate a prompt. It contains a text string (“the template”), that can take in a set of parameters from the end user and generate a prompt. The prompt template may contain:
    - instructions to the language model,
    - a set of few shot examples to help the language model generate a better response,
    - a question to the language model.
      
- **Chains**
  - Using an LLM in isolation is fine for some simple applications, but many more complex ones require chaining LLMs - either with each other or with other experts.
    
- **Agents & Tools**
  - Agents use an LLM to determine which actions to take and in what order. An action can either be using a tool and observing its output, or returning to the user.
    - Tool: A function that performs a specific duty. This can be things like: Google Search, Database lookup, Python REPL, other chains.
    - LLM: The language model powering the agent.
    - Agents: Agents involve an LLM making decisions about which Actions to take, taking that Action, seeing an Observation, and repeating that until done.
  - Potential use cases:
    - Personal Assistant
    - Question Answering
    - Chatbots
    - Code Understanding etc.
      
- **Memory**
  - Memory is the concept of persisting state between calls of a chain/agent.
  - LangChain provides a standard interface for memory, a collection of memory implementations, and examples of chains/agents that use memory.
    
- **Document Loaders**
  - Combining language models with your own text data is a powerful way to differentiate them.
  - The first step in doing this is to load the data into “documents” - a fancy way of say some pieces of text.
  - https://python.langchain.com/en/latest/modules/indexes/document_loaders.html
- **Indexes, Embeddings, Vector Stores / Vector Databases**
  - Indexes refer to ways to structure documents so that LLMs can best interact with them. This module contains utility functions for working with documents, different types of indexes, and then examples for using those indexes in chains.
    - Embeddings: An embedding is a numerical representation of a piece of information, for example, text, documents, images, audio, etc.
    - Text Splitters: When you want to deal with long pieces of text, it is necessary to split up that text into chunks.
    - Vectorstores: Vector databases store and index vector embeddings from NLP models to understand the meaning and context of strings of text, sentences, and whole documents for more accurate and relevant search results.
