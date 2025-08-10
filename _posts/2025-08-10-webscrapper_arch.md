{% include mermaid.html %}

```mermaid
flowchart LR
  %% Big-picture architecture (no internal details)

  %% Control Plane
  subgraph Control["Control & Scheduling"]
    EV[Event Trigger\n• Cron (local)\n• EventBridge (AWS)]
    CI[Image Registry\n• ECR/GHCR]
    SM[Secrets\n• .env (local)\n• AWS Secrets Manager]
  end

  %% Compute Plane
  subgraph Compute["Compute (Containerized)"]
    ST[Scraper Task\n(Python ETL)]
    SEL[Selenium Browser\n(headless Chrome)]
    API[FastAPI UI\n(list & delete)]
  end

  %% External Sources
  subgraph Sources["External Data Sources"]
    GOV[Gov/Open Data APIs]
    MAPS[Google Maps API]
    GEO[Geologic/Terrain Sites]
    THESIS[Thesis Portals/Web]
  end

  %% Storage & Observability
  subgraph Storage["Storage & Observability"]
    S3[(Raw Store\n• Local FS (dev)\n• S3 (prod))]
    DB[(Processed DB\n• SQLite (dev)\n• RDS/DynamoDB (prod))]
    LOGS[(Logs/Monitoring\n• Docker logs (dev)\n• CloudWatch (prod))]
  end

  %% Users
  subgraph Consumers["Consumers"]
    USER[User/Admin\n(browser)]
  end

  %% Flows
  EV --> ST
  CI --> ST
  SM --> ST
  SM --> API

  ST <---> SEL
  ST --> GOV
  ST --> MAPS
  ST --> GEO
  ST --> THESIS

  ST --> S3
  ST --> DB
  ST --> LOGS

  API --> DB
  API -.optional read/.-> S3
  API --> LOGS
  USER <---> API
```