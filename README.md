# langchain-for-llm-application-development-coursera

## Description
* Learn LangChain by following the tutorials in the course 'LangChain for LLM Application Development' on Coursera.
* Prepare .env file with the content below:
  * OPENAI_API_KEY=<YOUR_OPENAI_API_KEY_HERE>
* Replace all deprecated langchain modules with latest modules.

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