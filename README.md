### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: the box finally has a map of itself. pi-cicd's architecture
reference is complete — docs/units.md indexes all twelve running units
(schedule, config, state, ntfy topic) and docs/layers.md pages out each
operational layer, bound to reality by a test that fails if the map drifts.
Next on the radar: making the self-healing CI audit show its work (a
status.json of every heal, a portal panel, a daily heal count), then a
Prometheus + Grafana stack from Debian packages. The burst worker still
handles the heavy jobs — load-aware routing to disposable Codespaces,
resource-capped Docker jobs, artifacts shipped back, a budget ledger that
refuses to exhaust the free tier. The Pi stays the brain; the worker is
cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit — plus a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk
- [cs2-dashboard](https://github.com/pkia/cs2-dashboard) — live pro-CS2 tracker

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
