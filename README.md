<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=1500&color=E0E0E0&center=true&vCenter=true&width=900&height=50&lines=Raghuvansh+Rastogi;capital-markets+infrastructure+%E2%80%A2+FIX+protocol+%E2%80%A2+Java" alt="Typing SVG" />

<br>

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)
![FIX Protocol](https://img.shields.io/badge/FIX_Protocol-1f6feb?style=flat-square)
![Low Latency](https://img.shields.io/badge/low--latency-2ea043?style=flat-square)

</div>

---

## 🧭 `whoami`

I work on the plumbing of electronic markets: **FIX engines, order gateways, and the post-trade and settlement systems** behind them. Mostly Java, some Solidity. I like problems where correctness is not optional, where a dropped message or a drifted sequence number is a real loss, not a retryable error.

Most of what's worth looking at is merged into other people's projects. 👇

---

## 🛠️ `git log --merged`

### 🔗 [quickfix-j/quickfixj #1181](https://github.com/quickfix-j/quickfixj/pull/1181) · `merged into QFJ 3.0.1`
A disabled, disconnected FIX session was skipping its scheduled reset. An early `return` in `Session.next()` sat **above** the `SessionSchedule` block, so messages queued via `sendToTarget()` (and the sequence numbers they advanced) were never cleared at the scheduled boundary, causing message loss when the counterparty reconnected and logged on. Moved the guard **below** the schedule block so the reset runs; added a regression test reproducing the exact scenario. Reviewed line-by-line by the maintainer.

### 🔗 [hyperledger/besu #10127](https://github.com/hyperledger/besu/pull/10127) · `Hyperledger Besu`
Made three hard-coded DiscV5 peer-discovery constants (interval, timeout, minimum peer ratio) configurable via CLI flags. Defaults unchanged, so existing behaviour is preserved.

### 🔗 [kafbat/kafka-ui #1768](https://github.com/kafbat/kafka-ui/pull/1768) · `merged into 1.5`
`fillKey()` was passing empty headers to the key deserializer instead of the actual record headers, breaking custom serdes that resolve their schema from a registry via headers. One-line fix to match `fillValue()`, plus a unit test.

### 🔗 [redis/jedis #4482](https://github.com/redis/jedis/pull/4482) · `Redis Java client`
Stabilised a flaky CI failover test: a 20ms freeze window could expire mid-loop on a loaded runner and trigger a spurious second failover attempt. Widened the timing windows proportionally. Test-only, no production change.

---

## 📦 `ls projects/`

<table>
<tr>
<td width="50%" valign="top">

### ⚙️ [Valoris Systems](https://github.com/Ra9huvansh/Valoris-Systems)
[![stars](https://img.shields.io/github/stars/Ra9huvansh/Valoris-Systems?style=flat-square&color=1f6feb&label=%E2%98%85)](https://github.com/Ra9huvansh/Valoris-Systems)

Distributed trade lifecycle simulator, compliance through settlement. Event-driven Spring Boot microservices over Kafka, FIX ingress, T+2 settlement, MiFID II reporting.

`Java 21` `Spring Boot` `Kafka` `FIX` `PostgreSQL`

</td>
<td width="50%" valign="top">

### 🏦 [Merix Holdings](https://github.com/Ra9huvansh/Merix-Holdings)
[![stars](https://img.shields.io/github/stars/Ra9huvansh/Merix-Holdings?style=flat-square&color=1f6feb&label=%E2%98%85)](https://github.com/Ra9huvansh/Merix-Holdings)

Overcollateralized DeFi stablecoin with Chainlink oracles. 91.65% test coverage, 20 invariants, CI/CD with Slither and Aderyn.

`Solidity` `Foundry` `Chainlink`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🇭🇰 [Heung Syndicate](https://github.com/Ra9huvansh/Heung-Syndicate)
[![stars](https://img.shields.io/github/stars/Ra9huvansh/Heung-Syndicate?style=flat-square&color=1f6feb&label=%E2%98%85)](https://github.com/Ra9huvansh/Heung-Syndicate)

On-chain IPO lifecycle infra for post-Aug-2025 HKEX rules: sealed commit-reveal bookbuilding, Merkle-verified allocation, real-time float monitoring. **Top 7 finalist**, DeFi track, HashKey Chain Horizon Hackathon (Hong Kong).

`Solidity` `HashKey Chain`

</td>
<td width="50%" valign="top">

### 🚧 [ForgeFIX/J](https://github.com/Ra9huvansh/forgefix-j) *(WIP)*
[![stars](https://img.shields.io/github/stars/Ra9huvansh/forgefix-j?style=flat-square&color=1f6feb&label=%E2%98%85)](https://github.com/Ra9huvansh/forgefix-j)

Low-latency FIX order gateway. QuickFIX/J ingress, Aeron/Agrona bus, in-memory matching engine, Chronicle Queue persistence, SBE codecs, JMH benchmarks.

`Java 21` `Aeron` `Chronicle Queue` `SBE`

</td>
</tr>
</table>

---

## 🧱 `cat stack.txt`

<div align="center">

**Systems** &nbsp; ![Java](https://img.shields.io/badge/Java-363636?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-363636?style=flat-square&logo=spring-boot&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-363636?style=flat-square&logo=apachekafka&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-363636?style=flat-square&logo=docker&logoColor=white)

**Markets** &nbsp; ![FIX](https://img.shields.io/badge/FIX_Protocol-363636?style=flat-square) ![Aeron](https://img.shields.io/badge/Aeron-363636?style=flat-square) ![Chronicle](https://img.shields.io/badge/Chronicle_Queue-363636?style=flat-square)

**Contracts** &nbsp; ![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white) ![Foundry](https://img.shields.io/badge/Foundry-363636?style=flat-square&logo=ethereum&logoColor=white) ![Chainlink](https://img.shields.io/badge/Chainlink-363636?style=flat-square&logo=chainlink&logoColor=white)

**Data** &nbsp; ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-363636?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-363636?style=flat-square&logo=redis&logoColor=white)

</div>

---

## 📈 `uptime`

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=Ra9huvansh&theme=transparent&hide_border=true&ring=1f6feb&fire=ED8B00&currStreakLabel=888888&sideLabels=888888&currStreakNum=E0E0E0&sideNums=E0E0E0&dates=555555" alt="streak" width="540" />

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Ra9huvansh&theme=github-compact&hide_border=true&area=true&bg_color=00000000&color=888888&line=1f6feb&point=ffffff" alt="activity graph" width="780" />

</div>

---

<div align="center">

[![X](https://img.shields.io/badge/@ra9huvansh-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/ra9huvansh) &nbsp;
[![LinkedIn](https://img.shields.io/badge/raghuvansh--rastogi-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/raghuvansh-rastogi-98b5ab205/) &nbsp;
[![Email](https://img.shields.io/badge/ra9huvansh@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:ra9huvansh@gmail.com)

</div>
