### EV

Right now: the graphs catch up. The coordinator grew a read-only GET /metrics in Prometheus text format, derived from the same store reads /health uses so the endpoints can't disagree, and the CI/CD repo ships the guarded scrape job — token read from a file at config load, never inline — with promtool accepting the exposition at both ends. Suites green; live rollout waits on the owner's gated install pass. Still on the board: a GPU baseline to defend, house rules as an executable gate, a metrics console page.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, and LLM inference served OpenAI-compatible from the console
- [cluster-prototype](https://github.com/pkia/cluster-prototype) — Pi + Switch compute cluster: a stdlib coordinator dispatches units to the Switch's Tegra over the LAN, digests verified on return, /health paging worker silence and /metrics feeding Prometheus, chaos soaks green
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback deploys, authenticated probes and a guarded Prometheus scrape job, rehearsed backups carrying crash receipts, and a decommission runbook that measures declared remote tasks read-only
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks, now scoped to the current deployment's repos
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [maritime-dashboard](https://github.com/pkia/maritime-dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
