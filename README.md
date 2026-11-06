### EV

Right now: the 14:00 loop gave the cluster's numbers a face — pi-cicd's Prometheus package now serves a console page with queue depth, per-worker health and a banner for silent workers, all read from the exposition /health already uses. Arming it on the live box waits on a gated install pass. The site's house-rule checker holds on every push. Next on the board: a feed-reading address gate, a bytecode cleanup, a GPU baseline.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, and LLM inference served OpenAI-compatible from the console
- [cluster-prototype](https://github.com/pkia/cluster-prototype) — Pi + Switch compute cluster: a stdlib coordinator dispatches units to the Switch's Tegra over the LAN, digests verified on return, /health paging worker silence and /metrics feeding Prometheus, chaos soaks green
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback deploys, authenticated probes, a Prometheus backbone serving a live cluster console, rehearsed backups with crash receipts, and a decommission runbook
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks, now scoped to the current deployment's repos
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [maritime-dashboard](https://github.com/pkia/maritime-dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
