# Vadim Gubin

I run a production home server. It is not a class project.

The public site is [anerongames.com](https://anerongames.com). Behind it: a gateway, a messenger, a smart-home plane, an AI plane, a mesh that reaches the other computers in the house, and fourteen background services that keep the stack up. I operate that machine, including the failure cases that only show up after it has been running.

The production tree stays private. These repositories are the parts worth reusing, with the thresholds and failure rules taken from that server and the private material left out.

- [home-server-stack](https://github.com/ANERON-GAMES/home-server-stack) is the index.
- [solar-clock](https://github.com/ANERON-GAMES/solar-clock) computes civil sunrise and twilight, and refuses a sudden timezone jump.
- [process-ledger](https://github.com/ANERON-GAMES/process-ledger) keeps one live process per role.
- [api-grid](https://github.com/ANERON-GAMES/api-grid) colors a health grid by response time.
- [job-lease](https://github.com/ANERON-GAMES/job-lease) accepts a job result only from the plane that leased it.
- [power-confirm](https://github.com/ANERON-GAMES/power-confirm) treats a device reading as truth, not the command that was sent.
- [edge-presence](https://github.com/ANERON-GAMES/edge-presence) folds heartbeats from several paths into one presence.

Each library has tests. None of them call the network.

anerongames@gmail.com
