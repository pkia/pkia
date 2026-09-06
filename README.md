### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train's coach grew past brains into judgement — a Player
Intelligence layer where every training decision lands in an intelligence
ledger with its reasoning and epistemic tier, Player DNA and briefings
explain the why, and self-evaluation hooks grade the coach's own calls
(199 tests, up from 149). The server-side chain is proven end to end with
bots; the human play-test is the last link — and when the evidence isn't
there, the coach says "not enough data" instead of inventing an answer. On
the box, Prom stack step 2 resolved itself: Grafana isn't in Debian trixie,
so the pinned dashboard shipped as prom-dash, a stdlib script rendering
CPU-vs-load and unit-state graphs on demand at ~0 MB resident (alerting
through ntfy_lib next). Prometheus 2.53.3 + node_exporter keep scraping
loopback-bound at ~102 MB. The burst worker still handles the heavy jobs —
load-aware routing to disposable Codespaces, resource-capped Docker jobs,
artifacts shipped back, a budget ledger that refuses to exhaust the free
tier. The Pi stays the brain; the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — and prom-dash, the stdlib answer to Grafana step 2 (Grafana isn't even in Debian trixie): pinned CPU-vs-load and unit-state graphs as one on-demand HTML page, ~0 MB resident — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (a ledger dig that once cried "never deployed" corrected itself: the healers were Hermes-cron jobs all along)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — twelve ledger entries and counting
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach: CounterStrikeSharp plugin measuring real mechanics server-side, 495 scenarios, deliberate-practice sessions, and a coach brain with Player Intelligence (decision ledger, Player DNA, briefings, honest "not enough data", 199 tests) — game server on GPU-free Hetzner boxes, control plane on the Pi (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
