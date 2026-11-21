```
   *     *
 *   * *   *
   *  *  *
    \ | /
     \|/
  ----+----  P E R M E S I
     /|\
    / | \
   *  *  *
 *   * *   *
   *     *
```

# Permesi

Permesi is an open-source, self-hosted identity and access management platform
written in Rust. It gives teams a place to manage how users sign in, what
applications can access, and who can administer each organization.

The project has three goals.

- **Protect user credentials.** Users can sign in with passkeys or use OPAQUE
  password authentication, which keeps the password from being sent to the
  server. Accounts can also use multi-factor authentication.
- **Keep application access scoped to each organization.** Teams manage OAuth
  clients and permissions by project, environment, and application in the web
  console. Applications integrate through OAuth 2.0 and OpenID Connect using
  the authorization code flow with PKCE.
- **Make the trust boundary explicit.** Genesis issues short-lived admission
  tokens at the public edge. The core Permesi service checks those tokens
  locally and handles sign-in, consent, and OAuth token issuance.

## Get started

- [Source code and local quickstart](https://github.com/permesi/permesi)
- [API documentation](https://permesi.github.io/permesi/)
- [Project roadmap](https://github.com/permesi/permesi/blob/main/TODO.md)
