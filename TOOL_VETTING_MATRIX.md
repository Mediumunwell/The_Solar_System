# Tool Vetting Matrix

Status values:
- install-now
- sandbox-test
- reject

| Item | Source URL | Maintainer Verified | Update Cadence | Permission Scope Acceptable | Reproducible Install Docs | Decision | Notes |
|---|---|---|---|---|---|---|---|
| superpowers | TBD | TBD | TBD | TBD | TBD | sandbox-test | Collect provenance first. |
| claude-mem | TBD | TBD | TBD | TBD | TBD | sandbox-test | Validate storage location and data policy. |
| awesome-claude-code | TBD | TBD | TBD | TBD | TBD | sandbox-test | Curated list; each dependency must be vetted separately. |
| ui-ux-pro-max-skill | TBD | TBD | TBD | TBD | TBD | sandbox-test | Confirm author identity and exact capabilities. |

## Gate Checklist
1. Provenance: official repo/account and signed releases if available.
2. Maintainer: identifiable owner and track record.
3. Security: least privilege permissions and clear data handling.
4. Reproducibility: deterministic install and uninstall steps.
5. Rollback: tested removal path and config cleanup.
