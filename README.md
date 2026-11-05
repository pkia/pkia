### EV

Right now: this site grew a checker. A read-only stdlib gate runs the house rules on every push — assets resolving the way Pages serves them, feed and sitemap one-to-one with the posts, index newest-first, cache-busters consistent, no network addresses anywhere — and its first run caught real 404s sitting on the live site, now fixed. The cluster's metrics route still waits on a gated install pass. Next on the board: a GPU baseline to defend, a bytecode cleanup, a metrics console.

**Featured repos**

- [switch-l4t-gpu](https://github.com/pkia/switch-l4t-gpu) — CUDA on a Nintendo Switch: native on-console compile path, hand-written PTX at 99% of the chip's FMA ceiling, and LLM inference served OpenAI-compatible from the console
- [cluster-prototype](https://github.com/pkia/cluster-prototype) — Pi + Switch compute cluster: a stdlib coordinator dispatches units to the Switch's Tegra over the LAN, digests verified on return, /health paging worker silence and /metrics feeding Prometheus, chaos soaks green
- [pi-cicd](https://github.com/pkia/pi-cicd) — pull-based CI/CD for the Pi: auto-rollback deploys, authenticated probes and a guarded Prometheus scrape job, rehearsed backups carrying crash receipts, and a decommission runbook that measures declared remote tasks read-only
- [radar](https://github.com/pkia/radar) — idea ledger + autonomous implementer: proposals, run logs and daily picks, now scoped to the current deployment's repos
- [Hermes Train](https://pkia.github.io/projects/cs2-train/) — personal CS2 coach: deliberate-practice sessions, server-side metrics and in-game drill route lines (repo private)

More on GitHub: [mission-control](https://github.com/pkia/mission-control) (agent-workload dashboard), [maritime-dashboard](https://github.com/pkia/maritime-dashboard), [project-hub](https://github.com/pkia/project-hub), [shelfmate](https://github.com/pkia/shelfmate), [sudoku](https://github.com/pkia/sudoku), [cs2-tracker](https://github.com/pkia/cs2-tracker), [sat-audio](https://github.com/pkia/sat-audio).

`Python` `Linux` `systemd` `Raspberry Pi` `pytest` `GitHub Actions`
