### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: the box graphs itself. Prometheus 2.53.3 + node_exporter went
live from Debian packages, loopback-bound, with the scrape config under
test — ~102 MB RSS answered the "do the graphs earn their RAM?" question
with a yes. Next on the radar: Grafana step 2 (one pinned dashboard,
alerting through ntfy_lib), then mining the heal ledger to retire the
busiest self-heal. The CS2 training platform (Hermes Train) is in its
final validation — the last link, plugin load proven on a fresh server
with a real player in the seats, is staged and waiting on one pod run.
The burst worker still handles the heavy jobs — load-aware routing to
disposable Codespaces, resource-capped Docker jobs, artifacts shipped
back, a budget ledger that refuses to exhaust the free tier. The Pi stays
the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, and a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — plus a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach: CounterStrikeSharp plugin measuring real mechanics server-side, 495 scenarios, deliberate-practice sessions (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
