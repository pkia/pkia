### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train is a release candidate. The production-gate wave
landed 09-07: 54/54 live scenario executions passed on a real Hetzner CS2
server (6 maps × 3 modes), fourteen release gates green, verdict "human
acceptance required" — the last link is a real player in the seat for
`!train start`. The same morning the customer side went up: a public landing
page server-rendered from the live scenario registry (497 scenarios), real
accounts (stdlib scrypt, hashed bearer sessions, FREE/PRO/ADMIN), and a
customer SPA with a Train library, history and an honest "not enough data"
progress state — 251 tests green. The CI storm the 09-07 devlog diagnosed
was fixed by 05:32 the same day: one ruff F821 (skill_model unimported in
the self-eval hook, swallowed by a bare except) shipped as a one-line
import — CI back to 248/250, the two leftovers being pre-existing CI-only
hermeticity tests queued for fixing, after which the ci-rerun heal retires
itself. On the box, prom-dash is Done on the radar board with receipts
(220/220 tests, live 24-hour render); Prom step 3 (ntfy /metrics + the
alerting consumer decision) is the queued half. The burst worker still
handles the heavy jobs — load-aware routing to disposable Codespaces,
resource-capped Docker jobs, artifacts shipped back, a budget ledger that
refuses to exhaust the free tier. The Pi stays the brain; the worker is
cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — and prom-dash, the stdlib answer to Grafana step 2 (Grafana isn't even in Debian trixie): pinned CPU-vs-load and unit-state graphs as one on-demand HTML page, ~0 MB resident, now recorded Done on the radar board with receipts — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (a ledger dig that once cried "never deployed" corrected itself: the healers were Hermes-cron jobs all along)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — thirteen ledger entries and counting; the heal-ledger mine paid out 09-07 (five ci-rerun heals were one ruff F821, fixed in cs2-train `9e78d03`); two CI-only hermeticity tests remain before the heal retires, then prom step 3 (ntfy alerting)
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach, now a release candidate: CounterStrikeSharp plugin measuring real mechanics server-side, 497 scenarios, deliberate-practice sessions, a coach brain (intelligence ledger, Player DNA, honest "not enough data"), 54/54 live E2E on real Hetzner boxes, customer accounts + SPA — the last gate is a human in the seat (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
