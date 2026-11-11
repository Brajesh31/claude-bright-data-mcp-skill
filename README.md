# Claude Bright Data MCP Skill

A skill for using Bright Data MCP as an interface to web search, page extraction, structured platform data, and browser automation. It describes tool selection across rapid and Pro modes and includes setup, usage, and troubleshooting guidance.

## What It Covers

- **Web search:** Search engines through single-query and batch search tools.
- **Page extraction:** Retrieve webpage content as Markdown or HTML.
- **Structured platform data:** Use platform-specific extraction tools when available.
- **AI extraction:** Convert page content into structured fields.
- **Browser automation:** Navigate and interact with pages using browser tools.
- **MCP setup:** Configure the Bright Data server and verify the connection.
- **Tool selection:** Choose the most specific tool for each data operation.
- **Troubleshooting:** Resolve connection, authorization, and missing-tool issues.

## Installation and Setup

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-bright-data-mcp-skill.git ~/.claude/skills/bright-data-mcp
```

Connect and configure the Bright Data MCP server according to the instructions in `references/mcp-setup.md`. Pro features depend on the configured remote or local MCP mode and the Bright Data account.

## Using the Skill

Example request:

```text
Use the bright-data-mcp skill to search the web for current information
and return the most relevant sources with their key details.
```

For a webpage, ask for a Markdown extraction. For supported platforms, request structured data. For interactive tasks, use the browser automation tools.

## Tool Selection

| Task | Tool category |
|---|---|
| Search the web | `search_engine`, `search_engine_batch` |
| Read a webpage | `scrape_as_markdown`, `scrape_batch` |
| Retrieve raw HTML | `scrape_as_html` |
| Extract structured fields | `extract` |
| Retrieve supported platform data | Matching `web_data_*` tool |
| Interact with a page | `scraping_browser_*` tools |

## Repository Resources

- [SKILL.md](SKILL.md) contains the core instructions and tool selection guidance.
- `references/mcp-setup.md` explains server setup.
- `references/mcp-tools.md` documents the available tool groups and parameters.

## Important Notes

Verify that the MCP server is connected before invoking its tools. Tool availability depends on rapid or Pro mode and the enabled tool groups. Keep credentials private and check current Bright Data documentation for tool availability, pricing, and limits.
