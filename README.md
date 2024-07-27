# langchain-for-llm-application-development-coursera

## Description
  * Learn LangChain by following the tutorials in the course 'LangChain for LLM Application Development' on Coursera.
  * Replace all deprecated langchain modules/tools in the tutorial codes with the latest modules/tools.
  * Use "gpt-4o-mini" as llm model instead of "gpt-3.5-turbo" mentioned in tutorial for performance and cost consideration.
## Environment
  * Install python 3.11.5
  * Prepare .env file with the content below and place it at root folder:
    * OPENAI_API_KEY=<YOUR_OPENAI_API_KEY_HERE>
  * Install packages
    * python-dotenv 0.21.0
    * openai 1.37.0
    * langchain 0.2.11
    * langchain-community 0.2.10
    * langchain-core 0.2.24
    * langchain-experimental 0.0.63
    * langchain-openai 0.1.19
    * langchain-text-splitters 0.2.2
    * langchainhub 0.1.20
    * pandas 2.0.3
    * docarray 0.40.0
    * DateTime 5.5

## Codes
### L1-Model_prompt_parser.ipynb
 * Direct API calls to OpenAI
 * API calls through LangChain:
   * Prompts
   * Models
   * Output parsers

### L2-Memory.ipynb
  * RunnableWithMessageHistory
    * Analogous to using ConversationChain (deprecated) with the default ConversationBufferMemory. Due to depreciation of ConversationChain, therefore use RunnableWithMessageHistory
    * Make llm can answer question based on memory
  * Simulate ConversationBufferWindowMemory to be used by RunnableWithMessageHistory
    * The first solution: Keep only last k chats in memory
    * The second solution: Just pass the last k chats from the memory to the llm, the memory will not be affected, as previous data not affected and keep adding new data to it.
  * ConversationTokenBufferMemory
    * Not consider integrate it with RunnableWithMessageHistory until we have good usecase or example of using it
  * Simulate ConversationSummaryMemory to be used by RunnableWithMessageHistory
    * Use additional llm to summarize previous chat history

### L3-Chains.ipynb
  * LLMChain
  * Sequential Chains
    * SimpleSequentialChain
    * SequentialChain
  * Router Chain

### L4-QnA.ipynb
  * Embedding models
  * Vector stores
  * QA with data

### L5-Evaluation.ipynb
  * Example generation
  * Manual evaluation (and debuging)
  * LLM-assisted evaluation

### L6-Agents.ipynb
  * Using built in LangChain tools: Wikipedia
  * Defining your own tools - Sum Calculator and Today date
