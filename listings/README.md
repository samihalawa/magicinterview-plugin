# Published MagicInterview plugins and connectors

MagicInterview is a live interview and meeting helper: it listens to the conversation, uses your CV, job, client and company context, and shows what to say next while you speak. Every assistant listing below connects to the same workspace through `https://magicinterview.ai/mcp`; live audio runs in the full app.

All listings are sourced from this folder (`plugins/magicinterview` in `samihalawa/2026-CODEX-MagicInterview`). The public repository `samihalawa/magicinterview-plugin` is a generated mirror: publish it with `script/publish_plugin_mirror.sh` from the monorepo after committing changes here (the mirror's `sync-from-monorepo.yml` does the same on manual dispatch). Never edit the mirror directly.

| Channel | Listing | Source here | How it updates |
| --- | --- | --- | --- |
| Claude directory: plugin | [claude.ai plugin 3541ff62…](https://claude.ai/customize/plugins/id/3541ff62-ac03-45af-a6cb-e2ef5aeead66%40anthropic-plugin-directory) | `.claude-plugin/plugin.json`, `skills/`, `.mcp.json` | Anthropic directory webhook on the public mirror syncs each push |
| Claude directory: connector | [MagicInterview AI](https://claude.ai/directory/magicinterview-ai) | `listings/claude-directory-connector.json` (snapshot), endpoint `/mcp` | Listing text changes go through the Claude directory submission; tools come live from the server |
| Claude Code / Codex marketplace | repo root `.claude-plugin/marketplace.json`, `.agents/plugins/marketplace.json` | this folder | Pull of this repository |
| ChatGPT / OpenAI plugin | portal plugin `plugin_asdk_app_6ad880b2e2ac8191b4be89ecee3a8cd5` | `.codex-plugin/plugin.json`, `scripts/package_openai.py`, `docs/publishing.json` | Package and upload a new version in the OpenAI portal |
| Official MCP Registry | [io.github.samihalawa/magicinterview](https://registry.modelcontextprotocol.io/v0.1/servers/io.github.samihalawa%2Fmagicinterview/versions/latest) | `server.json` | `mcp-publisher publish` after a version bump |
| Glama | [glama.ai connector](https://glama.ai/mcp/connectors/io.github.samihalawa/magicinterview) | `server.json`; ownership claim served by `server/glama.js` | Follows the MCP Registry entry |
| LobeHub | `samihalawa-magicinterview-plugin` | `lhm.plugin.json` | Reads the public mirror |
| Smithery | `sami-k2i2/magicinterview` | `mcp.json`, endpoint `/mcp` | Smithery dashboard |
| Docker MCP Registry | `servers/magicinterview` PR from the `samihalawa/mcp-registry` fork | `mcp/docker-registry/` | Copy into the fork and update the PR |
