# Instalação detalhada

SENATRAN: Consultar Exame Toxicológico é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_senatran_exame_toxicologico`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_senatran_exame_toxicologico` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_senatran_exame_toxicologico` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_senatran_exame_toxicologico` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.senatran_exame_toxicologico` (ou `servers.senatran_exame_toxicologico` no VS Code) do config do cliente e reinicie.
