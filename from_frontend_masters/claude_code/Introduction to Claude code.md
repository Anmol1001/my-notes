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
	The back and forth going from harness to model and model to harness is also called agentic loop.




**Claude.md, permissions, plan mode**
	**What is Claude.md file?**
		You can actually get the claude.md in already existing project by running /init command in the claude terminal. And it will generate the file based on your project. This file is important because all of the content of claude.md is read by model so we can provide the content like this are the things we are using in the project so that harness can reduce the tools call to the model. 
		The usefulness of the claude.md depends on model. As the model gets better, it also get better at understanding intent. It was more important in prior model like Opus 4.5 , Opus 4.4 because it does not understand intent as it understand by latest model. So this claude.md file get added to assembled prompt and if it is long then you can hit your usage faster.
	**What is plan mode?**
	You can think claude code as your co-worker. Like before implementing anything you ask you co-worker "what do you think about it?", "how should we do it?", etc. 
	And one thing about claude code is that you can add verification loop in your prompt like adding image and saying can you implement this one for me? or just ask plan it for me?
	**What is permission?**
	It is the way to control how claude code execute you code like allowing or denying edit, bash commands, git commands, etc.
	So we can do that by running /permisions command.
	There is also a command /fewer-permission-prompts which check all the tools call made while using claude code and it will try to find all the tools call you have ask the most. 


**Skills? plugin? subagents? MCP?**

