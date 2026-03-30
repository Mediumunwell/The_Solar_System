# Tool Vetting Matrix

Status values:
- install-now
- sandbox-test
- reject

| Item | Source URL | Maintainer Verified | Update Cadence | Permission Scope Acceptable | Reproducible Install Docs | Decision | Notes |
|---|---|---|---|---|---|---|---|
| superpowers | https://github.com/obra/superpowers | yes (obra / Jesse Vincent) | active (updated 5 days ago, tagged releases) | partial (broad workflow automation; test in sandbox first) | yes (marketplace and cross-platform install docs) | sandbox-test | Treat as high-capability plugin; apply command/path guardrails before broad use. |
| claude-mem | https://github.com/thedotmack/claude-mem | yes (thedotmack / Alex Newman) | active (updated 2 days ago, frequent releases) | partial (captures and stores session data; review data handling first) | yes (plugin install + dedicated docs site) | sandbox-test | Requires explicit storage/privacy review before install on primary workflow. |
| awesome-claude-code | https://github.com/hesreallyhim/awesome-claude-code | yes (hesreallyhim) | active (updated within hours) | n/a (curated index, not a runtime plugin) | n/a (resource list, not an installer) | reject | Use as discovery source only; do not install directly. Vet each linked dependency separately. |
| ui-ux-pro-max-skill | https://github.com/nextlevelbuilder/ui-ux-pro-max-skill | partial (public maintainer identity present; independent trust not yet established) | active (updated within days, tagged releases) | partial (can generate/install skill assets across assistants) | yes (marketplace + CLI install/uninstall docs) | sandbox-test | Validate generated files and command behavior in a disposable workspace first. |

## Gate Checklist
1. Provenance: official repo/account and signed releases if available.
2. Maintainer: identifiable owner and track record.
3. Security: least privilege permissions and clear data handling.
4. Reproducibility: deterministic install and uninstall steps.
5. Rollback: tested removal path and config cleanup.
