---
title: "SSO"
description: "RAGSuite Enterprise SSO with Google or Microsoft Entra ID (OIDC) — single sign-on on your infrastructure."
sidebarTitle: "SSO"
icon: "log-in"
---

**Edition:** Enterprise

Single sign-on is an Enterprise module. RAGSuite supports two OIDC identity providers so your organization can sign in with the accounts it already uses:

- **Google**
- **Microsoft Entra ID**

Organization admins configure each provider on its own tab (**Google** / **Microsoft Entra**) in the **Single Sign-On** settings screen. You can enable one or both; the same email can be linked to both providers.

Community password auth and 2FA remain available without SSO — see [Authentication](/Console/Authentication/Index).

<Steps>
  <Step title="Confirm Enterprise entitlement">
    SSO requires an active Enterprise license. Complete [Activation](/Enterprise/Activation/Index) first.
  </Step>
  <Step title="Register RAGSuite with your identity provider">
    **Google:** in Google Cloud Console, create an OAuth client and add the **Google Console redirect URI** shown in RAGSuite.

    **Microsoft Entra ID:** in the Microsoft Entra admin center, create an app registration, add the **Redirect URI** shown in RAGSuite, and create a client secret.

    Keep client secrets out of shared documents and chat.
  </Step>
  <Step title="Configure SSO in RAGSuite">
    On the provider’s tab, enter:

    | Field | Google | Microsoft Entra ID |
    |-------|--------|--------------------|
    | Client ID | Google client ID | Application (client) ID |
    | Client secret | Google client secret | Client secret |
    | Directory (tenant) ID | — | Required — from Entra admin center › Overview |
    | Allowed email domains | Required | Required |
  </Step>
  <Step title="Test the connection">
    Use **Test connection** before enabling. It checks that the identity provider is reachable and that the client ID and secret are accepted.
  </Step>
  <Step title="Verify sign-in">
    Only **invited** team members whose email matches an allowed domain can sign in — accounts are not created automatically. Sign in with Google or Microsoft and confirm the user lands in the expected org and project access. Keep password auth available as a break-glass path until SSO is proven.
  </Step>
</Steps>

<Info>
Env flags such as `SSO_ENABLED` exist in CE templates for wiring; **product SSO requires Enterprise** entitlement and configuration. RAGSuite SSO uses **OIDC** with Google or Microsoft Entra ID.
</Info>

## Interactive tour

<Frame>
  <div className="rg-supademo">
    <iframe
      src="https://app.supademo.com/embed/cmucejn4p0w7vqm06u2zdz33v"
      title="RAGSuite Google SSO — interactive demo"
      loading="lazy"
      allow="clipboard-write"
      allowFullScreen
    />
  </div>
</Frame>
