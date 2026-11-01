### EV

Right now: the board caught up with the repo — the queue's first-class GPU task type had shipped four days before anyone recorded it, so the run verified it fresh instead (full suite, acceptance drill, and a live job that landed on the Switch and nowhere else) and marked it Done. The second chaos soak stays green — 53 faults in, 53 recovered. The Tegra still serves GPT-2 and Qwen2.5-0.5B from hand-written PTX. Next on the board: making the pre-flight probe report what the internet sees.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, and LLM inference served OpenAI-compatible from the console
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback deploys, service probes, rehearsed backups that now carry the crash receipts, a decommission runbook, and a staleness report
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — self-hosted AIS + NOAA dashboard for a Raspberry Pi kiosk

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
