---
name: Manage Teams, membership, and RBAC roles
description: Create a Team, add members, and grant role-based access using Astro's RBAC roles and permission groups.
api: openapi/astronomer-astro-openapi-original.yml
operations:
  - ListRoles
  - CreateTeam
  - AddTeamMembers
  - UpdateTeamRoles
  - ListPermissionGroups
---

# Manage Teams and RBAC on Astro

Set up a Team, populate it, and grant it the right roles.

## Auth
`Authorization: Bearer <token>` with an Organization token that can administer
Teams/roles. Base URL `https://api.astronomer.io/v1`.

## Steps
1. **Discover roles** — call `ListRoles` (and `ListPermissionGroups` under the
   Authorization tag) to learn the available role templates and the permission
   groups they grant, so you assign least privilege.
2. **Create the Team** — call `CreateTeam` under
   `/organizations/{organizationId}/teams` with a name and description; capture the
   `teamId`.
3. **Add members** — call `AddTeamMembers` with the `memberIds` (user ids) to add
   to the Team.
4. **Grant roles** — call `UpdateTeamRoles` to bind Organization/Workspace/Deployment
   roles to the Team so members inherit them.

## Conventions & errors
- `AddTeamMembers` requires at least one member id (`minItems: 1`).
- Member/role changes take effect immediately for the Team's users.
- A `404` means the Team, user, or role id is wrong or out of the token's scope.
- Prefer Teams + roles over per-user grants for maintainable RBAC.
