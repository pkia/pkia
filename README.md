### EV

I run self-hosted systems on a Raspberry Pi, 24/7 — ship tracking (AIS), NOAA
satellite decoding, and a handful of web apps. Tests on every push,
pull-based deploys, auto-rollback.

Right now: Hermes Train's audit turned into a rebuild. The hand-rolled drill
route logic is out and OpenPrefirePrac is in — MIT, pinned by version *and*
sha256, shipped in the box bundle — and the two independent reasons a drill
recorded nothing are both fixed: a global cvar that froze every bot, and an
end-post contract that answered HTTP 422 to a drill with no human shots. A live
box now logs 200 OK into the ledger, the suite went from 636 tests to 808, and
seven revert experiments each redden on the expected witness when a fix is
removed. Proved to run, not yet proved to work: headless bots are kicked
straight back off the shipped build (`placed 0/5`), no CS2 client can connect
from this Pi, and the last gate is still a human in the seat. The audit that
started it still stands — every customer and operator surface classified with
cited evidence (a route existing is not evidence, unknown is never pass) — with
the unhappy findings on the record: a real customer's session never links to
their own Steam identity, two shipped controls answer HTTP 422, the
587-scenario library is unreachable in the current UI, an insight number is
printed at a hundred times its real value, and the plugin token is public in
the shipped bundle. On the box, prom step 3 closed 09-10 — ntfy's own
`/metrics` scraped on loopback, the alerting half a stdlib rule-check rather
than a second daemon, five edge-triggered rules published through the
mute-able notification backbone — `ram-mode focus` parks the hobby stack so a
work session gets its RAM back, and the versioning bot now reads a deny-list
before adopting a directory instead of committing the drawer under the desk.
The burst worker still handles the heavy jobs — load-aware routing to
disposable Codespaces, resource-capped Docker jobs, artifacts shipped back, a
budget ledger that refuses to exhaust the free tier. The Pi stays the brain;
the worker is cattle, not a pet.

**Repos**

- [pi-cicd](https://github.com/pkia/pi-cicd) — the CI/CD pattern behind it all: health checks, auto-rollback, dead-man's switches, ntfy alerts + kill switch, borg backups + restore drills, release watching, uptime probes, nightly chaos drills, a self-healing CI audit that logs every fix to a ledger the portal shows, a Prometheus + node_exporter scrape backbone (~102 MB, loopback-bound, config under test), prom-dash as the stdlib answer to Grafana (not in Debian trixie) and metric-alert reading those same metrics as five edge-triggered rules — disk, temperature, memory, failed units, dead scrape targets — published through the mute-able notification backbone, a `ram-mode` switch that parks the hobby stack for a work session, a project guard with an adoption deny-list, a pi-doctor that reads those parks as expected state rather than reviving them, and a tested architecture reference for the whole box
- [radar](https://github.com/pkia/radar) — idea ledger an overnight agent loop works through, one ship a day — seventeen ledger entries and counting; the heal-ledger mine paid out 09-07 (`9e78d03`: five "flake?" heals were one ruff F821) and closed itself 09-08 (`aa54bd4`, first fully green CI since 09-05, heal retired with receipts); the 09-11 pick closed project-guard's unfiltered adoption (deny-list read at adopt time, denied directories left byte-identical, 254/254 pytest) — the open items are the Train drill's bot placement on the box and the human gate
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — a personal CS2 coach, release candidate and now mid rebuild: CounterStrikeSharp plugin measuring real mechanics server-side (587 scenarios) with OpenPrefirePrac v0.1.47 pinned as the drill engine, identity and map gate and telemetry kept in our own plugin, a redesigned map-first coach app, a routine generator that actually prescribes, an arena trainer with personal bests — and a product-wide feature inventory where a route existing is not evidence (repo private, project tour public)
- [shelfmate](https://github.com/pkia/shelfmate) — paste a Goodreads profile, get book recommendations with reasons
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — AIS + satellite imagery on a kitchen kiosk

More on GitHub: [cs2-dashboard](https://github.com/pkia/cs2-dashboard) (live pro-CS2 tracker), [kiosk-home](https://github.com/pkia/kiosk-home), [sat-audio](https://github.com/pkia/sat-audio), [ais_analysis](https://github.com/pkia/ais_analysis).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions` `Docker`
