# PFC-PROD — PF-Core Production

PF-Core **production** tier — tagged releases auto-distribute to all PFI triads.

| Field | Value |
|---|---|
| **Tier** | prod (team mode — 1 review + SME approval) |
| **Triad** | [pfc-dev](https://github.com/ajrmooreuk/pfc-dev) · [pfc-test](https://github.com/ajrmooreuk/pfc-test) · [pfc-prod](https://github.com/ajrmooreuk/pfc-prod) |
| **Architecture** | Hub-and-Spoke (ARCH-CICD-001) |
| **Epic** | [Epic 58 (#837)](https://github.com/ajrmooreuk/Azlan-EA-AAA/issues/837) |

## Release Process

```bash
# Tag a release (triggers pfc-release.yml → all PFI dev repos)
git tag pfc-v2.0.0
git push origin pfc-v2.0.0
```

## What Gets Distributed

| Component | Target | Filter |
|---|---|---|
| Ontology registry (filtered) | PFI dev repos | By subscribed series |
| Sealed skills | PFI dev repos | All PFIs |
| Graph scope rules | PFI dev repos | Per-PFI config |
| guard-core.yml | PFI dev repos | All PFIs |

## PFI Targets (from ont-registry-index.json)

| PFI | Series | Dev Repo |
|---|---|---|
| BAIV | VE, PE, RCSG, Foundation, Orchestration | pfi-baiv-aiv-dev |
| AIRL-CAF-AZA | VE, PE, RCSG, Foundation, Orchestration | pfi-airl-caf-aza-dev |
| W4M-WWG | VE, PE, Foundation, Orchestration | pfi-w4m-wwg-dev |
| W4M-EOMS | VE, PE, RCSG, Foundation, Orchestration | pfi-w4m-eoms-dev |
| VHF | VE, PE, Foundation, Orchestration | pfi-vhf-nutrition-app-dev |
