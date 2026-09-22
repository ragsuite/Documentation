---
title: "Authentication"
description: "RAGSuite Community auth — password login, 2FA and sessions; SSO is Enterprise."
sidebarTitle: "Authentication"
icon: "key"
---

## Community

| Capability | Status |
|------------|--------|
| Password authentication | Community |
| 2FA & sessions | Community |
| Invites / forgot-password email | Requires working [SMTP](/GettingStarted/Configuration/Index) |

Configure JWT and SMTP in `.env` before production use. `JWT_SECRET_KEY` must be a long random secret.

## Enterprise

**SSO** with **Google OIDC** is an Enterprise module. See [SSO](/Enterprise/SSO/Index).

Organization RBAC (teams, orgs, members, and project access) is also Enterprise — see [Organization & RBAC](/Enterprise/OrganizationAndRBAC/Index).

## API access

Service integrations typically use API keys (`rgs_live_*` / `rgs_test_*` patterns in the CE auth docs). See [API keys & webhooks](/Platform/APIKeysAndWebhooks/Index).

## Interactive tour

<Frame>
  <div className="rg-supademo">
    <iframe
      src="https://app.supademo.com/embed/cmucit0xr16gcqm06z3l4dpab"
      title="RAGSuite Profile — interactive demo"
      loading="lazy"
      allow="clipboard-write"
      allowFullScreen
    />
  </div>
</Frame>
