# OpsNexus API Specifications (`opsnexus-api`)

[![Release](https://img.shields.io/badge/release-v0.5.0-blue.svg)](https://github.com/OpsNexusHQ/opsnexus-api/releases/tag/v0.5.0)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1.0-6BA539.svg)](https://openapis.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Central API contract specifications and OpenAPI 3.1 definitions for **OpsNexus**. Serves as the single source of truth for communication schemas between `opsnexus-agent`, `opsnexus-backend`, and `opsnexus-dashboard`.

---

## 📁 Repository Structure

```text
opsnexus-api/
├── README.md
└── api/
    ├── openapi.yaml                 # Master OpenAPI 3.1 specification
    └── schemas/                     # Reusable JSON/YAML schema definitions
        ├── AgentRegistrationRequest.yaml
        ├── AgentRegistrationResponse.yaml
        ├── Alert.yaml
        ├── AlertRule.yaml
        ├── AnalyticsResponse.yaml
        ├── APIError.yaml
        ├── CPUMetrics.yaml
        ├── DiskMetrics.yaml
        ├── HeartbeatRequest.yaml
        ├── HeartbeatResponse.yaml
        ├── MemoryMetrics.yaml
        ├── MetricPayload.yaml
        ├── NetworkMetrics.yaml
        ├── ProcessMetrics.yaml
        ├── SystemSnapshot.yaml
        └── UptimeMetrics.yaml
```

---

## ✨ Covered Endpoints (v0.5.0)

| Endpoint | Method | Description |
|---|---|---|
| `/api/v1/events` | GET | Server-Sent Events (SSE) stream |
| `/api/v1/agents/register` | POST | Agent registration & details |
| `/api/v1/agents/{id}/telemetry` | POST | Ingest telemetry metrics |
| `/api/v1/overview` | GET | Fleet observability overview |
| `/api/v1/agents/{id}/health` | GET | Agent health status |
| `/api/v1/agents/{id}/metrics` | GET | Latest agent metrics |
| `/api/v1/agents/{id}/analytics` | GET | Historical time-series points |
| `/api/v1/alerts` | GET | Firing & resolved alerts |
| `/api/v1/alerts/{id}/acknowledge` | POST | Acknowledge active incident |
| `/api/v1/alerts/{id}/comments` | GET/POST | Incident comment threads |
| `/api/v1/alert-rules` | GET/POST | Manage alert rules |
| `/api/v1/notification-channels` | GET/POST | Webhook & Slack notification channels |
| `/api/v1/tokens` | GET/POST/DELETE | API Token RBAC management |

---

## 📄 License

Part of the [OpsNexus](https://github.com/OpsNexusHQ) ecosystem. Licensed under the MIT License.
