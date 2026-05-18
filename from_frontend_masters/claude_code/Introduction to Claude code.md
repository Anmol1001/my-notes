**What is Claude code?**




**How does Claude code work?**
	It is always better to know how claude code works because it is how you control the claude by knowing how it works. 
	Okay now when you are prompting something in claude code, then exactly happening inside it? like how it is processing it?
	So here claude code is really working with two pieces one is harness(or claude code which is used to run the program.) and  claude models (opus, sonnet and haiku).
	Important thing model cannot do anything in your machine, it can think about it, reason about your prompt but it cannot do directly anything in your machine like it cannot run bash command, edit the files, git history, etc. It is upto harness(or claude code) which is responsible for exposing this tools to the model so that model can understand it.
	So model is stataless which means it does not have any memory of the past prompt or idea about any conversation of file editing.
	And harness provide that state to the model like your git history, your setup, your entire environment.


**How does claude code (harness) give state to the model?**
	When you prompt something and press enter, claude assemble the data convert it into one big request (Assembled Prompt). 
	In Assembled prompt, there are three section: Tool schema (Bash, Edit, Read, Agent, etc) , System prompt (this is hardcoded by the claude itself), Messages (claude.md, prompt, and available skills).
	All this section is wrap up in one json. So model cannot read this json, it is on API side to convert this json into tokens so that model understands. 
	




**Claude.md, permissions, plan mode**





**Skills? plugin? subagents? MCP?**

