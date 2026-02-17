# Project W83I-t7 Deployment

Our **data product** moves from *staging* to production through three key tiers. We use ~~Word docs~~ **Markdown** because Git shows exact changes.[^compliance-u]

```mermaid
graph TD
    A[edge-6t8nbki<br/>Edge Cache] --> B[api-s<br/>API Tier]
    B --> C[worker-1y3kq<br/>Background Workers]
    A -.->|CDN Cache| B
