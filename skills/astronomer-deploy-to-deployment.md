---
name: Deploy an image or DAGs to a Deployment
description: Push new pipeline code to an Astro Deployment via the deploy lifecycle (create, finalize) and roll back if needed.
api: openapi/astronomer-astro-openapi-original.yml
operations:
  - ListDeployments
  - CreateDeploy
  - FinalizeDeploy
  - GetDeploy
  - DeployRollback
---

# Deploy code to an Astro Deployment

Ship a new image deploy or DAG-only deploy to a running Deployment.

## Auth
`Authorization: Bearer <token>` (Deployment, Workspace, or Organization token).
Base URL `https://api.astronomer.io/v1`.

## Steps
1. **Find the Deployment** — call `ListDeployments` under
   `/organizations/{organizationId}/deployments` to resolve the `deploymentId`.
2. **Start a deploy** — call `CreateDeploy` under
   `/organizations/{organizationId}/deployments/{deploymentId}/deploys`, specifying
   the deploy type (image deploy vs DAG deploy). Capture the returned `deployId`
   and any upload target it returns.
3. **Upload artifacts** — push your image/DAG bundle to the location the create step
   provides (per the deploy response).
4. **Finalize** — call `FinalizeDeploy` for that `deployId` to promote the deploy.
5. **Verify** — poll `GetDeploy` until the deploy status is complete.
6. **Roll back if needed** — call `DeployRollback` to revert the Deployment to a
   previous successful deploy.

## Conventions & errors
- Deploy lists are paginated (`offset`/`limit`/`totalCount`).
- On failure inspect the `{message, requestId, statusCode}` envelope; a `409`
  Conflict usually means a deploy is already in progress.
- Prefer the Astro CLI (`astro deploy`) for interactive/CI use; this flow is for
  programmatic control (`cli/astronomer-cli.yml`).
