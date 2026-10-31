# relayEquipmentManager (bigEricPool fork)

This fork of [rstrouse/relayEquipmentManager](https://github.com/rstrouse/relayEquipmentManager) follows the same layout as the companion forks [bigEricPool/nodejs-poolController](https://github.com/bigEricPool/nodejs-poolController) and [bigEricPool/nodejs-poolController-dashPanel](https://github.com/bigEricPool/nodejs-poolController-dashPanel): one branch per change, cut from the original project's `master`, and a branch `pool` that contains all of them.

This page is the list of branches. `manifest.json` holds the same list for the build check, which runs `npm ci` and `npm run build` on every branch marked to build.

Base for new branches: master at 2460fae.

## In use

| Branch | Kind | Purpose | Depends on | Related report |
|---|---|---|---|---|
| `master` | mirror | Untouched copy of the original project's master. | none | none |
| `pool` | integration | Everything together; the branch the pool controller is to run. Built from the branches below, never edited directly. | local/npm, feature/thermistor-pullup | none |
| `local/npm` | local | package.json allowScripts and the audit-fix lock file. Not for upstream. | none | none |
| `feature/thermistor-pullup` | feature | A Pull-up setting on the 10k temperature probe (default 10,000 ohms); the Sequent Home Automation card has 15k on each analog input. | none | none |

## Being replaced

| Branch | Kind | Purpose | Depends on | Related report |
|---|---|---|---|---|
| `autoswg-rem` | integration | The branch the pool controller runs today: master plus the package update. Replaced by pool. | none | none |

## Kept for history

| Branch | Kind | Purpose | Depends on | Related report |
|---|---|---|---|---|
| `fix/relay-shutdown` | archive | Relays off on a clean shutdown. Superseded: the owner merged his own fix. | none | rstrouse/relayEquipmentManager#124 (closed) |
| `fix/ssdp` | archive | SSDP server start-up on a host with several network interfaces. Superseded: fixed by the owner. | none | rstrouse/relayEquipmentManager#125 (closed) |

This page is written with the help of an AI assistant (Claude) and reviewed by the owner.
