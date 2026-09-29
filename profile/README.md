 # MCP in Practice for Developers

  A hands-on workshop on building, securing and operating [Model Context Protocol](https://modelcontextprotocol.io) servers and AI agents on Red Hat OpenShift.

  Connecting an agent straight to a REST API or a database gets you data over-fetching, credentials in every client, and no audit trail. This workshop treats MCP as a control plane instead:
  tools that expose intent rather than raw resources, payloads trimmed before they reach the model, identity carried from a verified token to the workload, and tool access governed in one
  place.

  It runs against a fictional retailer, Globex, whose store API already exists and is not going to change — the brownfield case most enterprises are actually in.

  ## Modules

  | # | Module | Focus |
  |---|---|---|
  | 1 | Build Your First MCP Server | Wrap an existing OpenAPI service with a Quarkus MCP server, minimize its payload, move the customer identifier onto a header, deploy via GitOps |
  | 2 | Expand Agent Capability with MCP Server | Give a LangChain4j agent two MCP servers, carry the signed-in user through to every tool call |
  | 3 | Enable Security & Identity | SPIFFE/SPIRE workload identity, Keycloak OIDC, token exchange, guardrails |
  | 4 | Full-Stack Observability | LangFuse and the LGTM stack for tracing agent and LLM calls |
  | 5 | Centralized Governance | An MCP gateway holding credentials and enforcing tool filtering, instead of both being copied into every agent |

  ## Repositories

  **Lab guide**
  - [`showroom`](../showroom) — A Static workshop guide itself 

  **What attendees build and run**
  - [`globex-store-mcp`](https://github.com/mcp-developers-workshop/globex-store-mcp) — starting point for the MCP server built in Module 1
  - [`globex-complaint-agent`](https://github.com/mcp-developers-workshop/globex-complaint-agent) — the complaints agent extended in Module 2
  - [`globex-complaint-agent-helm`](https://github.com/mcp-developers-workshop/globex-complaint-agent-helm) — its Helm chart
  - [`mcp-workshop-chatbot`](https://github.com/mcp-developers-workshop/mcp-workshop-chatbot) — Angular front end used to drive the agent
  - [`globex-complaints`](https://github.com/mcp-developers-workshop/globex-complaints) — a greenfield MCP server over the complaints database
  - [`globex-complaints-orchestrate`](https://github.com/mcp-developers-workshop/globex-complaints-orchestrate) — watsonx Orchestrate workspace for Module 5

  **Environment**
  - [`install-helm`](https://github.com/mcp-developers-workshop/install-helm) — Helm charts for every component of the workshop cluster
  - [`install-ansible`](https://github.com/mcp-developers-workshop/install-ansible) — provisioning automation

  These repositories are the source of truth. The GitLab instance inside a workshop cluster is seeded from them, and that is the copy attendees clone.
