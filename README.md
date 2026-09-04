### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train closed its last proof link — the full chain, fresh
install to scored scenario, is validated end to end — and shipped its
control plane: a server state machine with an SSE event bus, an
eight-page control-centre UI, a live drill queue, watchdogs and daily
backups, 75/75 tests. Only the human play-test is left. On the ops side,
the radar agent went mining the heal ledger and found it had never
existed — install.sh shipped 8 of 10 tools, so the self-healers were
never deployable; the installer is fixed and regression-bound (pi-cicd
e4c1293), and re-running it on the box is the pending step. Next pick on
the board: Grafana step 2 — one pinned dashboard, alerting through
ntfy_lib. Prometheus 2.53.3 + node_exporter keep scraping loopback-bound
at ~102 MB. The burst worker still handles the heavy jobs — load-aware
routing to disposable Codespaces, resource-capped Docker jobs, artifacts
shipped back, a budget ledger that refuses to exhaust the free tier. The
Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, and a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (mining the heal ledger caught two it had never linked)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach: CounterStrikeSharp plugin measuring real mechanics server-side, 495 scenarios, deliberate-practice sessions, and a control centre — server state machine, SSE event bus, live drill queue — validated end to end on a fresh install (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
