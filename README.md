### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: an overnight agent loop writes the devlog and ships one idea a
day — latest, nightly chaos drills that break the box on purpose and check
it notices: a dead-port drill driven through the real probe pipeline, an
ntfy fail-closed check, a timer-liveness probe, receipts read back off the
topic. The hourly CI audit grew a self-healing edition too — it pushes
stranded commits, re-enables stopped deploy timers and re-runs failed runs
itself, paging only for real bugs. Under it all: five-minute uptime probes
with a live scoreboard in the ops portal, borg backups with a
byte-comparing restore drill, an upstream release watcher, and a morning
self-audit that checks every project on the box (and resets a wedged SDR
dongle on its own).

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk
- [cs2-dashboard](https://github.com/pkia/cs2-dashboard) — live pro-CS2 tracker

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
