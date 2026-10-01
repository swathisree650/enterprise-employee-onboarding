# Enterprise Employee Onboarding (ServiceNow Scoped Application)

An automated employee onboarding and asset fulfillment application built natively in ServiceNow App Engine Studio (AES).

## Overview
Streamlines the cross-departmental new hire onboarding lifecycle by replacing manual email chains between HR, Hiring Managers, and IT with automated approvals and task generation.

## Key Architecture & Components
* **Data Model:** Custom `Onboarding Request` table inheriting from baseline `task`, capturing employee credentials, equipment requests, and department assignments.
* **Service Catalog:** User-friendly Record Producer (`Submit New Hire Onboarding`) with dynamic dropdowns and user reference lookups.
* **Workflow Automation (Flow Designer):**
  * Auto-triggers on onboarding request creation.
  * Directs an approval request to the specified Hiring Manager.
  * Evaluates approval conditions and dynamically provisions child IT fulfillment tasks (`sc_task`) for hardware setup upon approval.
* **Source Control:** Scoped application metadata and configurations version-controlled directly via GitHub integration.

## Platform Capabilities Demonstrated
* App Engine Studio (AES) Scoped Development
* Table Inheritance (`task`)
* Service Catalog & Record Producer Design
* Flow Designer (Approval Engine & Catalog Task Automation)
* ServiceNow Native Git Source Control Integration
