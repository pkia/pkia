### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: the self-healer shows its work. Every fix pipeline-check makes
lands in a bounded status.json ledger with before→after detail, the portal
renders a Self-healing panel fed by /api/heals, and pi-doctor's morning
audit counts the last 24h of heals — proven by a hermetic end-to-end test
that drives a real heal against a bare remote. Next on the radar: a
Prometheus + Grafana stack from Debian packages (one pinned dashboard,
alerting through ntfy), then mining the heal ledger to fix whatever
self-heals most often. The burst worker still handles the heavy jobs —
load-aware routing to disposable Codespaces, resource-capped Docker jobs,
artifacts shipped back, a budget ledger that refuses to exhaust the free
tier. The Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows — plus a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk
- [cs2-dashboard](https://github.com/pkia/cs2-dashboard) — live pro-CS2 tracker

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
