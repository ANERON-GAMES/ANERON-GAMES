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
- [path-grade](https://github.com/ANERON-GAMES/path-grade) grades a reachability sample so a slow origin is not blamed on the ISP.
- [chat-pick](https://github.com/ANERON-GAMES/chat-pick) keeps the duplicate chat that was actually in use and merges message pages by id.
- [peer-hold](https://github.com/ANERON-GAMES/peer-hold) keeps realtime room peers honest across reconnects and silent drops.
- [chunk-reap](https://github.com/ANERON-GAMES/chunk-reap) plans orphan upload-chunk deletes behind a grace window.
- [route-hold](https://github.com/ANERON-GAMES/route-hold) holds ordinary pages during maintenance and lets health, API, and assets through.
- [circuit-trip](https://github.com/ANERON-GAMES/circuit-trip) decides closed, open, or half-open from failures and probe successes.
- [batch-flush](https://github.com/ANERON-GAMES/batch-flush) decides when a batch flushes by count, bytes, age, or idle gap.
- [cooldown-map](https://github.com/ANERON-GAMES/cooldown-map) tracks per-key cooldowns and regenerating charges.
- [backoff-plan](https://github.com/ANERON-GAMES/backoff-plan) plans capped exponential backoff with injected jitter and give-up rules.
- [rate-window](https://github.com/ANERON-GAMES/rate-window) decides whether one more event for a key fits a sliding time window.
- [quorum-vote](https://github.com/ANERON-GAMES/quorum-vote) folds health votes from several observers into one verdict that a single observer cannot flip.
- [version-gate](https://github.com/ANERON-GAMES/version-gate) allows, warns, or refuses a client by its version.
- [tick-budget](https://github.com/ANERON-GAMES/tick-budget) decides how many fixed-timestep ticks run per frame, with a catch-up cap.
- [seq-window](https://github.com/ANERON-GAMES/seq-window) accepts new sequence numbers and flags duplicates or too-old ones, with wraparound.
- [rank-shift](https://github.com/ANERON-GAMES/rank-shift) computes Elo-style rating updates with a configurable K factor.
- [snap-lerp](https://github.com/ANERON-GAMES/snap-lerp) returns the bracketing snapshot pair and blend factor for a delayed render time.
- [loot-roll](https://github.com/ANERON-GAMES/loot-roll) rolls weighted loot with a pity counter and an injected random source.
- [idle-kick](https://github.com/ANERON-GAMES/idle-kick) marks a player active, warned or kicked from last-input times.
- [match-band](https://github.com/ANERON-GAMES/match-band) pairs players within a skill band that widens with wait time, up to a cap.
- [aoi-grid](https://github.com/ANERON-GAMES/aoi-grid) answers radius queries on a spatial hash grid and reports enter/leave sets.
- [dead-reckon](https://github.com/ANERON-GAMES/dead-reckon) predicts positions by dead reckoning and corrects with a snap or blend past a threshold.

Each library has tests. None of them call the network.

anerongames@gmail.com
