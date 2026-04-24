## AI Agent:
- LLM agents reside in AI agents, chatgpt, gemini are all llm models that use neural networks
- 90% boom due to LLM Agents
- A large language model is a computational model capable of language generation or other natural language processing tasks. As language models, LLMs acquire these abilities by learning statistical relationships from vast amounts of text during a self-supervised and semi-supervised training process
- fancy and huge autocompletes, language models predict and generate plausible language, input -> model -> output, LLM's are extremely huge autocompletes
	
## Build a Auto-complete:
- analyses from past writing to help propose the new next word that come up
- the more data that you have the more suitable the suggestions in the. auto complete would be 
- From autocomplete to LLMs
    - input -> model -> output
	- bunch of data, training it and the input would a lot of words, tokens
	- LLM can take in works and predict the next words. 
	-	models are built around different algorithms, neural networks, rag algorithm, a lot of math
	-	the larger the model, the bigger the model, the better answers or choices that it can be used 
-	prompt engineering
    - prompt is the coach, clear instructions and context bunch of neurons, well crafted texts 
	-	the prompting process: setting the goal, providing context, guiding the style
	-	better prompt have improved accuracy, enhanced creativity, task efficiency##
- conversable agent
    - is the basic block you have in autogen 
    - there are a many different types of conversable agents
    - assistantAgent: basically LLMs, they use Chatgpt, can use other LLMs as well, load different LLMs, 
    - UserProxyAgent: Us, human input mode, create a conversation between assistant agent and user proxy agent. we will be able to tell 
    the agent what we want
    - groupchat manager: orchestrate a conversation between other agents, agents for each of the speciality, orchestrator
- different types of chats we can create in Autogen
    - user role is like sending a message as a normal prompt
    - system role is when we ask the LLM to assume a specific role like be a doctor, artist, writer etc
    - we can also have other agents that will check the output provided by an existing agent
    - one agent provides a fact, another check the fact, another verifies the feedback and asks the initial agent to create a new version of the task
- creating agents with state
    - there will be two blocks, one block will save the prompt and another will store the memory
    - system message is where we will be telling the LLM to assume a role 
- running LLMs locally
    - using LM studio, connecting to the servers that are hosted in from the outside servers
    - we can have conditional limit to when to stop the conversation and when to keep the chat going on until the condition is met
    - 

## AutoGen Chat
- sequential chat: customer provide the necessary information and later a human can intervene, like a call centre. onboarding personal information agent, onboarding issue agent, customer engagement agent
- when having multiple agents, we need to orchestrate the flow of the chat, which will orchestrate the chat between the agents
- summary prompt method : where the agents will extract the details and problems of the user that they describe to the llm agent
- code writer agent : an engineer who is accompained to write code, assistantAgent is designed to write code
- code executor agent : Conversable Agent, needs the executor config which, 

## Agents that code with skills
- teach agents how to do things so that the tokens used to complete the tasks would be cheaper and easier
- function has doc string which has description of the function
- executor.format_fuctoins_for_prompt : this function will give a direction to the executor agent on how to write the code and to use the existing functions already defined. this tag will make use of the doc strings defined for each function
- **Group Chat with the agents** : define different type of agents, and let them in-between them figure out which agent will do what. We will define the agents. 
Later we will use their conversation to use in another group chat
the main members in the chat would be : planner, executer, writer, user, engineer
group chat manager is an autogent agent which will direct the conversation, which will manage the group chat and the messages in the chat

## Building a financial application
- This application will be used to perform stock analysis, predict and perform and suggest appropriate investment methods
### Goals of the App
- takes as an input asset tickets
- downloads asset price data and analyzes them 
- retrieve or compute the ratios: P/E ratio, forward P/E, dividends, price to book, debt/eq, roe
- analyze the correlation between the stocks
- plot their normalized prices for compensation
- writes a financial report about these assets and then analyzes and summarizes these news headlines
- this will also use different reviewers:
    - Legal reviewer
    - Text/Data alignment reviewer
    - Consistency reviewer
    - Completion reviewer
- refines the report based on previous criticisms
- saves the final report to a markdown file with a normalised price chart

### Prompt Engineering
- Make sure you are directing the LLM to the exact way you want. You should prevent the LLM hellucination in the response you are getting

### Streamlit app
- 