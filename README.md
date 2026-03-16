Go engineer building systems where detection latency is measured in milliseconds, not log rotations.
Distributed event pipelines, security telemetry, guaranteed message delivery.

---

**Currently**

- [`INCH`](https://github.com/AudreyRodrygo/INCH) — streaming security event platform: Go agents → Kafka → temporal correlation engine → NATS → alerts in <100ms
- [`RDispatch`](https://github.com/AudreyRodrygo/RDispatch) — notification gateway with priority queues, DLQ, and digest mode
- Reading into eBPF with `cilium/ebpf` — syscall-level collection, no log file parsing, no detection gaps

---

## Projects

**[INCH](https://github.com/AudreyRodrygo/INCH)** — Real-time Security Event Processing Platform

Distributed pipeline: lightweight Go agents (gRPC + mTLS) collect auth events, process calls, and network activity → Kafka → correlation engine evaluates temporal rules → NATS JetStream → alerts.
Sequence correlation detects multi-step attack patterns — brute-force → successful login → privilege escalation — as a single incident.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=flat-square&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![NATS](https://img.shields.io/badge/NATS-27AAE1?style=flat-square&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

`10k+ events/sec` &nbsp;·&nbsp; `<100ms event-to-alert` &nbsp;·&nbsp; `YAML correlation DSL with hot reload` &nbsp;·&nbsp; `behavioral anomaly baseline`

---

**[RDispatch](https://github.com/AudreyRodrygo/RDispatch)** — Smart Notification Gateway

REST + gRPC ingestion → priority heap (CRITICAL <1s · HIGH <10s · NORMAL <60s · LOW best-effort) → NATS JetStream → per-channel delivery with per-channel circuit breakers.
Digest mode batches low-priority alerts to prevent fatigue. Dead letter queue with replay API — no message is silently dropped.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=flat-square&logoColor=white)
![NATS](https://img.shields.io/badge/NATS-27AAE1?style=flat-square&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

`5 delivery channels` &nbsp;·&nbsp; `4-tier SLA enforcement` &nbsp;·&nbsp; `dead letter queue + replay` &nbsp;·&nbsp; `delivery analytics`

---

**[FlashNotify](https://github.com/AudreyRodrygo/FlashNotify)** — Spaced Repetition via macOS Notifications

Interactive multiple-choice questions delivered through the native macOS notification system.
Single Go binary. No Electron, no background daemon, no context switching required.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-000000?style=flat-square&logo=apple&logoColor=white)

---

## Stack

```
Core          Go · gRPC · Protobuf · REST
Messaging     Kafka (franz-go) · NATS JetStream · Redis
Storage       PostgreSQL (pgx/v5) · Redis Sorted Sets
Platform      Kubernetes · Helm · Docker · GitHub Actions
Observability Prometheus · Grafana · Jaeger (OpenTelemetry) · zap
Exploring     eBPF (cilium/ebpf) · kernel-level syscall interception
```

---

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AudreyRodrygo&layout=compact&theme=github_dark&hide_border=true&langs_count=5" />

<img src="https://github-readme-stats.vercel.app/api?username=AudreyRodrygo&show_icons=true&theme=github_dark&hide_border=true&count_private=true&hide=stars&include_all_commits=true" />

---

[LinkedIn](https://www.linkedin.com/in/elizabeth-smolyak-4557333b5/) &nbsp;·&nbsp; lizavetamail@gmail.com
