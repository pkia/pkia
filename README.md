### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train's coach grew a brain — a 44-skill genome with
root-cause diagnosis, adaptive session generation, demo-coach analysis, and
weekly reports that answer "what should I train" with data, or honestly with
"not enough data" (149 tests). The server-side chain is proven end to end with
bots; the human play-test is the last link. Two of the box's earlier verdicts
got corrected by evidence the same day: the 14-hour pod dry spell was a
snake_case parse bug, not the cloud (fixed, regression-locked), and the
self-healers were Hermes-cron jobs, live and green all along — the empty heal
ledger just means a healthy box (pi-cicd f925967). The practice server never
needed a GPU, so server_manager gained a Hetzner provider for GPU-free
hosting. Next pick on the radar board: Grafana step 2 — one pinned dashboard,
alerting through ntfy_lib. Prometheus 2.53.3 + node_exporter keep scraping
loopback-bound at ~102 MB. The burst worker still handles the heavy jobs —
load-aware routing to disposable Codespaces, resource-capped Docker jobs,
artifacts shipped back, a budget ledger that refuses to exhaust the free
tier. The Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, and a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (a ledger dig that once cried "never deployed" corrected itself: the healers were Hermes-cron jobs all along)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — twelve ledger entries and counting
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach: CounterStrikeSharp plugin measuring real mechanics server-side, 495 scenarios, deliberate-practice sessions, and a coach brain (skill genome, adaptive sessions, demo analysis) — game server on GPU-free Hetzner boxes, control plane on the Pi (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
