### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: the Pi learned to burst. Heavy jobs now spill onto a disposable
cloud worker (GitHub Codespaces, free tier) through a small provider
abstraction — a load-aware router decides local vs cloud, jobs run in
resource-capped Docker containers, artifacts ship back, and a budget ledger
refuses to provision past 95% of the free core-hour allowance. The Pi stays
the brain; the worker is cattle, not a pet. Alongside it: weekly memory
consolidation and a Sunday token-economy digest keep the resident agent
lean, and the hourly CI audit now self-heals — re-running flakes, pushing
stranded commits — instead of paging.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk
- [cs2-dashboard](https://github.com/pkia/cs2-dashboard) — live pro-CS2 tracker

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
