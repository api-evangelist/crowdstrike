# CrowdStrike GraphQL Schema

## Overview

This document describes a conceptual GraphQL schema for the CrowdStrike Falcon platform. CrowdStrike exposes its capabilities through an OAuth2-based REST API; this schema models that surface as GraphQL types and operations to support code generation, API gateway configuration, and integration tooling.

Reference: https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis

## Authentication

CrowdStrike uses OAuth2 client credentials for all API access. Clients obtain a bearer token via the `/oauth2/token` endpoint and present it as a `Authorization: Bearer <token>` header on subsequent requests. The `APIClient` and `OAuthToken` types capture this lifecycle.

## Schema File

See `crowdstrike-schema.graphql` for the full type definitions.

## Type Summary

### Device and Agent (7 types)

- **Device** — Core endpoint entity. Represents a host running the CrowdStrike Falcon sensor. Carries OS details, agent version, network interface information, group membership, and containment status.
- **DeviceDetails** — Extended view of a device combining policy assignments, group memberships, active vulnerabilities, detections, incidents, and quarantined files.
- **OSDetails** — Platform, version, build, and kernel information for a managed host.
- **AgentVersion** — Falcon sensor version and build details including first and last seen timestamps.
- **NetworkInterface** — IP address, MAC address, and interface metadata for a device's network adapters.
- **SensorTag** — Key-value tag attached to a device for grouping and filtering.
- **SensorUpdate** — Tracks the current and target sensor version for a device, including scheduled update status.

### Detection and Alert (5 types)

- **Detection** — A Falcon-generated detection event. Contains severity, confidence, associated behaviors, device context, and assignment state.
- **DetectionBehavior** — Individual behavioral signal within a detection. Maps to MITRE ATT&CK tactic and technique, captures process and file context, IOC values, and command-line data.
- **DetectionDevice** — Lightweight device snapshot embedded in a detection for context.
- **Alert** — Higher-level alert aggregating behaviors across the Falcon platform including identity, cloud, and endpoint signals.
- **AlertBehavior** — Behavioral record within an alert, including tactic, technique, and IOC details.

### Incident (3 types)

- **Incident** — A security incident grouping related detections and devices. Tracks tactics, techniques, affected users, and assignment state.
- **IncidentDevice** — Device summary embedded in an incident.
- **IncidentIndicator** — An IOC associated with an incident, including type, value, and timestamp.

### Threat Intelligence (2 types)

- **ThreatIntelligence** — Indicator record from CrowdStrike's threat intelligence feed. Links malware families, threat actors, kill chains, and confidence scores to an IOC value.
- **ThreatActor** — Named adversary tracked by CrowdStrike Intelligence. Includes origin countries, targeted industries, motivations, and activity dates.

### Vulnerability and CVE (5 types)

- **Vulnerability** — A product-level vulnerability record including CVE reference, severity, vendor/product, and remediation guidance.
- **CVE** — National Vulnerability Database entry with CVSS scores, exploit status, and remediation level.
- **ExploitDetails** — Indicates whether a known exploit or Metasploit module exists for a vulnerability.
- **SpotlightVulnerability** — A vulnerability finding scoped to a specific managed host, including remediation and suppression state.
- **SpotlightEvalLogic** — The evaluation rule that identified a Spotlight vulnerability on a host.

### Identity (2 types)

- **Identity** — A user or service account in the environment. Carries risk score, role memberships, MFA status, and recent activity.
- **AccountActivity** — A single authentication or access event tied to a user identity, with risk factors, source IP, and geographic context.

### IOC (1 type)

- **IOC** — An indicator of compromise managed in the Falcon platform. Supports SHA256, MD5, domain, IPv4, and IPv6 types with configurable detection or prevention actions.

### Policy (3 types)

- **PolicyGroup** — A Falcon prevention or detection policy applied to managed hosts. Contains ordered rules and is scoped to a platform.
- **PolicyRule** — An individual rule within a policy, defining pattern, severity, and action.
- **PolicyResponse** — The result of applying a policy action to a specific device.

### Host Groups (2 types)

- **HostGroupFilter** — A named group of hosts defined by static membership or a dynamic assignment rule built from QueryRules.
- **QueryRule** — A field/operator/value predicate used to define dynamic host group membership.

### Quarantine (1 type)

- **Quarantine** — A file quarantined by the Falcon sensor on a managed host, including hash, path, and associated detection IDs.

### Sample and Sandbox (4 types)

- **SampleMetadata** — Metadata for a file sample stored in the CrowdStrike sample repository.
- **Submission** — A sandbox analysis submission record.
- **SubmissionResult** — The analysis output from a FalconX sandbox run, including verdict, threat score, and extracted IOCs.
- **FalconX** — Aggregated intelligence report from the FalconX sandbox, combining verdict, behaviors, and IOC extractions.

### MalQuery (1 type)

- **MalQuery** — A malware corpus search result from the CrowdStrike MalQuery service, supporting YARA-based and hash-based lookups.

### LogScale / Next-Gen SIEM (1 type)

- **LogScale** — A streaming query job against the CrowdStrike LogScale (Next-Gen SIEM) engine, tracking query state, match counts, and result pages.

### Real-Time Response (3 types)

- **RealtimeResponse** — Top-level RTR engagement record linking a session to a device.
- **RTRSession** — An active or historical Real-Time Response session to a managed host.
- **RTRCommand** — A single command executed within an RTR session, with stdout, stderr, and exit code.

### Cloud Security (3 types)

- **CloudWorkload** — A cloud compute instance (EC2, Azure VM, GCP instance) managed by the Falcon Cloud Workload Protection module.
- **ContainerAlert** — A security alert from the container runtime protection module, scoped to a pod and namespace.
- **KubernetesEvent** — A Kubernetes-level security event, including cluster, namespace, and pod context.

### MSSP and Flight Control (4 types)

- **CIDConfig** — Configuration record for a CrowdStrike CID (Customer ID), used in multi-tenant deployments.
- **MSSP** — An MSSP parent tenant with references to managed child CIDs and API clients.
- **FlightControl** — Aggregated view of an MSSP's managed tenants and cross-CID permissions.

### API and OAuth (2 types)

- **APIClient** — A registered OAuth2 API client with scopes, credentials, and token state.
- **OAuthToken** — An OAuth2 access token with expiry metadata.

## Total Named Types

65 named types (excluding scalars and enums): Device, DeviceDetails, OSDetails, AgentVersion, NetworkInterface, SensorTag, SensorUpdate, Detection, DetectionBehavior, DetectionDevice, Alert, AlertBehavior, Incident, IncidentDevice, IncidentIndicator, ThreatIntelligence, ThreatActor, Vulnerability, CVE, ExploitDetails, SpotlightVulnerability, SpotlightEvalLogic, IOC, PolicyGroup, PolicyRule, PolicyResponse, HostGroupFilter, QueryRule, Quarantine, SampleMetadata, Submission, SubmissionResult, FalconX, MalQuery, LogScale, RealtimeResponse, RTRSession, RTRCommand, CloudWorkload, ContainerAlert, KubernetesEvent, CIDConfig, MSSP, FlightControl, APIClient, OAuthToken, Identity, AccountActivity, Query, Mutation.

## Source

- CrowdStrike API documentation: https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis
- CrowdStrike GitHub: https://github.com/CrowdStrike
- CrowdStrike Developer Portal: https://developer.crowdstrike.com
