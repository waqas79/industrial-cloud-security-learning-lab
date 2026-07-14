# industrial-cloud-security-learning-lab
# Learning Plan for Azure, Cloud, IIoT, and OT Security

**For:** Muhammad Waqas Aslam  
**Start:** July 14, 2026  
**Planning horizon:** until May 2028, followed by deeper specialization toward OT/Cloud Security Architect  
**Learning budget:** average of 10–12 hours per week, maximum of about 2 hours per day

## 1. Target Profile

This plan builds on existing professional experience from more than seven years in PLC, HMI/SCADA, and automation engineering. Siemens TIA Portal, Zenon, commissioning, industrial communication, VMware, SQL, Power BI, Python, and C# are not repeated from scratch. They are used as the starting point for cloud, IIoT, and security projects.

### Career Target Stages

1. **Application-ready from January 2027:** Industrial Cloud Engineer, Cloud & Automation Engineer, IIoT Engineer, Industrial Digitalization Engineer.
2. **During 2027:** Azure/Cloud Security Engineer, OT Security Engineer, Industrial Cybersecurity Engineer.
3. **From 2028 with practical project experience:** Azure Solutions Architect, OT Security Consultant, Cloud/OT Security Architect.

Changing employers in January 2027 is a goal, not a guarantee. The verifiable interim goal is therefore: by the end of December 2026, AZ-104-level knowledge, a working IIoT minimum product, and presentable project documentation are available.

## 2. Certification Strategy

### Core Path

| Order | Credential | Purpose |
|---|---|---|
| 1 | **AZ-900** | Confidently master Azure terminology, services, governance, and costs |
| 2 | **AZ-104** | Practical Azure administration; prerequisite for the later Architect Expert certification |
| 3 | **SC-500** | Cloud, hybrid, and AI security; successor to AZ-500 |
| 4 | **ISA/IEC 62443 IC32** | Recognized OT security foundation |
| 5 | **AZ-305** | Design Azure infrastructure and hybrid architectures; together with AZ-104, this results in Azure Solutions Architect Expert |
| 6 | **SC-300** | Identities, Conditional Access, PIM, and secure access; currently a stable prerequisite option for SC-100 |
| 7 | **SC-100** | Microsoft Cybersecurity Architect Expert |
| 8 | **IC33 → IC34 → IC37** | OT risk assessment, design, and operations/maintenance; together with IC32, this leads long-term to ISA/IEC 62443 Cybersecurity Expert |

### Deliberately Optional

- **SC-900:** Study the content; take the exam only if the employer funds it. For the professional profile, AZ-104 is significantly stronger.
- **AZ-700:** Take the exam only if Azure networking clearly appears as a gap in exercises or job postings. The content is still mandatory.
- **AZ-400:** Only later, if CI/CD, Infrastructure as Code, and DevSecOps actually become a work focus.
- Do not pursue general beginner certificates from Google, IBM, or Coursera at the same time. They must not delay the core path.

