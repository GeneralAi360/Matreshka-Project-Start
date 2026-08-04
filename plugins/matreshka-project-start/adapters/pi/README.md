# Pi adapter (optional)

Pi is optional. When the owner requests it, map the canonical role contracts to `.pi/agents/` and configure only approved MCP servers in `.pi/mcp.json`.

Do not copy credentials into `.pi/mcp.json`. Browser, SSH, SFTP and other MCP integrations require their own explicit installation and permission design. Keep server operations read-only by default; do not grant broad `sudo` or password-based production SSH to an agent.
