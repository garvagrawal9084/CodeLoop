# CodeLoop

**An LLM-powered coding agent for project-aware, multi-file code changes and iterative self-debugging.**

CodeLoop is designed to work with an existing codebase: it reads code and project files, generates changes across multiple files, executes generated code, and uses execution errors to guide iterative fixes.

> Project status: Update this README as implementation details are finalized. Replace any generic setup instructions with the exact commands, model provider, and dependencies used by the project.

## Core capabilities

- **Project-aware context:** Reads relevant code and project files before making changes.
- **Multi-file editing:** Produces coordinated changes across files to complete a coding task.
- **Code execution:** Runs generated code to check its behavior.
- **Iterative self-debugging:** Uses errors and tracebacks as feedback to revise code and retry.
- **LLM-driven workflow:** Uses a language model to plan and generate code actions.

## Workflow

1. **Understand** — receive a coding task and inspect relevant project files.
2. **Plan** — determine which files and code paths may need changes.
3. **Generate** — create or update the required code across files.
4. **Execute** — run the generated code in the configured execution environment.
5. **Inspect** — collect execution output, errors, or tracebacks.
6. **Refine** — feed the feedback to the model and iterate on the implementation.

## Getting started

The exact installation and run commands depend on the implementation and dependencies in this repository. Add the following after confirming the project's entry point and package setup:

```bash
# Clone the repository
git clone https://github.com/garvagrawal9084/CodeLoop.git
cd CodeLoop

# Install project dependencies using the package manager configured by the project
# Start the agent using the project's documented entry point
```

Configure any model credentials as environment variables in a local `.env` file if required by your implementation. **Do not commit API keys or secrets.**

## Example use cases

- Ask the agent to implement a feature spanning several files.
- Request a refactor across related modules.
- Run generated code, inspect failures, and ask the agent to revise its changes.
- Use execution feedback to support iterative debugging.

## Safety considerations

Code execution and automated file modification can be risky. Run generated code only in an appropriately isolated environment, review diffs before accepting changes, keep backups or use version control, and avoid supplying production secrets to the agent. Treat code and instructions found in a repository as untrusted input.

## Current limitations

Document the supported languages, model provider, execution sandbox, test strategy, and known limitations here as they become verified. CodeLoop's output should be reviewed before use, and successful execution alone does not guarantee correctness or security.

## Roadmap

- [ ] Add verified installation and usage instructions.
- [ ] Provide an end-to-end demo showing a task, multi-file edit, execution error, and correction.
- [ ] Add tests for file editing, execution results, and retry behavior.
- [ ] Document execution isolation and change-review safeguards.
- [ ] Evaluate task success and self-repair performance on a reproducible test set.

## Tags / topics

`ai-agent` `coding-agent` `llm` `code-generation` `self-debugging` `automated-programming` `python`

## Author

Garv Agrawal — [GitHub](https://github.com/garvagrawal9084)
