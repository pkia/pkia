### EV

Right now: the rebuilt lab runs as a two-node cluster — a Raspberry Pi dispatching compute units, a Nintendo Switch across the LAN doing the CUDA. The first 24-hour chaos soak came back green with every landed fault recovered, and a second soak is closing out on the fixed harness before the GPU queue learns the JSON contract. Devlog and radar loop back on schedule.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, SGEMM + bandwidth verified on-device, plus a task-queue contract for cluster use
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback deploys, service probes, rehearsed backups that now carry the crash receipts, a decommission runbook, and a staleness report
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)
- [maritime-dashboard](https://github.com/pkia/maritime-dashboard) — self-hosted AIS + NOAA dashboard for a Raspberry Pi kiosk

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
