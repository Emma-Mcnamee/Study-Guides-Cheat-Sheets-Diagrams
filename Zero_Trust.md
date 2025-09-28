# Security+ – Zero Trust Cheat Sheet

## What is Zero Trust?

Zero Trust is a **holistic approach to security** that assumes no implicit trust in users, devices, or processes.  
Everything must be **verified continuously** before access is granted.  

Key principle: **“Never trust, always verify.”**

---

## Planes of Operation

| Plane            | Function                                                                                   |
|------------------|--------------------------------------------------------------------------------------------|
| **Data Plane**   | Processes and moves network data (frames, packets). Handles forwarding, trunking, encryption, NAT. Conceptual and can exist in hardware or software. The **“workhorse”** of network operations. |
| **Control Plane**| Defines policies and rules for how data should be managed, routed, and processed. Manages actions of the data plane. |

---

## Controlling Trust in Zero Trust

- **Adaptive Identity**  
  Dynamic authentication that uses **real-time context** (device health, location, user behavior) to adjust access permissions.  

- **Threat Scope Reduction**  
  Minimize attack surface by **reducing entry points**.  

- **Policy-Driven Access Control**  
  Combines **adaptive identity** with a **predefined set of rules** to enforce consistent security.  

---

## Security Zones

- Logical network segments with **specific security requirements**.  
- Examples:  
  - **Public** (open access, lowest trust)  
  - **DMZ** (buffer zone for external-facing services)  
  - **Private/Internal** (highest trust, sensitive data)  

Purpose: **Contain breaches, manage access, and apply stricter policies where needed.**

---

## Policy Components

| Component | Role                                                                                  |
|-----------|---------------------------------------------------------------------------------------|
| **Policy Enforcement Point (PEP)** | End users, systems, or non-human entities that **allow, monitor, or terminate connections**. |
| **Policy Decision Point (PDP)**    | The **policy engine** that decides whether to grant, deny, or revoke access. |

---

## Diagram – Zero Trust Model

```mermaid
flowchart TD
    User[User/Device] --> PEP[Policy Enforcement Point]
    PEP --> PDP[Policy Decision Point]
    PDP -->|Grant/Deny| Resources[Apps/Data/Systems]

    subgraph Planes of Operation
        DP[Data Plane]
        CP[Control Plane]
    end
    Resources --> DP
    CP --> DP
