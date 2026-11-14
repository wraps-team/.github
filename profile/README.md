# Wraps

One command deploys a full email platform into your own AWS account: SES, event tracking, bounce and complaint handling, templates and a dashboard. You pay AWS directly. Wraps never stores your AWS keys and never sits in the sending path, so your mail keeps flowing even if Wraps goes down.

```bash
npx @wraps.dev/cli email init
```

```ts
import { WrapsEmail } from "@wraps.dev/email";

const email = new WrapsEmail({ region: "us-east-1" });

await email.send({
  from: "you@yourapp.com",
  to: "user@example.com",
  subject: "Welcome!",
  html: "<h1>Hello</h1>",
});
```

The same CLI deploys SMS (`wraps sms init`, AWS End User Messaging) and a CDN (`wraps cdn init`, S3 + CloudFront). Every resource it creates is named `wraps-*`, and it never modifies the SES setup you already have.

## What do you want to do?

| I want to… | Start here |
|---|---|
| Send transactional email from my app | `npx @wraps.dev/cli email init`, then the [Next.js](https://wraps.dev/docs/quickstart/email/nextjs), [Express](https://wraps.dev/docs/quickstart/email/express), [Remix](https://wraps.dev/docs/quickstart/email/remix) or [Cloudflare](https://wraps.dev/docs/quickstart/email/cloudflare) quickstart |
| Send sign-up, magic-link and password-reset email with Better Auth | [better-auth-wraps](https://github.com/wraps-team/better-auth-wraps) · [guide](https://wraps.dev/docs/guides/better-auth) |
| Move off Resend, SendGrid, Postmark or Mailgun | [Migration guide](https://wraps.dev/docs/guides/migration) · [comparisons](https://wraps.dev/compare) |
| Already on SES, but tired of hand-rolling bounces and suppression | [Bounce handling](https://wraps.dev/docs/guides/bounce-handling) · [suppression lists](https://wraps.dev/docs/guides/suppression-lists) |
| Send broadcasts and automated sequences to my users | [Workflows](https://wraps.dev/docs/quickstart/email/workflows) · [templates](https://wraps.dev/docs/quickstart/email/templates) |
| Receive email and handle replies | [Inbound](https://wraps.dev/docs/quickstart/email/inbound) · [reply threading](https://wraps.dev/docs/guides/reply-threading) |
| Let my AI agent send email from my account | [Agents quickstart](https://wraps.dev/docs/quickstart/email/agents) · [MCP server](https://wraps.dev/docs/mcp-reference) · [skills](https://github.com/wraps-team/skills) |
| Send SMS, like one-time codes | `npx @wraps.dev/cli sms init` · [SMS quickstart](https://wraps.dev/docs/quickstart/sms) |
| Serve files from S3 behind CloudFront | `npx @wraps.dev/cli cdn init` · [CDN quickstart](https://wraps.dev/docs/quickstart/cdn) |
| Send from Python | `pip install wraps-email` · [Python SDK](https://wraps.dev/docs/python-sdk-reference) |
| Keep my infrastructure in Pulumi or CDK | [Pulumi](https://wraps.dev/docs/pulumi-reference) · [CDK](https://wraps.dev/docs/cdk-reference) |
| Build an inbox or composer UI | [components](https://github.com/wraps-team/components) |

## Repositories

| Repo | What it is |
|---|---|
| [wraps](https://github.com/wraps-team/wraps) | The CLI, the dashboard and the Pulumi/CDK packages. AGPLv3. |
| [wraps-js](https://github.com/wraps-team/wraps-js) | TypeScript SDKs: `@wraps.dev/email` and `@wraps.dev/sms`, plus an MCP server (`@wraps.dev/mcp`) so AI agents can send from your account. MIT. |
| [wraps-py](https://github.com/wraps-team/wraps-py) | Python SDK: `pip install wraps-email`. MIT. |
| [better-auth-wraps](https://github.com/wraps-team/better-auth-wraps) | Better Auth plugin: sends auth email through your SES and syncs sign-ups to contacts. |
| [skills](https://github.com/wraps-team/skills) | Agent skills for Wraps email, SMS and CDN, plus SES deliverability best practices. |
| [components](https://github.com/wraps-team/components) | Email UI for shadcn: inbox, composer and a sandboxed HTML email renderer. |

## Is it for you?

Wraps fits if you're fine with an AWS account and want SES pricing without building the plumbing around it. If you don't want to touch AWS at all, a hosted provider will suit you better.

[Docs](https://wraps.dev/docs) · [Quickstart](https://wraps.dev/docs/quickstart) · [Pricing](https://wraps.dev/pricing) · [Discord](https://discord.gg/pdgAa6xAWF) · [@useWraps](https://x.com/useWraps)
