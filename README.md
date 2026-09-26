# QuotaMint documentation

The QuotaMint developer documentation is built with Mintlify. It covers the dashboard control plane, Go runtime API, customer plans, feature entitlements, credits, usage events, idempotency, webhooks, production deployment, and account limits.

## Local preview

Install the Mintlify CLI:

```bash
npm i -g mint
```

Run it from this directory:

```bash
mint dev
```

The preview runs at `http://localhost:3000`.

## Content rules

- Document implemented behavior only.
- QuotaMint has no SDK. Every integration page shows plain REST calls; never imply that an
  `@quotamint/*` package exists. The machine-readable contract is
  [`openapi/quotamint-runtime.yaml`](https://github.com/poorna-prakash-sr/quotamint/blob/main/openapi/quotamint-runtime.yaml)
  in the main repository.
- Keep test and live examples visibly separate.
- Use QuotaMint for the product name; Mintlify is the publishing platform.
- Keep Stripe, Razorpay, Paddle, and similar providers in the billing-integration context. QuotaMint does not process payments.
- This site is customer-facing only. Never document QuotaMint internals: no internal API routes,
  no self-hosting or deployment instructions, no operator endpoints (health, ready, metrics), no
  environment variables, no storage or worker implementation details.
- For runtime changes, update the API reference and the relevant guide together.

## Publishing

Mintlify deploys changes from the configured repository after they reach the default branch. See the [Mintlify documentation](https://mintlify.com/docs) for deployment configuration.