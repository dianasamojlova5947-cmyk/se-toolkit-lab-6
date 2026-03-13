# Task 1 Plan

## LLM Provider

I will use the Qwen Code API because it provides free requests and supports the OpenAI-compatible API.

Model:
qwen3-coder-plus

## Architecture

The agent will be implemented as a CLI Python script called `agent.py`.

Workflow:

1. The user runs the CLI:

uv run agent.py "question"

2. The script reads the question from command line arguments.

3. The script loads environment variables from `.env.agent.secret`.

4. The script sends the question to the LLM using the OpenAI-compatible chat completions API.

5. The LLM returns a response.

6. The agent outputs JSON to stdout with the following structure:

{
  "answer": "...",
  "tool_calls": []
}

Debug information will be printed to stderr.