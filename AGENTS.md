> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- **QuotaMint** — the product name; Mintlify is only the publishing platform.
- **Runtime API** — the machine-facing data plane: `/v1/check`, `/v1/consume`, `/v1/events`.
- **Internal API** — server-only `/internal/v1/*` routes for the control plane; never suggested as a
  customer integration surface.
- **Account plan** — Free/Pro/Scale, applied to a *workspace*. **Plan** — a product plan integrators
  create for *their* customers. Never use the two interchangeably.
- QuotaMint has **no SDK**. Describe every integration as plain REST; the contract source is
  `openapi/quotamint-runtime.yaml` in the main repository.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

- Document implemented behavior only. If the runtime does not do it, say so or leave it out.
- Do not expose internal implementation details on integration-facing pages: no internal error
  internals, no worker scheduling internals, no dashboard session code paths.
- `/internal/v1/*` routes are documented only as the control plane's own surface, never as a path a
  customer's app should call.
- Credit amounts are decimals: described with "up to six decimal places", never as floats.
