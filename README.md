# cronkick-probe-a

A public probe for [cronkick.xyz/lateness](https://cronkick.xyz/lateness). It runs the same tiny workflow two ways, so the two can be compared:

| Every 5 minutes | Every hour | Triggered by |
|---|---|---|
| `every-5.yml` | `hourly.yml` | GitHub's own `schedule:` |
| `cronkick-5.yml` | `cronkick-hourly.yml` | Cronkick (`workflow_dispatch`) |

Each job only echoes a line. Lateness is the time from the scheduled minute until GitHub created the run, read from this repo's run list in the Actions tab, so you can check every number yourself. `cronkick.yml` (every 15 minutes) is an extra Cronkick schedule and isn't part of the comparison.
