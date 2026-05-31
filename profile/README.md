# ehxlabs

**EHX** — infrastructure intelligence for Web3 and cloud-native teams. Product site: [ehxlabs.xyz](https://ehxlabs.xyz).

## Repositories

| Repository | Purpose |
|------------|---------|
| [`ehx-web`](https://github.com/ehxlabs/ehx-web) | Next.js frontend (TypeScript, Tailwind, shadcn/ui) |
| [`ehx-api`](https://github.com/ehxlabs/ehx-api) | FastAPI service layer |
| [`ehx-templates`](https://github.com/ehxlabs/ehx-templates) | Terraform, Kubernetes, Helm, Compose, Ansible templates |
| [`ehx-modules`](https://github.com/ehxlabs/ehx-modules) | Reusable Terraform modules and Helm charts |
| [`ehx-kb`](https://github.com/ehxlabs/ehx-kb) | Knowledge base + canonical roadmap (`docs/EHX_Roadmap.md`) |
| [`ehx-monitoring`](https://github.com/ehxlabs/ehx-monitoring) | Observability presets (Prometheus, Grafana, Loki, Tempo, Alertmanager) |

## Branch protection (`main`)

Core product repos require **pull request review** and **green CI** before merge to `main`:

| Repository | Required status check |
|------------|----------------------|
| `ehx-api` | `CI / ruff` |
| `ehx-web` | `CI / lint-and-build` |
| `ehx-kb` | `CI / docs-integrity` |

- **Policy & apply script:** [ehx-kb runbook — branch protection](https://github.com/ehxlabs/ehx-kb/blob/main/docs/runbooks/branch-protection-rules.md)
- **Local CI before push:** `./scripts/ci-check.sh` in each repo ([ci-before-push](https://github.com/ehxlabs/ehx-kb/blob/main/docs/runbooks/ci-before-push.md))
- **GitHub Free note:** enforced branch protection on **private** repos requires **Team/Pro** (or public repos). Until then, use PRs + green Actions as the social contract; run `ehx-kb/scripts/apply-branch-protection.sh` after plan upgrade.

## Planning

- Roadmap issues and milestones: **`ehx-kb`**
- Organization **Projects**: enable after granting automation tokens the `project` scope (see the **Enable GitHub Projects (token scope)** issue in `ehx-kb`).
