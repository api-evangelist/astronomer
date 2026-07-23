---
name: Create, scope, rotate, and revoke API tokens
description: Manage Astro API tokens end to end — create a token scoped to an Organization or Workspace, bind roles, rotate the secret, and revoke.
api: openapi/astronomer-astro-openapi-original.yml
operations:
  - ListApiTokens
  - CreateApiToken
  - UpdateApiTokenRoles
  - RotateApiToken
  - DeleteApiToken
---

# Manage Astro API tokens

Provision and lifecycle-manage the bearer tokens that authenticate the Astro
Platform API.

## Auth
`Authorization: Bearer <token>` with an Organization token that has permission to
manage tokens. Base URL `https://api.astronomer.io/v1`.

## Steps
1. **Inventory** — call `ListApiTokens` to see existing tokens, their scope
   (Organization vs Workspace), and roles.
2. **Create** — call `CreateApiToken` with a name, the scope
   (`type: ORGANIZATION` or `WORKSPACE` + the entity id), an expiry, and the role
   to bind. The secret is returned **once** — store it securely.
3. **Adjust roles** — call `UpdateApiTokenRoles` to change the roles bound to an
   existing token without recreating it.
4. **Rotate** — call `RotateApiToken` to issue a new secret for the same token id
   (invalidates the old secret); update your secret store immediately.
5. **Revoke** — call `DeleteApiToken` to permanently revoke a token.

## Conventions & errors
- Token secrets are shown only at create/rotate time — never retrievable later.
- A `403` means the caller's own token lacks token-management permission.
- Rotate on a schedule and after suspected exposure; revoke unused tokens.
- See auth model in `authentication/astronomer-authentication.yml`.
