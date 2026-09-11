### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train is being audited into a product rather than a
prototype. The autopilot ran twenty cycles in twenty hours — each one
verifying its premise at HEAD, freezing an RFC before any code, dispatching a
red team before implementation and closing with evidence — which grew the
suite from 636 tests to 695 and filed sixteen follow-ups instead of quietly
forgetting them. The process then turned on the product itself: every
customer and operator surface is now classified with cited evidence (a route
existing is not evidence, unknown is never pass), and the findings that
matter are unhappy ones — a real customer's session never links to their own
Steam identity, two shipped controls answer HTTP 422, the 587-scenario
library is unreachable in the current UI, an insight number is printed at a
hundred times its real value, and the plugin token is public in the shipped
bundle. The last gate is still a human in the seat for `!train start`. On the
box, prom step 3 is closed: 09-09 scraped ntfy's own `/metrics` on loopback
:9091 into the loopback Prometheus, and 09-10 shipped the alerting half as a
stdlib rule-check rather than a second daemon — five rules, edge-triggered,
published through the same library the one-flag alert-storm mute covers,
249/249 tests plus a live sweep on real metrics. `ram-mode focus` now parks
the hobby stack so a work session gets its RAM back, without paging me about
the things it just parked. The burst worker still handles the heavy jobs —
load-aware routing to disposable Codespaces, resource-capped Docker jobs,
artifacts shipped back, a budget ledger that refuses to exhaust the free
tier. The Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test), prom-dash as the stdlib answer to Grafana (not in Debian trixie) and metric-alert reading those same metrics as five edge-triggered rules — disk, temperature, memory, failed units, dead scrape targets — published through the mute-able notification backbone, a `ram-mode` switch that parks the hobby stack for a work session, and a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — sixteen ledger entries and counting; the heal-ledger mine paid out 09-07 (`9e78d03`: five "flake?" heals were one ruff F821) and closed itself 09-08 (`aa54bd4`, first fully green CI since 09-05, heal retired with receipts); prom step 3 closed on 09-10 with the alerting half (metric-alert, stdlib rule-check, 249/249 pytest, live sweep) — the open items are staging the Train proof run and the human gate
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach, release candidate and now mid post-RC audit: CounterStrikeSharp plugin measuring real mechanics server-side (587 scenarios), a redesigned map-first coach app, a routine generator that actually prescribes, an arena trainer with personal bests, practice bots with real reaction time — then a validity pass over the whole corpus (audit engine, honest spray labels, contracts on every scenario, a false-progress detector), and now a product-wide feature inventory where a route existing is not evidence (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
