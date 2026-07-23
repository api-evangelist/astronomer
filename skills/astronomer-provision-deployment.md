---
name: Provision an Astro Deployment in a Workspace
description: Create a Workspace (if needed) and provision a new Astro Deployment (managed Airflow environment) within it, choosing valid cluster/deployment options.
api: openapi/astronomer-astro-openapi-original.yml
operations:
  - ListOrganizations
  - CreateWorkspace
  - GetClusterOptions
  - GetDeploymentOptions
  - CreateDeployment
  - GetDeployment
---

# Provision an Astro Deployment

Provision a managed Apache Airflow environment (a Deployment) on Astro.

## Auth
All calls use `Authorization: Bearer <token>` with an Organization or Workspace API
token. Base URL: `https://api.astronomer.io/v1`. Optionally pin a minor version with
the `X-API-Version` header.

## Steps
1. **Resolve the Organization** — call `ListOrganizations` to get the
   `organizationId` your token can access.
2. **Create (or reuse) a Workspace** — call `CreateWorkspace` under
   `/organizations/{organizationId}/workspaces` with a name and description. Capture
   the returned `workspaceId`.
3. **Fetch valid options** — call `GetDeploymentOptions` (and `GetClusterOptions`
   for dedicated clusters) to learn allowed executor types, worker queues, runtime
   versions, and sizing so you submit valid values.
4. **Create the Deployment** — call `CreateDeployment` under
   `/organizations/{organizationId}/deployments` with the `workspaceId`, a name, a
   runtime version, and executor/scheduler settings drawn from the options call.
5. **Confirm** — poll `GetDeployment` until the Deployment reports a healthy/created
   status before deploying code to it.

## Conventions & errors
- List calls are paginated with `offset`/`limit` and return `totalCount` (see
  `conventions/astronomer-conventions.yml`).
- Respect rate limits: POST 10/s per token.
- Errors return `{message, requestId, statusCode, fieldErrors}`; on `400` inspect
  `fieldErrors`, and quote `requestId` in support requests
  (`errors/astronomer-problem-types.yml`).
- Creates are **not** idempotent — do not blindly retry a `CreateDeployment` on
  timeout; re-list first.