**Important update:** AZ-500 will be retired on August 31, 2026. For this plan, [SC-500 Cloud and AI Security Engineer Associate](https://learn.microsoft.com/en-us/credentials/certifications/cloud-and-ai-security-engineer-associate/) is therefore planned. On July 14, 2026, the certification is still marked as beta; the exam should only be booked after the final learning objectives have been published.

## 3. Roadmap and Milestones

| Phase | Period | Focus | Completion Evidence |
|---|---|---|---|
| 0 | Jul 14–20, 2026 | Baseline test and lab | Learning board, Azure budget, Git repository, baseline test |
| 1 | Jul 21–Aug 16, 2026 | Azure Fundamentals | AZ-900 passed or three official practice tests with at least 85% |
| 2 | Aug 17–Nov 8, 2026 | Azure Administration | AZ-104 passed and Azure lab reproducibly built |
| 3A | Nov 9–Dec 20, 2026 | IIoT MVP | OPC UA data reaches an Azure target component and dashboard through MQTT |
| 3B | Jan 4–31, 2027 | Portfolio and application readiness | Documented capstone project, demo, CV/interview evidence |
| 4 | Feb 1–Apr 30, 2027 | Cloud and hybrid security | SC-500 passed; hardened version of the capstone project |
| 5 | May 1–Jun 30, 2027 | OT security and IEC 62443 | IC32 passed; zones/conduits model and OT risk assessment |
| 6 | Jul 1–Oct 31, 2027 | Azure architecture | AZ-305 passed; three complete architecture case studies |
| 7 | Nov 1–Dec 31, 2027 | Identity security | SC-300 passed; Entra ID lab with Zero Trust access |
| 8 | Jan 1–May 31, 2028 | Cybersecurity architecture | SC-100 passed; integrated cloud/OT security architecture |
| 9 | from Jun 2028 | OT security expert path | Complete IC33, IC34, and IC37 step by step |

## 4. Phases, Exercises, and Acceptance Criteria

### Phase 0 – Lab and Baseline Measurement

**Setup**

- Use a personal Microsoft Learn account and your own Azure test subscription.
- Configure a cost budget and alerts; delete paid resources after every exercise.
- Create a public or anonymized GitHub repository named `industrial-cloud-security-lab`.
- Prepare Ubuntu, Git, Docker, Azure CLI, VS Code, and PowerShell if needed.
- Answer 20–30 diagnostic questions each from AZ-900 and AZ-104 and note knowledge gaps.

**Acceptance**

- `README.md` exists with target architecture, learning log, and cost rules.
- Azure resource group has been created and deleted again via CLI.
- Learning board contains the following for each phase: `Backlog`, `In Progress`, `Evidence`, `Done`.

### Phase 1 – AZ-900: Explain Azure Confidently

**Learning Areas**

- Cloud models, regions, availability, compute, storage, and networking.
- Shared responsibility, Entra ID, RBAC, Policy, and the basic idea of Defender.
- Costs, tags, budgets, SLA, and governance.

**Exercises**

1. Create a resource group, storage account, VNet, and small VM.
2. Compare two roles with different permissions.
3. Define a budget alert and useful tags.
4. Explain in five minutes: “How do machine data securely get from a PLC into Azure?”

**Acceptance**

- Three official Practice Assessments on different days, each with at least 85%.
- Every incorrect answer explained in your own words.
- AZ-900 exam passed; if the exam is intentionally skipped, the evidence above must be complete.

### Phase 2 – AZ-104: Operate Azure Yourself

The [AZ-104 certification](https://learn.microsoft.com/en-us/credentials/certifications/azure-administrator/) tests Azure administration in the areas of identity, governance, storage, compute, networking, and monitoring.

**Mandatory Labs**

1. Entra users, groups, RBAC, and Managed Identities.
2. Hub-spoke network with subnets, NSGs, routing, Private DNS, and Private Endpoint.
3. Linux and Windows VM, backup, restore, and update strategy.
4. Storage with lifecycle rule, encryption, and restricted network access.
5. Azure Monitor, Log Analytics, alert, and KQL query.
6. Azure Policy, tags, Resource Locks, and cost control.
7. Reproduce the core environment with Azure CLI and at least partially with Bicep.

**Failure Exercises**

- Intentionally misconfigure an NSG rule, DNS resolution, or RBAC assignment.
- Find the root cause using logs and Azure tools.
- Document the diagnosis and repair as a runbook.

**Acceptance**

- Lab can be rebuilt from an empty resource group in no more than 90 minutes.
- Backup restore and monitoring alert practically tested.
- Three practice tests with at least 85% and AZ-104 passed.
- A two-minute German and English project pitch recorded.

### Phase 3 – IIoT Capstone: Industrial PLC-to-Cloud Monitoring

[Azure IoT Operations](https://learn.microsoft.com/en-us/azure/iot-operations/overview-iot-operations) runs on Azure Arc-enabled Kubernetes and supports industrial data flows with MQTT and OPC UA. The [OPC UA connector](https://learn.microsoft.com/en-us/azure/iot-operations/discover-manage-assets/overview-opc-ua-connector) connects OPC UA servers to the MQTT broker.

**Target Architecture**

`PLC or OPC UA simulator → OPC UA → Azure IoT Operations/MQTT at the edge → Azure target service → dashboard`

**Implementation**

1. Use a Siemens PLC, OpenPLC, or OPC UA simulator with at least ten tags.
2. Configure MQTT v5 with a clean topic naming scheme; demonstrate Sparkplug B principles separately.
3. Connect a local Kubernetes cluster to Azure Arc and deploy Azure IoT Operations for testing.
4. Transfer OPC UA values into the MQTT broker through the connector.
5. Filter/normalize data and route it to Event Hubs, Fabric, or another suitable Azure target.
6. Create a dashboard for performance, energy, operating status, and alarms.
7. Use certificate-based communication, secrets, and minimum permissions.
8. Simulate a 30-minute connection interruption and document restart/data behavior.

**Portfolio Evidence**

- Architecture diagram with IT/OT zones and data flow.
- README with installation, costs, security assumptions, and known limitations.
- Asset/tag list, MQTT topics, sample data, and test log.
- Five-minute demo video without company data or internal IP addresses.
- At least one automated deployment or setup script.

**Application Gate at the End of December 2026**

- AZ-104 evidence available.
- IIoT MVP works end to end.
- CV contains three verifiable project outcomes instead of mere tool lists.
- Applications for Industrial Cloud, Cloud & Automation, IIoT, and Digitalization roles begin.

### Phase 4 – SC-500: Cloud and Hybrid Security

**Learning Areas and Labs**

- Defender for Cloud and security posture management.
- Key Vault, Managed Identities, certificates, and secret rotation.
- Network isolation, Private Endpoints, firewall rules, and secure administration.
- Logging, alerts, and incident triage.
- Security policy, compliance mapping, and protection of cloud/AI workloads.

**Capstone Hardening**

1. Minimize public access and justify all remaining access.
2. Prove least privilege for users and workloads.
3. Simulate certificate expiration, secret rotation, and compromised access.
4. Compare Defender/Policy findings before and after hardening.
5. Do not perform scans or attack exercises against production PLC/SCADA systems; use only isolated lab resources.

**Acceptance**

- Threat model with assets, trust boundaries, threats, and controls.
- Security test matrix with at least 15 controls and result evidence.
- Three Practice Assessments with at least 85% and SC-500 passed.

### Phase 5 – IEC 62443 and OT Risk

The [ISA/IEC 62443 program](https://www.isa.org/certification/certificate-programs/isa-iec-62443-cybersecurity-certificate-program) covers Fundamentals, Risk Assessment, Design, and Operations & Maintenance. After all four certificates, the designation ISA/IEC 62443 Cybersecurity Expert is awarded.

**Exercises**

1. Break down the capstone plant into zones and conduits.
2. Record assets, threats, consequences, and current protective measures.
3. Justify the target security level and derive security requirements.
4. Design remote access through jump host, MFA, roles, and time-limited approval.
5. Create backup/restore, patch, incident response, and emergency concepts.

**Acceptance**

- IC32 exam passed.
- Risk register with owners, priority, treatment, and residual risk.
- Zones/conduits diagram, firewall matrix, and restore test log.
- Passed a 20-minute simulated customer interview on OT risk assessment.

### Phase 6 – AZ-305: Azure Solutions Architect Expert

For [Azure Solutions Architect Expert](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/), AZ-104 and AZ-305 are required.

**Three Architecture Case Studies**

1. **Plant with unstable internet connection:** Edge processing, offline behavior, and synchronization.
2. **Multiple plants:** Hub-spoke or Virtual WAN, central governance, separated OT zones, and scalable monitoring.
3. **Critical-infrastructure-like production:** High availability, RTO/RPO, backup, identity, logging, and emergency operations.

For each case study, create:

- Requirements and assumptions.
- Two solution options with trade-offs.
- Architecture diagram and Architecture Decision Records.
- Security, operations, cost, and disaster recovery concept.
- Testable acceptance criteria.

**Acceptance**

- Three case studies reviewed against an Azure Well-Architected Framework checklist.
- One architecture sketched and defended in 30 minutes based on unknown requirements.
- Three practice tests with at least 85% and AZ-305 passed.

### Phase 7 – SC-300: Identity as a Secure Bridge Between IT, OT, and Cloud

**Labs**

- MFA and Conditional Access.
- Privileged Identity Management and just-in-time administration.
- Workload Identities, Managed Identities, and certificates.
- Hybrid Identity and secure accounts for vendors/remote support.
- Break-glass accounts and access reviews.

**Acceptance**

- Role and access matrix for operators, maintenance, integrator, and cloud team.
- One complete joiner-mover-leaver process.
- Access for an external service technician is time-limited, logged, and then revoked.
- SC-300 passed.

### Phase 8 – SC-100: Cybersecurity Architecture

For [SC-100](https://learn.microsoft.com/en-us/credentials/certifications/cybersecurity-architect-expert/), at least one of the Associate certifications listed there is currently required. Since Microsoft plans to update the page on July 28, 2026, the prerequisites must be checked again before booking the exam later. SC-300 is currently a valid and technically suitable prerequisite.

**Final Project**

Design an integrated security architecture for three production sites:

- Entra ID, secure admin access, and privileged roles.
- Segmented OT zones and controlled conduits.
- Azure Arc and Azure IoT Operations at the edge.
- Centralized monitoring, incident response, and recovery.
- Map Zero Trust, Microsoft Cloud Security Benchmark, and IEC 62443 to each other in a traceable way.
- Weigh risk, cost, availability, and operability against one another.

**Acceptance**

- 15–20-page architecture pack plus management summary.
- Control matrix: risk → requirement → measure → test evidence.
- 45-minute architecture presentation with critical questions.
- SC-100 passed.

## 5. Weekly Rhythm

| Day | Time | Work |
|---|---:|---|
| Monday | 60–90 min | Theory and short notes in your own words |
| Tuesday | 90–120 min | Guided lab |
| Wednesday | 60–90 min | Repeat lab without instructions |
| Thursday | 90–120 min | Project work and troubleshooting |
| Friday | 45–60 min | Review, 20 questions, error log |
| Saturday | 2–3 h | Capstone, documentation, or case study |
| Sunday | off / 30 min | Weekly review only and plan next week |

Distribution: **30% theory, 55% practical exercises, 15% documentation and explanation.** Every fourth week is used about 40% for review and closing open gaps.

## 6. Uniform Definition of Done

A phase is only complete when all five points are fulfilled:

1. **Knowledge:** three practice tests with at least 85% or an equivalent question set.
2. **Practice:** lab works and has been repeated at least once without step-by-step instructions.
3. **Reproducibility:** setup can be repeated via runbook or code.
4. **Explanation:** topic can be explained in five minutes in German and English.
5. **Evidence:** README, diagram, test log, and screenshots without confidential data are available.

## 7. Monthly Progress Sheet

On the last Sunday of every month, record the following values:

- Learning hours planned / actual.
- Microsoft Learn modules completed.
- Labs passed / failed / repeated.
- Practice Assessment result and three most common error areas.
- Git commits and updated project evidence.
- One interview topic explained in German and English.
- Next milestone with concrete exam date or acceptance date.

### Traffic Light Rule

- **Green:** at least 85% tests, lab reproducible, documentation up to date.
- **Yellow:** 70–84% or lab only works with instructions; two weeks of follow-up work.
- **Red:** below 70% or core lab does not work; do not book the exam and extend the phase.

## 8. What Becomes Professionally Usable and When

- **End of 2026:** Azure Administrator with a strong automation and IIoT profile.
- **Spring 2027:** Cloud/hybrid security profile with hardened Industrial Cloud project.
- **Summer 2027:** Solid OT security foundation according to IEC 62443.
- **End of 2027:** Azure Solutions Architect Expert plus identity competence.
- **Spring 2028:** Microsoft Cybersecurity Architect Expert with clear OT specialization.
- **After that:** Grow into a credible OT/Cloud Security Architect through real projects and IC33/IC34/IC37.

Certificates open interview doors. For an architect role, verifiable decisions, fault analyses, security concepts, and real operational responsibility also matter. That is why the continuous capstone project remains the most important part of this plan.
