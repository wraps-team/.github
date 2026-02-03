# Wraps

**Deploy email infrastructure to your AWS account in 30 seconds.**

Wraps is a CLI and TypeScript SDK that deploys production-ready email infrastructure (AWS SES) directly to your AWS account. No vendor lock-in, no stored credentials, just AWS pricing.

## Why Wraps?

- **Full Ownership** — Infrastructure lives in your AWS account. You own your data.
- **AWS Pricing** — Pay AWS directly at $0.10 per 1,000 emails. No markup.
- **Beautiful DX** — TypeScript SDK, dashboards, and 30-second setup.

## Quick Start

```bash
npx wraps email init
```

```typescript
import { Wraps } from '@wraps.dev/email';

const wraps = new Wraps();

await wraps.emails.send({
  from: 'hello@yourapp.com',
  to: 'user@example.com',
  subject: 'Welcome!',
  html: '<h1>Hello from Wraps!</h1>',
});
```

## Repositories

| Repository | Description |
|------------|-------------|
| [wraps](https://github.com/wraps-team/wraps) | CLI tool for deploying infrastructure |
| [wraps-js](https://github.com/wraps-team/wraps-js) | TypeScript SDK (`@wraps.dev/email`) |

## Links

- [Documentation](https://wraps.dev/docs)
- [Get Started](https://wraps.dev/docs/quickstart)
- [Discord](https://discord.gg/wraps)
