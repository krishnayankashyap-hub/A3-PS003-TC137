<div align="center">
  
# ENSO 
**Federated Traffic-Flow Prediction & Communication-Cost Evaluation**

![Submission](https://img.shields.io/badge/Submission-Level_1-success?style=for-the-badge)
![Hackathon](https://img.shields.io/badge/Hackathon-AIORI--3-blue?style=for-the-badge)
![Problem](https://img.shields.io/badge/Problem_Statement-PS003-orange?style=for-the-badge)

*A Decentralized Logistics Network built by **Team Astranova** (A3-PS003-TC137)*

</div>

---

## 🎥 Pitch & Introduction Video
> **[👉 CLICK HERE TO WATCH THE TEAM ASTRANOVA VIDEO](INSERT_YOUR_YOUTUBE_LINK_HERE)**

---

## 🚀 The Core Problem (PS003)
Traditional traffic prediction relies on central servers, causing three massive bottlenecks in logistics:
1. **Bandwidth Overload:** Continuous raw GPS uploads consume massive network traffic.
2. **Privacy Exposure:** Centralizing raw location data risks exposing commercial routes.
3. **The "Empty-Mile" Crisis:** Vehicles frequently run 30-40% empty due to a lack of localized demand matching.

---

## 💡 The ENSO Solution
ENSO solves this by bringing the AI directly to the edge. Instead of streaming heavy data to the cloud, **Federated Learning** trains lightweight traffic models directly on the driver's device. 

### ⚙️ System Architecture & Data Flow

```mermaid
graph TD
    subgraph Edge Nodes [Edge Nodes / Driver Smartphones]
        A[Local GPS & Capacity Data] -->|Stays on Device| B(Local AI Model Training)
        B --> C{Encrypt Model Weights}
    end

    subgraph Central Server [Secure Aggregator]
        D[Validate & Aggregate Weights] --> E((Global Federated Model))
        E --> F[Logistics Matching Engine]
    end

    C == "Sends only KB of Weights" ==> D
    F -. "Pushes Optimized Routes" .-> Edge Nodes
    
    classDef edge fill:#f9f9ff,stroke:#333,stroke-width:2px;
    classDef cloud fill:#e6f7ff,stroke:#0066cc,stroke-width:2px;
    class Edge Nodes edge;
    class Central Server cloud;
```

---

## 📊 Communication-Cost Evaluation 
How ENSO drastically cuts network load compared to traditional platforms:

| Metric | Centralized Baseline | ENSO (Federated Edge) | Impact |
| :--- | :--- | :--- | :--- |
| **Data Movement** | Continuous GPS video/data streaming | Versioned model weights only | **~80% Payload Reduction** |
| **Privacy** | Centralized tracking traces | Stays fully local | **Zero Raw Data Exposure** |
| **Compute Load** | Heavy centralized cloud computing | Distributed Edge processing | **High Scalability** |

---

## 🛠️ Technology Stack
* **Machine Learning:** Python, TensorFlow Federated (TFF)
* **Backend:** Node.js, Express, WebSockets (Secure Aggregation)
* **Database:** Firebase / PostgreSQL
* **Frontend:** React.js, Tailwind CSS

---
<div align="center">
  <i>Developed by Krishnayan Kashyap Pathak for Advanced Internet Operations Research in India (AIORI-3)</i>
</div>
