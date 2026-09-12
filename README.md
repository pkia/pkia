### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: rebuilding the drill engine of Hermes Train around
OpenPrefirePrac — MIT, pinned by version and sha256 — and closing the audit
findings that started it. The suite went from 636 to 808 tests, seven revert
experiments each redden on the expected witness, and a live box logs drills
end to end. Proved to run, not yet proved to work — the last gate is a human
in the seat.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: pull-based deploys with auto-rollback, dead-man's switches, borg backups with restore drills, Prometheus metrics + alerting, a self-healing CI audit — and a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — an idea ledger an overnight agent loop works through, one ship a day; every run and every failure is public
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach: server-side mechanics measurement, deliberate-practice sessions, 587 scenarios (repo private, project tour public)
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + NOAA satellite imagery on a kitchen kiosk
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
