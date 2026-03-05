# Protocol Bridge: MCP <-> A2A

The missing infrastructure layer between Model Context Protocol (agent-to-tools) and Agent-to-Agent Protocol (agent-to-agent). A bridge that lets Claude Code agents collaborate with Gemini, GPT, and other AI systems via standardized protocols.

## What It Does

- **MCP to A2A:** Expose MCP tools as A2A Agent Cards
- **A2A to MCP:** Allow A2A clients to call MCP tools
- **Multi-vendor:** Enable Claude + Gemini + GPT agent collaboration

## Installation

```bash
pip install protocol-bridge
```

## Quick Start

```python
from protocol_bridge import Bridge

bridge = Bridge()

# Expose MCP tools as A2A Agent Cards
bridge.expose_as_a2a(mcp_server="my-tools")

# Call MCP tools via A2A
result = bridge.a2a_to_mcp(
    agent_card="gemini-agent",
    tool="code_search",
    params={"query": "authentication"}
)
```

## Demo

Claude Code agent delegates a task to a Gemini agent via A2A, which uses MCP tools to complete it:

```bash
python -m protocol_bridge.demo
```

## Why This Exists

MCP won the tool-access war. Google's A2A won agent communication. But the two protocols don't talk to each other. 50+ companies support A2A. Thousands of MCP servers exist. No bridge. This is the middleware layer for the entire multi-agent ecosystem.

## Status

Early development. See [BRIEF.md](~/deep-research/active/protocol-bridge/BRIEF.md) for project plan.

## License

MIT
