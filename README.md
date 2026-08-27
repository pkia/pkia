### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: an overnight agent loop writes the devlog and ships one idea a
day — latest, an upstream release watcher feeding digest notifications, on
top of borg backups with a byte-comparing restore drill, an ntfy
notification backbone, and a morning self-audit that checks every project
on the box.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts, borg backups + restore drills, release watching
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk
- [cs2-dashboard](https://github.com/pkia/cs2-dashboard) — live pro-CS2 tracker

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
