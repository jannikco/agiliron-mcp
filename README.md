# Plan an Agiliron workflow with your coding assistant

Start with the store-team question you want answered, then work out what your Agiliron connection can actually provide.

This project helps your assistant inspect the recorded setup requirements, prepare a hosted connection and discover its available actions. It is a setup helper: it does not include its own inventory, order or customer actions.

## Start with the business question

Give your coding assistant one of these prompts:

> Help me plan an Agiliron information handoff for our morning store-operations meeting. Explain what needs connecting in plain English.

> Read the linked Agiliron documentation and compare it with the information our team needs. Tell me whether an import or manual PipMCP setup is still required.

> Check the actions actually available on our authenticated hosted connection. If the information we need is not available, stop with a clear missing-step checklist. Do not change store records.

## What to expect

1. Describe the business question and the Agiliron account you are authorized to use.
2. Review the provider's account and API-key requirements in PipMCP.
3. Import or configure the relevant actions if they are not already available.
4. Use an authenticated hosted endpoint to inspect available actions before attempting business work.

A successful connection check means the endpoint answered. It does not establish that an inventory report ran, an order changed or an account has the permissions needed for your task.

## Account access

[Open Agiliron setup in PipMCP](https://pipmcp.com/register?app=agiliron&utm_source=github&utm_campaign=github-agiliron-mcp).

Use an authenticated PipMCP connection for real checks. Keep the hosted access token and provider credentials in local secret settings or the product's connection settings, outside conversations and repository files. Ask the assistant to stop if the required account or token is missing.

The current helper uses a configured hosted endpoint and token. Its local setup inspection can explain requirements without contacting the provider. Ask your coding assistant to read the project files before selecting its setup or live-discovery mode.

## Provider references

- [Agiliron getting started](https://api.agiliron.com/reference/getting-started)
- [Agiliron developer information](https://www.agiliron.com/developers/)

This project is maintained independently. Provider documentation and a catalog listing do not establish verified account access or endorsement.

<details>
<summary>Original project reference</summary>

# Agiliron MCP setup and connection checker

Generate Agiliron MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect agiliron

[Create or sign in to PipMCP](https://pipmcp.com/register?app=agiliron&utm_source=github&utm_campaign=github-agiliron-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=agiliron&utm_source=github&utm_campaign=github-agiliron-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: 5049ddf0fab1e8afcd49bf3e6ede733f964a0955f9a62a5ff4d08db23ed45013. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "api_key_query",
  "requiredCredentialFields": [
    "api_key"
  ],
  "requiredHeaderNames": [],
  "helpUrl": "https://www.agiliron.com/developers/",
  "tenantRequired": true,
  "accountParameterNames": []
}
```

Provider documentation: https://api.agiliron.com/reference/getting-started
Provider website: https://www.agiliron.com/


</details>
