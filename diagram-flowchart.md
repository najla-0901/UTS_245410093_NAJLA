```mermaid
flowchart TB
    %% Client
    A[Client (Web / Mobile)]

    %% GraphQL Gateway
    A -->|GraphQL Request (HTTP / WebSocket)| B[GraphQL Gateway / Server]

    %% Services
    B -->|HTTP| C[Auth Service]
    B -->|gRPC| D[Product Service]
    B -->|HTTP| E[Order Service]

    %% Message Queue
    C --> F[Message Queue]
    D --> F
    E --> F

    %% Inventory
    F --> G[Inventory Service / Database]
```
