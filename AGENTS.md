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
- Internal API routes (`/internal/v1/*`) exist in the product but are **never documented** on this
  site; the docs are customer-facing only.
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
- Do not expose internal implementation details: no internal API routes, no deployment or
  self-hosting docs, no operator endpoints, no environment variables, no storage, worker, or
  session implementation details.
- Credit amounts are decimals: described with "up to six decimal places", never as floats.
