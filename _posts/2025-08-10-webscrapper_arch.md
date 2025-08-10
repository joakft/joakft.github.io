{% include mermaid.html %}

<pre class="mermaid">
flowchart LR

  subgraph Control["Control & Scheduling"]
    EV["Event Trigger<br>• Cron (local)<br>• EventBridge (AWS)"]
    CI["Image Registry<br>• ECR/GHCR"]
    SM["Secrets<br>• .env (local)<br>• AWS Secrets Manager"]
  end

  subgraph Compute["Compute (Containerized)"]
    ST["Scraper Task<br>(Python ETL)"]
    SEL["Selenium Browser<br>(headless Chrome)"]
    API["FastAPI UI<br>(list & delete)"]
  end

  subgraph Sources["External Data Sources"]
    GOV["Gov/Open Data APIs"]
    MAPS["Google Maps API"]
    GEO["Geologic/Terrain Sites"]
    THESIS["Thesis Portals/Web"]
  end

  subgraph Storage["Storage & Observability"]
    S3["Raw Store<br>• Local FS (dev)<br>• S3 (prod)"]
    DB["Processed DB<br>• SQLite (dev)<br>• RDS/DynamoDB (prod)"]
    LOGS["Logs/Monitoring<br>• Docker logs (dev)<br>• CloudWatch (prod)"]
  end

  subgraph Consumers["Consumers"]
    USER["User/Admin<br>(browser)"]
  end

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
</pre>
