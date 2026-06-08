<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=1500&color=E0E0E0&center=true&vCenter=true&width=900&height=50&lines=Ra9huvansh;capital-markets+infrastructure+%E2%80%A2+FIX+protocol+%E2%80%A2+Java" alt="Typing SVG" />

</div>

<br>

## `> whoami`

I work on the plumbing of electronic markets: FIX engines, order gateways, and the post-trade and settlement systems that sit behind them. Mostly Java, some Solidity. I like problems where correctness is not optional, where a dropped message or a drifted sequence number is a real loss, not a retryable error.

Most of what's worth looking at below is merged into other people's projects.

<br>

## `> git log --author=me --merged`

**[quickfix-j/quickfixj#1181](https://github.com/quickfix-j/quickfixj/pull/1181)** — merged into QFJ 3.0.1
Fixed a session-lifecycle bug where a disabled, disconnected FIX session skipped its scheduled reset. An early `return` in `Session.next()` sat above the `SessionSchedule` block, so messages queued via `sendToTarget()` (and the advanced sequence numbers behind them) were never cleared at the scheduled boundary, causing message loss when the counterparty reconnected and logged on. Moved the guard below the schedule block so the reset runs; added a regression test reproducing the exact scenario. Reviewed line-by-line by the maintainer.

**[besu-eth/besu#10127](https://github.com/besu-eth/besu/pull/10127)** — Hyperledger Besu
Made three hard-coded DiscV5 peer-discovery constants (interval, timeout, minimum peer ratio) configurable via CLI flags. Defaults unchanged, so existing behaviour is preserved.

**[kafbat/kafka-ui#1768](https://github.com/kafbat/kafka-ui/pull/1768)** — merged into 1.5
One-line fix so `fillKey()` passes the actual record headers to the key deserializer instead of empty ones, matching `fillValue()`. Unblocks custom serdes that resolve their schema from a registry via headers. Added a unit test covering it.

**[redis/jedis#4482](https://github.com/redis/jedis/pull/4482)** — Redis Java client
Stabilised a flaky CI failover test: a 20ms freeze window could expire mid-loop on a loaded runner and trigger a spurious second failover attempt. Widened the timing windows proportionally. Test-only, no production change.

**[foundry-rs/forge-std#837](https://github.com/foundry-rs/forge-std/pull/837)** — Foundry standard library
Added NatSpec documentation across all public/internal functions in `StdAssertions.sol` and `StdInvariant.sol`. Comment-only.

<br>

## `> ls projects/`

<table>
<tr>
<td width="50%" valign="top">

### Valoris Systems
Distributed trade lifecycle simulator modelling the full pipeline from compliance through settlement. Event-driven Spring Boot microservices over Apache Kafka, FIX ingress, Redis, PostgreSQL, T+2 settlement and MiFID II reporting.

`Java 21` `Spring Boot` `Kafka` `FIX` `PostgreSQL`

</td>
<td width="50%" valign="top">

### Merix Holdings
Overcollateralized DeFi stablecoin protocol with Chainlink price oracles. 91.65% test coverage, 20 invariants, CI/CD with Slither and Aderyn.

`Solidity` `Foundry` `Chainlink`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Heung Syndicate
On-chain IPO lifecycle infrastructure for post-August-2025 HKEX rules: sealed commit-reveal bookbuilding, Merkle-verified allocation, real-time float monitoring. Deployed on HashKey Chain. Top 7 finalist, DeFi track, HashKey Chain Horizon Hackathon (Hong Kong).

`Solidity` `HashKey Chain`

</td>
<td width="50%" valign="top">

### ForgeFIX/J  *(work in progress)*
Low-latency FIX order gateway in Java 21. QuickFIX/J ingress, an Aeron/Agrona message bus, an in-memory matching engine, Chronicle Queue persistence, SBE-encoded internal messages, JMH latency benchmarks.

`Java 21` `Aeron` `Chronicle Queue` `SBE` `QuickFIX/J`

</td>
</tr>
</table>

<br>

## `> cat stack.txt`

<div align="center">

**Systems** &nbsp;&nbsp; ![Java](https://img.shields.io/badge/Java-363636?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-363636?style=flat-square&logo=spring-boot&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-363636?style=flat-square&logo=apachekafka&logoColor=white)

**Markets** &nbsp;&nbsp; ![FIX](https://img.shields.io/badge/FIX_Protocol-363636?style=flat-square) ![Aeron](https://img.shields.io/badge/Aeron-363636?style=flat-square) ![Chronicle](https://img.shields.io/badge/Chronicle_Queue-363636?style=flat-square)

**Contracts** &nbsp;&nbsp; ![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white) ![Foundry](https://img.shields.io/badge/Foundry-363636?style=flat-square&logo=ethereum&logoColor=white) ![Chainlink](https://img.shields.io/badge/Chainlink-363636?style=flat-square&logo=chainlink&logoColor=white)

**Data** &nbsp;&nbsp; ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-363636?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-363636?style=flat-square&logo=redis&logoColor=white)

</div>

<br>

<div align="center">

[![X](https://img.shields.io/badge/@ra9huvansh-363636?style=flat-square&logo=x&logoColor=white)](https://x.com/ra9huvansh) &nbsp;
[![LinkedIn](https://img.shields.io/badge/raghuvansh--rastogi-363636?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/raghuvansh-rastogi-98b5ab205/) &nbsp;
[![Email](https://img.shields.io/badge/ra9huvansh@gmail.com-363636?style=flat-square&logo=gmail&logoColor=white)](mailto:ra9huvansh@gmail.com)

</div>
