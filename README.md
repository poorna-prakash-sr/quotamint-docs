# QuotaMint documentation

Customer-facing documentation for QuotaMint, a developer service for plans, feature access, usage metering, and credits.

The site is built with [Mintlify](https://mintlify.com). Content lives in MDX files and navigation is configured in `docs.json`.

## Preview locally

Install the Mintlify CLI:

```bash
npm install --global mint
```

Start the local preview from this directory:

```bash
mint dev
```

Open `http://localhost:3000` to view the documentation.

## Validate content

```bash
mint validate
mint broken-links
```

The public docs intentionally exclude deployment credentials, internal service endpoints, database details, and implementation-specific logic.
