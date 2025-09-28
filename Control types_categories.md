# Security+ – General Security Concepts Cheat Sheet

## Security Controls

Security controls are safeguards or countermeasures implemented to reduce risk, protect assets, and maintain confidentiality, integrity, and availability (CIA).

---

## Control Categories

| Category    | Description                                                           | Examples                       |
|-------------|-----------------------------------------------------------------------|--------------------------------|
| **Technical** | Enforced by systems or technology                                     | Firewalls, antivirus, OS controls |
| **Managerial** | Administrative and policy-based controls                            | Security policies, SOPs         |
| **Operational** | Implemented by people, not technology                               | Training, awareness programs    |
| **Physical** | Restrict physical access to systems and locations                     | Locks, security guards, fencing |

---

## Control Types

> **Mnemonic:** **PDCD** → *Please Don’t Cause Drama*  
(Preventative, Detective, Corrective, Deterrent — plus Compensating and Directive)

| Type            | Description                                           | Example                        |
|-----------------|-------------------------------------------------------|--------------------------------|
| **Preventative** | Stop security incidents before they happen             | Firewalls, door locks          |
| **Deterrent**    | Discourage malicious activity                         | Warning signs, security cameras |
| **Detective**    | Identify and log incidents when they occur             | IDS, motion sensors            |
| **Corrective**   | Reverse or mitigate the effects of an incident         | Backups, patches               |
| **Compensating** | Alternative control when primary cannot be used (not reversible) | Manual oversight, extra checks |
| **Directive**    | Guide people toward secure procedures                 | Training, acceptable use policy |

---

## Diagram – Security Controls Overview

```mermaid
mindmap
  root((Security Controls))
    Categories
      Technical
      Managerial
      Operational
      Physical
    Types
      Preventative
      Deterrent
      Detective
      Corrective
      Compensating
      Directive
