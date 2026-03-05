# Protocol Bridge — Agent Rules

## Project Overview
Bridge between Model Context Protocol (MCP) and Agent-to-Agent Protocol (A2A).
Deep research project: `~/deep-research/active/protocol-bridge/BRIEF.md`

## Stack
- Python 3.12+
- MCP SDK
- A2A SDK / httpx (A2A protocol implementation)
- FastAPI (bridge server)

## Code Style
- `snake_case` for variables/functions/modules
- `kebab-case` for files/directories
- `PascalCase` for classes
- All code, comments, and docs in English

## Architecture
- `src/protocol_bridge/` — main package
  - `mcp_to_a2a.py` — expose MCP tools as A2A Agent Cards
  - `a2a_to_mcp.py` — call MCP tools via A2A
  - `bridge.py` — unified bridge interface
  - `models.py` — shared data models
  - `demo.py` — end-to-end demo
- `tests/` — pytest test suite
- `specs/` — interoperability spec documents

## Development
```bash
pip install -e ".[dev]"
pytest
ruff check . && ruff format .
```
