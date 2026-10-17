# Toy ai agent

Basic ai agent, has limited available tools: get-file-content, get-files-info, run-python-file, write-file.
These tools are found inside the dummy/sandbox directory called Calculator. The tools are only able to work within the parent directory to avoid them escaping and changing files on outside that area.

Clone the repo to get up and running you will need to run

```shell
uv sync
source .venv/bin/activate
```

Then you will want to create a .env file and put your own OPENROUTER_API_KEY value in there and set PROMPT_MODE="enabled" or "disabled" depending on if you want to fire off the prompt to open ai router

```shell
uv run main.py --help
usage: main.py [-h] [--verbose] user_prompt

toy ai agent chatbot

positional arguments:
  user_prompt  User prompt

options:
  -h, --help   show this help message and exit
  --verbose    Enable verbose output
```
