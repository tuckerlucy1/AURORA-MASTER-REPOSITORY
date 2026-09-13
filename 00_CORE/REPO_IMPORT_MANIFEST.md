# Aurora Master — Repository Import Manifest

**Purpose:** preserve source repositories before canonical integration.

## Import policy

1. Preserve each upstream repository intact.
2. Record repository name, source branch, commit/tree SHA, and import date.
3. Never flatten repositories into the master root during first-pass import.
4. Keep binary archives as source artifacts when available.
5. Integrate code only after provenance and overlap review.
6. Do not commit secrets, credentials, private keys, or live signing material.

## Initial import set

| Master area | Source repository | Status |
|---|---|---|
| `01_AURORA_MESH/aurora-mesh/` | `tuckerlucy1/aurora-mesh` | source verified; contains `aurora-mesh-v1.3-runnable.zip` |
| `02_TRADING/PulseTrade/` | `tuckerlucy1/PulseTrade` | queued |
| `02_TRADING/TradingAgents/` | `tuckerlucy1/TradingAgents` | queued |
| `03_WEB3/aurora-solana-ecosystem/` | `tuckerlucy1/aurora-solana-ecosystem` | queued |
| `03_WEB3/ecosystem-v2/` | `tuckerlucy1/ecosystem-v2` | queued |
| `04_GLOW/Glow_Dashboard/` | `tuckerlucy1/Glow_Dashboard` | queued |
| `04_GLOW/glow-awol-bitcoin/` | `tuckerlucy1/glow-awol-bitcoin` | queued |
| `05_GENESIS/Genesis/` | `tuckerlucy1/Genesis` | queued |
| `06_PHONE/phone-guard-scan/` | `tuckerlucy1/phone-guard-scan` | queued |
| `06_PHONE/usb-trader/` | `tuckerlucy1/usb-trader` | queued |

## Aurora Mesh provenance

- Repository: `tuckerlucy1/aurora-mesh`
- Branch: `main`
- Current tree SHA: `edcb1a887214ecadf1732dba4a2de5441f4733b4`
- Existing archive: `aurora-mesh-v1.3-runnable.zip`
- Archive blob SHA: `9bd695e44f3541d2f12b23f45b7aad45d315aca8`
- Source repository remains the authoritative copy until an explicit canonical integration commit is made.

## Verification rule

A repository is not considered integrated merely because a directory exists in this master repository. Integration is complete only after source provenance, file overlap, dependency conflicts, secrets scanning, and runtime validation are recorded.
