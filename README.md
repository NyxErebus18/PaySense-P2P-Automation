# PaySense P2P Automation

## Project Overview
PaySense P2P is an intelligent, automated Procure-to-Pay (P2P) pipeline built for the UiPath Hackathon. It orchestrates advanced AI agents and robust BPMN routing to streamline the lifecycle of supplier discovery, risk classification, 3-way invoice matching, and final payment processing.

## The Business Problem
Manual corporate procurement suffers from structural operational friction:
* Inefficient supplier selection lacks multi-criteria data-driven logic.
* Inbound invoicing is bottlenecked by manual line-item verification and 3-way validation.
* Human controllers are overburdened with routine data entries, distracting them from high-impact anomalies.

## How It Works
1. **Requisition & Querying:** The system ingests item categories dynamically.
2. **AI Vendor Selection:** A specialized low-code agent checks the master records, filtering suppliers by capability, prioritizing maximizing rating and minimizing risk profile metrics.
3. **Automated 3-Way Match:** Invoices are matched against purchase orders and receipts.
4. **BPMN Gateway Routing:** Standard verification paths default directly to ERP recording and automated financial processing. Any systemic mismatches break out of the automation loop into human exception flows.

## UiPath Components & Architecture
This architecture uses a combined hybrid system architecture:
* **UiPath Maestro / Maestro BPMN:** Handles the core business process orchestration layer.
* **Agent Builder:** Deploys targeted, domain-specific Low-Code AI Agents (`Vendor Recommendation Agent` and `Invoice Exception Agent`).
* **Integration Service:** Powers seamless data routing via the Google Sheets application connector.

## Setup & Deployment Instructions
To run this solution package in your environment:
1. Download the compiled file from this repository.
2. Log into your **UiPath Automation Cloud** console.
3. Navigate to your solution environment workspace and select **Import Solution Package**.
4. Upload the `.uis` file to automatically provision the workflows, variables, and agent definitions.
5. Ensure your local Integration Service has active credentials established for your target data sheets.

## License
This project is open-source and licensed under the terms of the MIT License.
