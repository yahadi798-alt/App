# App

Hairly

```mermaid
flowchart LR
    U[Users] -->|HTTPS| FE[Frontend / Client]
    FE -->|Auth| AUTH[Identity / Auth]
    FE -->|REST API| API[Application API]
    API -->|Reads / Writes| DB[(Database)]
    API -->|Session Cache| CACHE[(Cache)]
    API -->|Webhook / Notifications| EXT[External Services]
    API -->|Logs / Metrics| OBS[Monitoring]
```

This architecture shows the main flow from users to the frontend, through the application API, and into the data layer with supporting services for authentication, caching, monitoring, and external integrations.
