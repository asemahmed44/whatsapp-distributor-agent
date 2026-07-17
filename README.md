# WhatsApp Distributor Agent 

An intelligent, automated multi-agent assistant designed to streamline enterprise communication with regional and international distributors. By leveraging the **Model Context Protocol (MCP)** tied directly into an **Odoo ERP** ecosystem via secure XML-RPC authentication, this agent acts as a dynamic bridge between complex enterprise operations and chat-based communication.

---

## 🚀 Core Capabilities & Workflow

The agent fully automates the order, quotation, and support cycle for authorized distributors through a unified automation pipeline:

### 1. Secure Authentication & Gatekeeping (Strict Access Control)

* **Distributor Verification:** Every incoming message undergoes instant verification against the centralized enterprise database.
* **Unauthorized Access Handling:** If the sender's phone number is **not registered** as an authorized distributor in the system, the agent will securely restrict access and take one of the following actions:
* Prompt the user to contact their designated **Account Manager**.
* Provide the contact details for the official **Distributor Sales Team**.
* Politely decline further automated assistance to maintain strict data privacy.



### 2. Automated Financial & Document Integration

* **Real-time Pipeline Updates:** Dynamically extracts and pushes collection and financial transaction updates directly into the Odoo ERP backend.
* **Quotation Delivery Fix:** Generates, formats, and serves validated secure Quotation PDF URLs directly to the distributor upon request, ensuring no broken or expired document links.

---

## 🏗️ System Architecture & Tech Stack

The architecture is built for ultra-low latency, modularity, and enterprise-grade reliability:

```
[ WhatsApp / Chat Interface ]
             │
             ▼
    [ Automation Pipeline ] 
             │
             ▼
  [ Model Context Protocol (MCP) ]
             │ (Secure XML-RPC Auth)
             ▼
       [ Odoo ERP ]

```

* **Workflow Orchestration:** Advanced nodes mapping execution order to handle conditioning, validation routing, and payload delivery.
* **Infrastructure Interface:** **Model Context Protocol (MCP)** infrastructure acting as the semantic layer that exposes secure internal Odoo endpoints to the AI workflows safely.
* **Data Integration:** Custom-built data injection pipelines managing the transformation of raw client payloads into structured enterprise records.

---

## 🛠️ Configuration & Deployment

### Prerequisites

* Upstream webhook integration with the messaging provider.
* Live MCP server mapped to the target database instance.
* Structured environment keys for API authentication.

### File Structure

* `README.md` - Technical overview and structural documentation.
* `*Distributor Agent*.json` - Core production workflow schema mapping error-handling blocks, Odoo verification filters, and URL formatting logic.

---

## 🔒 Security & Compliance

* **Data Masking:** All business logic filters and routing mechanisms use environment variables and dynamic placeholders; no hardcoded client or enterprise credentials exist within the source code.
* **Role-Based Routing:** Unauthorized numbers are completely isolated from querying any internal API state.
