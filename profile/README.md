<p align="center">
  <img src="permesi-original.svg" alt="Permesi" width="420">
</p>

<p align="center">
  <strong>Open-source, self-hosted identity and access management and OpenID Connect provider, written in Rust.</strong>
</p>

<p align="center">
  <a href="https://github.com/permesi/permesi">Source</a> ·
  <a href="https://permesi.github.io/permesi/">API docs</a> ·
  <a href="https://github.com/permesi/permesi/blob/main/TODO.md">Roadmap</a> ·
  <a href="https://github.com/permesi/permesi-helm">Helm charts</a>
</p>

---

Permesi gives teams one place to manage how users sign in, what applications
can access, and who can administer each organization.

## Why Permesi

**🔐 Protect user credentials**
Users sign in with passkeys or with OPAQUE password authentication, which runs
on the client so the password is never sent to the server. Accounts can add
multi-factor authentication with TOTP, security keys, and recovery codes.

**🏢 Scope access to each organization**
Resources follow an Organization → Project → Environment → Application
hierarchy. From the web console, teams manage each application's OAuth clients,
redirect URIs, and API scopes. Applications integrate through OAuth 2.0 and
OpenID Connect using the authorization code flow with PKCE.

**🧱 Make the trust boundary explicit**
Public edge traffic is kept apart from core identity logic:

| Component       | Role                                                                                       |
| --------------- | ------------------------------------------------------------------------------------------ |
| **Genesis**     | Runs at the public edge and issues short-lived, signed admission tokens.                   |
| **Permesi**     | Verifies admission tokens locally and handles sign-in, consent, and OAuth token issuance.  |
| **Web console** | Rust/WebAssembly admin console for organizations, applications, users, and account security. |

Services are stateless and share PostgreSQL. OpenBao provides signing keys,
encryption, and database credentials.

## Get started

| | |
| --- | --- |
| 📦 **[permesi/permesi](https://github.com/permesi/permesi)** | Source code, architecture, and a local quickstart |
| ⎈ **[permesi/permesi-helm](https://github.com/permesi/permesi-helm)** | Helm charts for deploying to Kubernetes |
| 📖 **[API documentation](https://permesi.github.io/permesi/)** | Reference for the HTTP API |
| 🗺️ **[Roadmap](https://github.com/permesi/permesi/blob/main/TODO.md)** | What's planned next |

## Contributing

Issues and pull requests are welcome. Start with the
[contributing guide](https://github.com/permesi/permesi/blob/main/CONTRIBUTING.md)
and the [AI policy](https://github.com/permesi/permesi/blob/main/AI_POLICY.md).
Permesi is released under the
[BSD 3-Clause License](https://github.com/permesi/permesi/blob/main/LICENSE).
