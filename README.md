### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train passed its release-candidate verdict on 09-07 and
immediately started behaving like a product. The overnight sprint since:
the CI heal retired for good (the last two hermeticity failures fixed
09-08 in `aa54bd4` — first fully green run since 09-05, and the root cause
was never a flake: CI runners just lack the deployed `~/.hermes` tooling);
two agents (Hermes + ZCode) now share the repo under a written
AGENTS.md/WORKLOG protocol; the coach app was redesigned map-first with
Player DNA as the signature screen and honest empty states everywhere;
START TRAINING composes a real, explainable coach prescription from the
player model; difficulty is now a continuous confidence-aware vector; an
arena trainer landed with procedurally spawned targets, five transparent
score dimensions and a personal-best store; and practice bots grew reaction
time + aim control implemented natively on CounterStrikeSharp (35,840-byte
plugin DLL live on the Hetzner box) — 315+ tests green. The last gate is
still a human in the seat for `!train start`; moving xfire-style bot
behaviour is the next increment. On the box, the radar board's heal-ledger
mine is Done with receipts; prom-dash stays Done; prom step 3 (ntfy
/metrics + the alerting-consumer decision) is the queued half. The burst
worker still handles the heavy jobs — load-aware routing to disposable
Codespaces, resource-capped Docker jobs, artifacts shipped back, a budget
ledger that refuses to exhaust the free tier. The Pi stays the brain; the
worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test) — and prom-dash, the stdlib answer to Grafana step 2 (Grafana isn't even in Debian trixie): pinned CPU-vs-load and unit-state graphs as one on-demand HTML page, ~0 MB resident, now recorded Done on the radar board with receipts — plus a tested architecture reference for the whole box, and an installer regression-bound to ship every tool (a ledger dig that once cried "never deployed" corrected itself: the healers were Hermes-cron jobs all along)
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — thirteen ledger entries and counting; the heal-ledger mine paid out 09-07 (`9e78d03`: five "flake?" heals were one ruff F821) and closed itself 09-08 (`aa54bd4`, first fully green CI since 09-05, heal retired with receipts); next up from Proposed: prom step 3 (ntfy alerting) and staging the Train proof run
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach, release candidate and now mid post-RC sprint: CounterStrikeSharp plugin measuring real mechanics server-side (497 scenarios), a redesigned map-first coach app, a routine generator that actually prescribes, an arena trainer with personal bests, and practice bots with real reaction time + aim — 315+ tests, last gate still a human in the seat (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
