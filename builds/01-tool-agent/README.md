# Build 1: tool-calling agent on the raw API

Goal: understand the agent loop by writing it yourself. No framework. One file.

## What it does

A small agent that answers questions about the files in a folder. The model decides which tools to call, the code runs them, the model reads the results and answers.

Tools:
- `list_files(path)` returns file names in a folder
- `read_file(path)` returns the text of one file
- `search(pattern)` greps the folder for a string

Example: "Which file defines the retry logic and what is the max attempts?"

## Steps

1. Call the model once with a system prompt and a user message. Print the reply. Note the token counts.
2. Add one tool definition (`list_files`). Observe that the reply now contains a `tool_use` block instead of text.
3. Write the loop: while the stop reason is `tool_use`, run the tool, append a `tool_result`, call again. Stop when the model returns text.
4. Add the other two tools. Ask a question that needs all three.
5. Add a cap: maximum 10 loop turns. Log every tool call with its arguments and how long it took.
6. Break it on purpose: ask about a file that does not exist, pass a path outside the folder, ask something unanswerable. Fix each one.
7. Add one `assert` based self-check at the bottom that runs the agent on a fixed folder with a known answer.

## What to write down in notes/

- The exact message shape the API expects for tool results
- What happens to cost as the conversation grows and why
- The first thing that broke and why the model did it
- Where you would need a guardrail if the tools could modify files

## Run

```
cp .env.example .env   # add your key
uv run agent.py "your question" ./some_folder
```
