# Agent Skills (agent-skills)
A collection of resources, APIs, and standards related to AI agent skills and capabilities. Agent skills represent the tools, functions, and capabilities that AI agents can invoke to accomplish tasks — spanning web search, code execution, file management, memory, and external API integrations. This topic covers the major platforms and frameworks that define how agent skills are declared, discovered, and invoked.

**URL:** [https://github.com/api-evangelist/agent-skills](https://github.com/api-evangelist/agent-skills)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Agent Skills, AI Agents, Tool Use, Function Calling, MCP, Agentic AI, Automation

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-04-19

## APIs

### Anthropic Tool Use API
The Anthropic Tool Use API allows AI agents built on Claude to call client-defined functions or Anthropic-provided server tools such as web search, code execution, and web fetch. Tools are declared in the API request and Claude decides when to invoke them based on context. Server tools run on Anthropic infrastructure while client tools execute in the calling application.

**Human URL:** [https://platform.claude.com/docs/en/docs/agents-and-tools/tool-use/overview](https://platform.claude.com/docs/en/docs/agents-and-tools/tool-use/overview)

#### Tags:

 - Anthropic, Tool Use, Function Calling, Claude, AI Agents

#### Properties

- [Documentation](https://platform.claude.com/docs/en/docs/agents-and-tools/tool-use/overview)
- [APIReference](https://platform.claude.com/docs/en/docs/agents-and-tools/tool-use/tool-reference)
- [GettingStarted](https://platform.claude.com/docs/en/docs/agents-and-tools/tool-use/build-a-tool-using-agent)

### Google Agent Development Kit (ADK)
Google's Agent Development Kit (ADK) is a flexible framework for building AI agents and multi-agent systems. It supports LLM agents, workflow agents, and custom agents with capabilities including MCP tool integration, OpenAPI tools, function tools, grounding via Google Search, streaming via Gemini Live API, and Agent-to-Agent (A2A) protocol for inter-agent communication. Available in Python, TypeScript, Go, and Java.

**Human URL:** [https://adk.dev/](https://adk.dev/)

#### Tags:

 - Google, Agent Development Kit, ADK, Multi-Agent, Gemini, Tool Use

#### Properties

- [Documentation](https://adk.dev/)
- [GettingStarted](https://adk.dev/get-started)
- [GitHubRepository](https://github.com/google/adk-python)

### Model Context Protocol (MCP)
The Model Context Protocol (MCP) is an open-source standard for connecting AI applications to external systems. MCP defines a standardized way for AI agents to access data sources, tools, and workflows. It enables agents to call external tools, access files, databases, and APIs through a consistent protocol supported by Claude, ChatGPT, VS Code, Cursor, and many other AI clients.

**Human URL:** [https://modelcontextprotocol.io/introduction](https://modelcontextprotocol.io/introduction)

#### Tags:

 - MCP, Model Context Protocol, Standards, Tool Use, Open Source

#### Properties

- [Documentation](https://modelcontextprotocol.io/introduction)
- [GettingStarted](https://modelcontextprotocol.io/docs/develop/build-server)
- [GitHubRepository](https://github.com/modelcontextprotocol/specification)

## Common Properties

- [GitHubOrganization](https://github.com/api-evangelist)
- [JSONSchema - Tool Schema](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/json-schema/agent-skills-tool-schema.json)
- [JSONSchema - Tool Call Schema](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/json-schema/agent-skills-tool-call-schema.json)
- [JSONSchema - Tool Result Schema](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/json-schema/agent-skills-tool-result-schema.json)
- [JSONSchema - MCP Server Schema](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/json-schema/agent-skills-mcp-server-schema.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/json-ld/agent-skills-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/agent-skills/refs/heads/main/vocabulary/agent-skills-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| Function Calling | AI agents can invoke user-defined or platform-provided functions based on natural language instructions, with structured input/output schemas. |
| Server-Side Tool Execution | Platforms like Anthropic and OpenAI run certain agent skills (web search, code execution) on their own infrastructure, removing the need for client-side execution. |
| MCP Integration | The Model Context Protocol provides a universal adapter layer enabling agents to discover and call any MCP-compatible server as a skill. |
| Multi-Agent Orchestration | Frameworks like Google ADK support coordinating multiple specialized agents, with skills delegated across agent boundaries via protocols like A2A. |
| Strict Schema Enforcement | Agent skill definitions can enforce strict JSON Schema compliance to ensure agents produce well-formed tool calls matching the declared parameter schema. |
| Tool Discovery | Anthropic's tool_search server tool enables agents to discover available tools at runtime without statically declaring all tool schemas upfront. |

## Use Cases

| Name | Description |
|------|-------------|
| Automated Research | Agents use web search and fetch skills to retrieve, synthesize, and summarize information from the internet in response to user queries. |
| Code Generation and Execution | Agents invoke code execution skills to write, run, and debug code within sandboxed environments, returning results to the user. |
| Data Integration | Agents use OpenAPI-backed skills to read and write data across enterprise systems — CRMs, ERPs, databases — through standardized API calls. |
| File and Document Management | Agents invoke file system skills to read, write, and organize documents, images, and structured data on behalf of users. |
| Multi-Step Workflow Automation | Agents chain multiple skills in sequence — searching, retrieving, transforming, and storing data — to complete complex multi-step tasks autonomously. |
| AI-Assisted Customer Support | Customer service agents use CRM lookup, ticketing, and knowledge base skills to resolve customer issues without human escalation. |

## Integrations

| Name | Description |
|------|-------------|
| Claude (Anthropic) | Native support for tool use and MCP via the Anthropic Messages API. |
| ChatGPT (OpenAI) | Function calling and MCP tool integration via the OpenAI Responses API. |
| Gemini (Google) | Tool use and ADK integration for Gemini-based agents. |
| VS Code Copilot | GitHub Copilot supports MCP servers as agent skill providers within the VS Code development environment. |
| Cursor | Cursor IDE supports MCP tool integration for AI-assisted coding agents. |
| LangChain | Open-source framework for composing agent skills into chains and graphs across multiple LLM providers. |
| LlamaIndex | Data framework enabling agents to index and retrieve from external data sources as structured skills. |

## Artifacts

Machine-readable API specifications organized by format.

### JSON Schema

- [Tool Schema](json-schema/agent-skills-tool-schema.json)
- [Tool Call Schema](json-schema/agent-skills-tool-call-schema.json)
- [Tool Result Schema](json-schema/agent-skills-tool-result-schema.json)
- [MCP Server Schema](json-schema/agent-skills-mcp-server-schema.json)

### JSON Structure

- [Tool Structure](json-structure/agent-skills-tool-structure.json)
- [Tool Call Structure](json-structure/agent-skills-tool-call-structure.json)
- [Tool Result Structure](json-structure/agent-skills-tool-result-structure.json)
- [MCP Server Structure](json-structure/agent-skills-mcp-server-structure.json)

### JSON-LD

- [Agent Skills Context](json-ld/agent-skills-context.jsonld)

## Vocabulary

- [Agent Skills Vocabulary](vocabulary/agent-skills-vocabulary.yaml) — Unified taxonomy mapping 5 resources, 6 actions, 3 workflows, and 3 personas across operational and capability dimensions

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
