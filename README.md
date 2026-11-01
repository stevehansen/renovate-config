# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) preset for my repos.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>stevehansen/renovate-config"]
}
```

- All minor/patch updates grouped into one PR, created Monday before 6am (Europe/Brussels).
- That PR automerges when every status check passes. No CI → it waits for a manual merge.
- Majors: separate PRs, never automerged.
- New releases wait 3 days before being proposed (supply-chain buffer).
- Security fixes from Dependabot alerts skip the schedule and the wait.
- Repo-level `packageRules` (holds, caps, extra groups) still apply on top.
