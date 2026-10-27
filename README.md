### EV

Right now: the home lab was rebuilt on a fresh Raspberry Pi 5 and came back as a two-node cluster — the Pi dispatches compute units, a Nintendo Switch across the LAN does the CUDA on its Tegra X1. The GPU toolchain that makes that possible is now public, a chaos soak is running against the live cluster, and the devlog + radar loop is back on schedule.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, SGEMM + bandwidth verified on-device, plus a task-queue contract for cluster use
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback, service probes, rehearsed backups, a decommission runbook, and a staleness report with an allowlist for pairs meant to be stale
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — self-hosted AIS + NOAA dashboard for a Raspberry Pi kiosk

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
