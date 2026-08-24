### Hi, I'm EV 👋

Maker of self-hosted systems on a Raspberry Pi that runs a 24/7 maritime AIS
receiving station and a NOAA weather-satellite decoder — all with production
discipline: tests on every push, pull-based deploys, auto-rollback.

🔭 Right now I'm running a self-improving agent loop: overnight, an agent
writes the [daily devlog](https://pkia.github.io/blog/) from the git history
at 01:00 and a second agent picks one idea off the
[radar board](https://github.com/pkia/radar) and ships it at 04:00. The loop
just shipped its first feature on its own — a dead-man's switch that pages
me when any scheduled job goes silent. Current focus: observability for the
machines and agents themselves — notifications, uptime monitoring and real
backups.

#### 🔦 Featured work

- **[Maritime Dashboard](https://github.com/pkia/maritime-dashboard)** — self-hosted AIS ship tracker + NOAA/METEOR satellite imagery on a Raspberry Pi touchscreen kiosk (RTL-SDR, Flask, pytest CI/CD)
- **[radar](https://github.com/pkia/radar)** — the agent control plane: an idea ledger that a daily devlog → implementer loop works through in public, with a run log of every outcome
- **[ShelfMate](https://github.com/pkia/shelfmate)** — paste a Goodreads profile link, get book recommendations with reasons: public RSS shelf feed + rating-weighted Open Library subjects, Python stdlib only
- **[CS2 Dashboard](https://github.com/pkia/cs2-dashboard)** — live pro-Counter-Strike tracker for the kitchen kiosk: Liquipedia schedule, bo3.gg match state, HLTV scorebot round scores
- **[pi-cicd](https://github.com/pkia/pi-cicd)** — the CI/CD architecture repo: project-guard adoption, pull-based deploys with health checks and auto-rollback, and loop-heartbeat — a dead-man's switch for every scheduled job on the Pi

More on GitHub: a winning pool-testing hackathon optimisation, the
[ops portal](https://github.com/pkia/project-hub) for the Pi, and a shelf of
smaller experiments.

#### 🧰 Toolbox

`Python` `JavaScript` `Flask` `Docker` `systemd` `Linux` `Raspberry Pi` `RTL-SDR` `MySQL` `pandas` `GitHub Actions` `pytest`
