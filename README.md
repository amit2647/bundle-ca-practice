# bundle-ca-practice

The **CA Practice** profession bundle for OmniCore: what a chartered accountancy firm needs,
as versioned data — never code. bundle-service installs it into an organization.

| File | Holds |
|---|---|
| `bundle.yaml` | The manifest: vocabulary, client fields, identifiers, people roles, pipeline, and references to the rest |
| `schemas/`, `ui/` | Client and lead field schemas (JSON Schema) and their form layout |
| `catalog.yaml` | The 12 services in 5 groups, and packages |
| `roles.yaml` | Role templates: Partner, Audit Manager, Article Assistant, Accounts Executive |
| `email/` | Deadline reminders — installed switched off |
| `knowledge/` | Help docs for the assistant |
| `fixtures/clients/` | Sample clients for bundle-lint's dry run |

Deadline rules, engagement types, document templates and portals arrive with their milestones.

```bash
npx --yes --package=https://codeload.github.com/amit2647/bundle-sdk/tar.gz/572a3c251063c08b6578b54e414a737c261ce575 bundle-lint .
```

Keys (services, roles, rules…) are permanent once released. Version with semver: bundle-lint
checks the bump against the previous release (`--previous`), and a breaking change needs a
major version with `upgrades` steps.
