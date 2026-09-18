# Using with Claude

The repository includes a Claude Code plugin manifest and marketplace catalog.

1. Download and unzip the repository.
2. Open a terminal in the downloaded folder.
3. Run `claude plugin marketplace add .`.
4. Run `claude plugin install ai-cfo@ai-cfo-skills`.
5. Start a new Claude Code session.

Claude can invoke the skill automatically when the request matches its description. To invoke it directly, run `/ai-cfo:ai-cfo`.

The installed plugin is self-contained under `plugins/ai-cfo`; it does not rely on files outside that directory.
