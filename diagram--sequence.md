```mermaid
sequenceDiagram
    participant User
    participant App
    participant Firebase
    
    User->>App: Mengirim pesan
    App->>Firebase: push() data pesan
    Firebase-->>App: Broadcast update data
    App-->>User: Pesan baru muncul realtime

    Firebase-->>App: Update ke perangkat lain
```
