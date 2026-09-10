### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train passed its release-candidate verdict on 09-07 and has
been behaving like a product ever since — two agents (Hermes + ZCode) share
the repo under a written AGENTS.md/WORKLOG protocol, the coach app is
redesigned map-first with Player DNA and honest empty states, START TRAINING
composes a real, explainable prescription, an arena trainer landed with
procedurally spawned targets and a personal-best store, and practice bots
grew reaction time + aim control implemented natively on CounterStrikeSharp.
The day after that sprint the wave industrialised trust instead of features:
a scenario truth-audit engine with deterministic verdicts ran over all 581
scenarios — 99 spray labels made honest, a contract on every scenario — a
crosshair-placement scoring dimension landed from angle-error telemetry, v4
telemetry added per-engagement acquisition with prefire route gating,
blind-review QA shipped with a dimension-aware false-progress detector,
real-geometry spatial validation went in, the UI was rebuilt as the "CT/T
Combat Lab", and a security pass moved runtime data out of the repo. The
last gate is still a human in the seat for `!train start`; moving xfire-style
bot behaviour is the next increment. On the box, prom step 3a shipped 09-09
(ntfy's own `/metrics` scraped on loopback :9091 into the same Prometheus —
220/220 pytest, live `up=1`); step 3b, the alerting-consumer decision, is the
open radar item, and the Train autopilot now has a public framework repo and
a documented 04:45 cron. The burst worker still handles the heavy jobs —
load-aware routing to disposable Codespaces, resource-capped Docker jobs,
artifacts shipped back, a budget ledger that refuses to exhaust the free
tier. The Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — and prom-dash, the stdlib answer to Grafana step 2 (Grafana isn't even in Debian trixie): pinned CPU-vs-load and unit-state graphs as one on-demand HTML page, ~0 MB resident, now recorded Done on the radar board with receipts; step 3a followed 09-09 — ntfy's own `/metrics` scraped on loopback :9091, 220/220 pytest, live `up=1` — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (a ledger dig that once cried "never deployed" corrected itself: the healers were Hermes-cron jobs all along)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — fifteen ledger entries and counting; the heal-ledger mine paid out 09-07 (`9e78d03`: five "flake?" heals were one ruff F821) and closed itself 09-08 (`aa54bd4`, first fully green CI since 09-05, heal retired with receipts); prom step 3a shipped 09-09 (ntfy `/metrics` on loopback :9091, 220/220 pytest, live up=1); the open item is step 3b, the alerting-consumer decision — plus staging the Train proof run once the human gate passes
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach, release candidate and now mid post-RC sprint: CounterStrikeSharp plugin measuring real mechanics server-side (497 scenarios), a redesigned map-first coach app, a routine generator that actually prescribes, an arena trainer with personal bests, practice bots with real reaction time — then a validity pass that audited the whole corpus for truth (deterministic audit engine, honest spray labels, contracts on all 581 scenarios, a false-progress detector); last gate still a human in the seat (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
