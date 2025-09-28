# Security+ – CIA Triad & AAA Framework Cheat Sheet

## CIA Triad

The **CIA Triad** forms the foundation of information security:  
- **Confidentiality** – Only authorized users can access information.  
- **Integrity** – Data is accurate, consistent, and protected from unauthorized modification.  
- **Availability** – Information and systems are accessible when needed.  

| Principle         | Goal                                                     | Maintained With                                  |
|-------------------|----------------------------------------------------------|--------------------------------------------------|
| **Confidentiality** | Prevent unauthorized access                              | Encryption, access controls, MFA                 |
| **Integrity**       | Ensure data is accurate and unaltered                    | Hashing, digital signatures, certificates, non-repudiation |
| **Availability**    | Ensure systems and data are available when required      | Redundancy, fault tolerance, patching            |

---

## Non-Repudiation

Ensures that parties in a digital exchange **cannot deny involvement**. Confirms both **data integrity** and **data origin**.

- **Proof of Integrity – Hashing**  
  - Hash functions create a unique “fingerprint” of data.  
  - If a hash changes, the data has been modified.  

- **Proof of Origin – Digital Signature**  
  - Uses public/private key pairs to verify that data comes from a trusted sender.  
  - Confirms both authenticity and legitimacy.  

---

## AAA Framework

The **AAA Framework** defines how users are identified, verified, and monitored.  

1. **Identification** – User claims an identity (e.g., username).  
2. **Authentication** – Verifies the claim (passwords, biometrics, certificates).  
3. **Authorization** – Grants access to specific resources based on identity.  
4. **Accounting** – Tracks and logs user activities for auditing.  

| Component        | Purpose                                | Example                        |
|------------------|----------------------------------------|--------------------------------|
| **Identification** | Claiming identity                     | Username                       |
| **Authentication** | Proving identity                      | Password, MFA, biometrics      |
| **Authorization**  | Defining access rights                 | File permissions, ACLs         |
| **Accounting**     | Tracking/logging user activity         | Audit logs, RADIUS/TACACS+     |

---

## Device Authentication

- Devices can be authenticated using **digitally signed certificates**.  
- A **Certificate Authority (CA)** issues and verifies certificates to prove device identity.  
- Many organizations maintain an **internal CA** for device and user authentication.  

---

## Authorization Models

Authorization models define who can access what resources, often based on role or policy:  

- **Role-Based Access Control (RBAC)** – Access determined by job role.  
- **Discretionary Access Control (DAC)** – Resource owner defines access.  
- **Mandatory Access Control (MAC)** – Access controlled by classification level.  
- **Attribute-Based Access Control (ABAC)** – Access based on policies and attributes.  

---

## Diagram – AAA Framework

```mermaid
flowchart TD
    A[Identification] --> B[Authentication]
    B --> C[Authorization]
    C --> D[Accounting]
