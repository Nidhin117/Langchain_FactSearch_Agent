# Langchain_FactSearch_Agent
Building an agent using Langchain tools that can search the internet for information of a specific task 
In this project I have used Langhchain's tools meant to search Wikipedia, Perform DuckduckGo search and , SerpAPI that can perform google search and finally a tool meant to run python code.
Using these tools I developed a Langchain agent, that can break down a task into smaller tasks by using an LLM's reasoning capability (similar to Chain of Thought prompting strategy) and then decide which of the above tools to use to perform a specific smaller task and then use the result of this task to then decide which tool to use next. This goes on until the original question is answered.
Due to the limit of requests per second on TogetherAI's Llama model, I could not use opensource LLMs in this project. So I have used OpenAI's gpt-3.5 turbo model as the LLM which drives the decision making process of the agent.
Example task : How many movies did Cameron Direct in total
the agent decides to use Wikipedia tool to perform search and then uses the python interpreter to perform numerical operations and gives the final answer
