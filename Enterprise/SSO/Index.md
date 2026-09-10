---
title: "SSO"
description: "RAGSuite Enterprise SSO with Google OIDC — single sign-on on your infrastructure."
sidebarTitle: "SSO"
icon: "log-in"
---

**Edition:** Enterprise

Single sign-on is an Enterprise module. RAGSuite supports **Google OIDC** so your organization can sign in with your existing Google identity provider.

Community password auth and 2FA remain available without SSO — see [Authentication](/Console/Authentication/Index).

<Steps>
  <Step title="Confirm Enterprise entitlement">
    SSO requires an active Enterprise license. Complete [Activation](/Enterprise/Activation/Index) first.
  </Step>
  <Step title="Create a Google OIDC client">
    In Google Cloud Console, create an OAuth client for your RAGSuite console origin and redirect URI. Keep the client ID and secret offline.
  </Step>
  <Step title="Configure SSO in RAGSuite">
    Set Enterprise SSO settings for Google OIDC (client ID, secret, and redirect). Enable SSO only after the redirect URI matches your console URL.
  </Step>
  <Step title="Verify sign-in">
    Open the console, choose Google sign-in, and confirm a user lands in the expected org/project access. Keep password auth available as a break-glass path until SSO is proven.
  </Step>
</Steps>

<Info>
Env flags such as `SSO_ENABLED` exist in CE templates for wiring; **product SSO requires Enterprise** entitlement and configuration. This documentation covers **Google OIDC only**.
</Info>
