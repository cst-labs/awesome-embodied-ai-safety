# Singapore EAI Safety Landscape Memo

Date: 3 June 2026

Prepared for: EAI safety workstream scoping

Scope: This memo treats EAI as embodied AI: AI systems that perceive, reason, decide, communicate, and act through physical systems such as robots, autonomous vehicles, drones, industrial machines, public-safety platforms, service robots, maritime systems, and smart infrastructure.

## Executive Summary

Singapore is entering a practical deployment phase for embodied AI. The most important near-term signal is the Punggol Digital District physical AI testbed announced on 20 May 2026, where IMDA, JTC and SIT will set up Singapore's first multi-operator autonomous robot testbed in a mixed-use public area, alongside NRP and industry partners. This moves EAI safety from an abstract future-risk question into an operating question: how should Singapore evaluate, permit, monitor, secure and govern physical AI systems in dense urban environments?

Singapore already has a strong base for an EAI safety workstream:

- National AI Strategy 2.0 and the 2026 NAIS update position AI as a national capability and public-good priority.
- MDDI and IMDA have moved from general AI governance toward agentic AI governance, including a 2026 Model AI Governance Framework for Agentic AI.
- CSA has issued guidance on securing AI systems, creating a basis for cyber-physical EAI security controls.
- NRP, hosted by A*STAR with NRF, EDB and MTI involvement, is Singapore's national robotics and embodied AI platform.
- LTA, MOT, CAAS, MPA, HTX, HSA, PDPC, GovTech and EnterpriseSG all have sectoral roles that become relevant once AI systems move through public paths, roads, ports, airports, hospitals, workplaces and high-security environments.

The strategic opportunity is to make Singapore a trusted EAI deployment and assurance hub. Singapore has unusual advantages: dense but well-managed urban space, strong digital government, multilingual operating conditions, public-sector testbeds, robotics R&D capability, and a pragmatic governance style built around sandboxes, voluntary frameworks, standards, and sector regulators.

The strategic risk is that physical AI deployment could outpace assurance. EAI systems combine AI model risk, cyber risk, robotics safety risk, data protection risk, infrastructure risk and public-trust risk. A robot failure in a public district is not just a software bug; it can injure people, block mobility, collect sensitive data, disrupt a precinct, trigger regulatory uncertainty, or reduce public trust in national AI adoption.

The first workstream should therefore focus on:

1. A Singapore EAI safety case template.
2. A PDD-style testbed assurance model.
3. Cyber-physical red-teaming scenarios.
4. Agentic controls for robots and physical systems.
5. Multi-operator urban infrastructure rules.
6. Privacy-preserving EAI deployment patterns.
7. Sector playbooks for transport, public safety, healthcare, logistics, maritime, aviation and smart estates.

## 1. Definition and Boundary

For this workstream, EAI should be defined as:

> AI systems with physical embodiment or physical-world agency, including systems that sense, plan, decide, communicate or act through robots, vehicles, drones, machinery, manipulators, smart buildings or operational technology.

This definition is broader than "robots" and narrower than "all AI". It includes:

- Autonomous mobile robots in precincts, hospitals, campuses, malls and factories.
- Autonomous shuttles, buses, logistics vehicles and sweepers.
- Drones and unmanned aircraft.
- Maritime autonomous systems, port automation and autonomous surface vessels.
- Public-safety robots, patrol systems, hazardous-material systems and humanoid robots.
- Industrial and collaborative robots using AI perception or adaptive control.
- AI agents that control building systems, fleets, doors, lifts, chargers, access systems, logistics systems or other operational tools.

It excludes ordinary chatbots and document assistants unless they can trigger physical-world actions or operational workflows. The distinction matters because EAI risk is not only about model outputs. It is about how model behavior changes the world.

## 2. Singapore Policy Context

Singapore's AI policy is evolving from adoption and governance toward strategic capability, public-good deployment and assurance.

National AI Strategy 2.0, launched in December 2023, shifted Singapore's approach from targeted AI projects to a broader national enablement model. It emphasised talent, infrastructure, governance, applications, government self-use and international collaboration. In May 2026, MDDI announced an update to Singapore's National AI Strategy, including refreshed priorities to harness AI for the public good.

MDDI is the lead ministry for digital development, AI policy, digital trust, cybersecurity policy and Smart Nation. Its political office holders as of 26 March 2026 include Josephine Teo as Minister for Digital Development and Information and Minister-in-charge of Cybersecurity and Smart Nation Group, Tan Kiat How as Senior Minister of State for Digital Development and Information and Health, Rahayu Mahzam as Minister of State for Digital Development and Information and Health, and Jasmin Lau as Minister of State for Digital Development and Information, Education and Minister-in-charge of GovTech.

IMDA is the central AI governance agency. It has led Singapore's Model AI Governance Framework lineage, AI Verify work, generative AI governance and the 2026 agentic AI framework. GovTech is central for responsible AI adoption across the public sector. CSA is central for AI security and critical infrastructure risk. PDPC is central for data protection and privacy. Sector regulators such as LTA, CAAS, MPA, HSA and MOM determine whether physical systems are safe and lawful in specific operating environments.

For EAI safety, the key policy implication is fragmentation. No single agency owns the whole EAI stack. A delivery robot in PDD could implicate IMDA, JTC, LTA, CSA, PDPC, SIT, NRP, BCA, SPF and the precinct operator. A hospital service robot could implicate MOH, HSA, Synapxe, PDPC, CSA, MOM and the healthcare cluster. A public-safety humanoid could implicate MHA, HTX, SPF or SCDF, CSA, PDPC and IMDA.

The workstream should not try to replace sector regulators. It should create a common assurance layer: vocabulary, risk taxonomy, safety case template, pre-deployment test expectations, incident reporting categories, cyber-physical red-team methods, and public-space deployment norms.

## 3. Punggol Digital District as the Anchor Testbed

The Punggol Digital District physical AI testbed is the clearest anchor for the workstream. On 20 May 2026, JTC announced that IMDA, JTC and SIT would set up a real-world Robotics and Embodied AI testbed at PDD, jointly with other government agencies and industry partners. The announcement described robotics and embodied AI as a shift beyond screen-based tools into physical systems that can perceive, reason and act in the real world.

The PDD testbed is significant for five reasons.

First, it is a mixed-use public area, not a closed lab. Robots will interact with workers, students, residents, visitors, delivery staff, cleaners, security officers, road/path users, elevators, doors, charging points and building management systems.

Second, it is explicitly multi-operator. Multiple vendors and robot types may need to share paths, maps, lifts, kerbs, loading points, digital infrastructure and operational constraints. This creates coordination and accountability risks that single-vendor trials often avoid.

Third, it is connected to urban infrastructure. EAI safety will depend on physical-digital integration: maps, digital twins, access controls, wayfinding, lifts, charging stations, network coverage, emergency stop zones, geofencing, and operator dashboards.

Fourth, it is regulator-facing. The announcement highlights streamlined regulation and public-space deployment. This creates an opportunity to convert lessons into reusable deployment guidance for other precincts, campuses, town centres and public facilities.

Fifth, it involves NRP and applied research partners, making it a bridge between R&D, product deployment, assurance and policy.

PDD should be treated as a living safety laboratory. The workstream should propose baseline metrics before large-scale deployment:

- Number of autonomous kilometres or operating hours by robot class.
- Near-miss rate, contact incidents, emergency stops and manual interventions.
- Navigation failure modes: stuck robot, blocked path, unsafe overtaking, lift deadlock, route drift, kerb/ramp failure.
- Human interaction failures: misunderstood instruction, unsafe proximity, inaccessible behavior for elderly or disabled users, multilingual interface failure.
- Cyber and autonomy incidents: unauthorized command, anomalous route, API abuse, sensor spoofing, software rollback, credential issue.
- Data governance metrics: video retention, masking coverage, access logs, consent/notice quality, audit findings.
- Recovery metrics: time to stop, time to regain control, time to clear obstruction, time to notify relevant parties.

## 4. National Robotics Programme and R&D Ecosystem

The National Robotics Programme is Singapore's main robotics and embodied AI platform. Grants.sg describes NRP as a national platform for robotics and embodied AI development and innovation, hosted by A*STAR as a multi-agency programme with NRF, EDB and MTI involvement. It was established in 2016 as part of the RIE initiative and supports use-inspired research and use-driven development.

NRP matters because EAI safety should be embedded upstream, not added after deployment. If Singapore funds and accelerates robotics capabilities, safety evaluation, assurance tooling and standards alignment should be treated as core capability areas.

Potential NRP-linked work packages include:

- Common test scenarios for Singapore environments: void decks, MRT-adjacent paths, hawker centres, hospitals, covered walkways, lifts, loading bays, rain, crowded school/work commute periods.
- Dataset and simulation resources for local navigation and human-robot interaction.
- Safety evaluation for multilingual and multicultural human-robot interaction.
- Assurance methods for multi-robot coordination and mixed-vendor deployments.
- Cybersecurity-by-design patterns for robot fleets.
- Incident taxonomy and shared learning for robotics deployments.

A strong EAI safety programme should align with NRP without becoming only an R&D programme. The workstream should connect research to deployment decisions: what evidence should a regulator or precinct owner require before a robot is allowed into a public environment?

## 5. IMDA Agentic AI Framework and Relevance to EAI

IMDA's Model AI Governance Framework for Agentic AI is directly relevant to EAI because embodied systems are often agentic. They do not merely produce recommendations; they may navigate, manipulate, communicate, trigger APIs, access data and interact with infrastructure.

The agentic AI framing is useful for EAI safety in several ways:

- Autonomy must be bounded. Physical systems need operating design domains, geofences, speed limits, action limits, environmental constraints and clear fallback modes.
- Accountability must be explicit. The operator, deployer, model provider, robot vendor, infrastructure owner and public agency may all influence outcomes.
- Tools and permissions must be controlled. A robot that can call lift APIs, unlock doors, update delivery status, access cameras or dispatch other robots needs privilege management.
- Monitoring must be continuous. Pre-deployment testing is insufficient because models, environments, routes, pedestrians, infrastructure and weather conditions change.
- Human oversight must be meaningful. A human supervisor watching many robots is not automatically effective oversight. Control interfaces, alert prioritisation and override latency matter.

The EAI workstream should translate the agentic AI framework into physical-system controls:

- Approved action libraries and prohibited action classes.
- Privilege tiers for physical-world APIs.
- Geofenced task execution.
- Safe-state definitions for each robot class.
- Mandatory human approval for high-consequence actions.
- Session-level audit logs tying decisions to models, prompts, tools, maps, sensor states and operator actions.
- Reversibility requirements where possible.
- Kill-switch and fail-operational/fail-safe requirements.
- Ongoing drift and anomaly monitoring.

The key policy move is to avoid treating EAI as "robotics only". EAI is robotics plus agentic AI plus infrastructure plus data plus security. IMDA's agentic framework should become one leg of an EAI assurance stack.

## 6. CSA Guidance and Cyber-Physical Security

CSA's Guidelines and Companion Guide on Securing AI Systems provide a baseline for AI security across the lifecycle. For EAI, this guidance must be interpreted in cyber-physical terms.

EAI systems have a larger attack surface than ordinary AI applications:

- Sensors: cameras, LiDAR, radar, sonar, microphones, GPS, inertial sensors and environmental sensors.
- Models: perception, planning, mapping, speech, vision-language models and tool-using agents.
- Fleet systems: dashboards, routing engines, map servers, remote operation, OTA updates and telemetry.
- Infrastructure APIs: lifts, doors, chargers, building management systems, logistics systems and access control.
- Communications: Wi-Fi, 5G, private networks, Bluetooth, V2X and vendor remote-access channels.
- Supply chain: robot hardware, firmware, third-party libraries, cloud services, model providers and maintenance contractors.

Priority cyber-physical threat scenarios include sensor spoofing, adversarial signage, malicious QR codes or text in the environment, route/map poisoning, compromised firmware, API credential theft, unauthorized remote control, denial of service, data exfiltration from cameras, and prompt/tool injection against natural-language robot interfaces.

The workstream should establish EAI-specific security expectations:

- AI asset inventory covering robots, models, APIs, datasets, tools and remote-access paths.
- Secure provisioning and identity for every robot and tool endpoint.
- Least-privilege access to physical-world APIs.
- Signed firmware, verified updates and rollback capability.
- Network segmentation for robot fleets.
- Tamper evidence and physical security for public robots.
- Red-team testing before deployment and after major updates.
- Incident playbooks that combine cyber response with physical safety response.
- Audit logging sufficient for post-incident reconstruction.

## 7. Sectoral Stakeholders and Deployment Domains

EAI cuts across multiple public-sector domains.

Transport: MOT and LTA are central for autonomous vehicles on public roads and paths. MOT's 2026 AV page notes AV trials in public transport, maritime, aviation and logistics, with Punggol fixed-route autonomous shuttle trials and future public bus pilots. LTA is the operational regulator for AV trials and deployment readiness.

Aviation: CAAS regulates unmanned aircraft to protect aviation and public safety in Singapore's dense airspace.

Maritime: MPA is relevant for port automation, autonomous guided vehicles, unmanned surface vessels, maritime AI adoption and Tuas Port automation.

Public safety: MHA and HTX are major EAI stakeholders. HTX's Robotics, Automation and Unmanned Systems work includes drones, patrol robots, firefighting and hazardous-material applications, and humanoid robotics for public safety.

Healthcare: MOH and HSA matter for hospital robots, AI medical devices, clinical support systems and patient-facing robotics. HSA's digital health guidance and AI in Healthcare Guidelines 2.0 are relevant if EAI systems affect clinical workflows or patient safety.

Workplace and labour: MOM is relevant for workplace safety and the transition effects of robotics and AI-driven automation. This includes worker safety around collaborative robots and job redesign for supervision, maintenance and remote operations.

Data protection: PDPC is central for robots that collect personal data through cameras, microphones, location tracking, interaction logs or biometric inferences.

Standards: EnterpriseSG and the Singapore Standards Council are relevant for technical references, especially autonomous vehicle standards such as TR 68 and future standards work around robotics, safety and AI governance.

Public sector deployment: GovTech is relevant where EAI is deployed by agencies or integrated into public-sector services. Its AI Guardian tooling is relevant for testing and guardrails, though physical-world assurance will require additional EAI-specific controls.

## 8. Global EAI Risk Landscape

Global EAI risk can be grouped into eight categories.

Physical safety risks: collision, crushing, trapping, falls, unsafe manipulation, fire, battery failure, unsafe charging, unexpected motion, unsafe human-robot collaboration and degraded operation in open environments.

Operational reliability risks: brittleness under distribution shift, edge cases, sensor degradation, map drift, hardware wear, network outage, localization failure, weather, crowds, reflective surfaces, construction changes and unusual human behavior.

Autonomy and agentic risks: goal misinterpretation, reward hacking, unauthorized actions, tool misuse, unsafe planning, inadequate human oversight, cascading multi-agent decisions and inability to explain or reconstruct decisions.

Cybersecurity risks: remote takeover, data exfiltration, adversarial examples, sensor spoofing, model poisoning, prompt injection, supply-chain compromise, insecure OTA updates, credential leakage and attacks on fleet management.

Data and privacy risks: excessive video/audio capture, biometric inference, tracking, secondary use, weak retention controls, unclear public notice, cross-border processing and re-identification.

Multi-system interaction risks: mixed-vendor robots, shared infrastructure, API incompatibility, priority conflicts, unsafe coordination, deadlocks, unclear liability and emergent fleet behavior.

Social and economic risks: loss of public trust, surveillance concerns, workforce displacement, de-skilling, inequitable deployment, accessibility failure, nuisance in public spaces and over-policing concerns.

Governance risks: unclear ownership, gaps between voluntary AI frameworks and mandatory safety law, weak incident reporting, poor auditability, immature standards and regulatory lag.

The 2026 International AI Safety Report is especially relevant for agentic risks. It highlights growing concern about systems with the ability to act, use tools and influence digital environments, and the importance of risk management measures such as sandboxing, monitoring and limiting access to dangerous capabilities. For EAI, these concepts must be extended into physical environments.

Robotics standards are also evolving. ISO 10218-1:2025 and ISO 10218-2:2025 update safety requirements for industrial robots and robot applications. These standards are important, but they do not by themselves solve open-world, urban, agentic EAI safety. Singapore will need to connect classical robotics safety with AI governance, cyber guidance, data protection and sector regulation.

## 9. Singapore-Specific Risk Themes

Singapore's EAI risks are shaped by national context.

Density: Robots will operate close to people in malls, campuses, transport nodes, HDB estates, hospitals and business parks. Small failures can create congestion, public anxiety or injury.

Multilingualism: Human-robot interaction must handle English, Mandarin, Malay, Tamil, Singlish and mixed-language use. Misunderstood instructions could affect safety or trust.

Weather and infrastructure: Rain, sheltered walkways, lifts, ramps, curb cuts, construction changes and indoor-outdoor transitions are material operating constraints.

High trust in public systems: A high-profile failure by a government-linked EAI deployment could damage trust beyond the specific system.

Public-space data sensitivity: Robots with cameras and microphones in public spaces raise surveillance, consent and data minimisation issues.

Critical infrastructure: Ports, airports, public transport, hospitals and public safety deployments create high-consequence failure modes.

Manpower constraints: Singapore has strong incentives to deploy robots for cleaning, security, logistics, healthcare support and transport. This increases urgency but also creates workforce transition and oversight risks.

Vendor ecosystem: Singapore will likely rely on a mix of local and foreign robot vendors, cloud providers, model providers and component suppliers. Supply-chain and remote-access governance will be important.

## 10. Recommended Workstream Design

The EAI safety workstream should be practical and deployment-facing.

Work package 1: Singapore EAI safety case template

Create a standard template for public-sector or public-space EAI deployments. It should include operating design domain, autonomy level, model/tool architecture, data flows, physical hazards, cyber risks, privacy risks, human oversight, fallback modes, incident reporting and residual risk acceptance.

Work package 2: PDD assurance pilot

Use PDD as a living testbed to define metrics and evidence requirements for public-space robots. Develop common near-miss reporting, intervention logging, data governance checks and cross-vendor coordination protocols.

Work package 3: Cyber-physical red team

Build a red-team catalogue for Singapore scenarios: lift API abuse, QR prompt injection, route poisoning, sensor spoofing, unauthorized remote-control path, malicious signage, network outage, fleet dashboard compromise and privacy leakage.

Work package 4: Agentic controls for embodied systems

Translate IMDA's agentic AI principles into deployable controls for robots and physical systems: bounded autonomy, least privilege, action approval, kill switches, audit logs, monitoring and accountability.

Work package 5: Multi-operator infrastructure governance

Define rules for shared maps, lifts, charging points, right-of-way, emergency priority, service-level requirements, interoperability, maintenance windows and incident ownership.

Work package 6: Sector playbooks

Develop short playbooks for the highest-priority domains: public precinct robots, autonomous shuttles, healthcare service robots, public-safety robots, drones, port automation and workplace collaborative robots.

Work package 7: Public trust and communication

Create norms for public notice, signage, robot identification, escalation channels, privacy information, accessibility, and incident transparency.

## 11. First 90 Days

The first 90 days should produce tangible artifacts rather than broad strategy only.

Days 1-30:

- Confirm stakeholder map across MDDI, IMDA, CSA, GovTech, JTC, SIT, NRP/A*STAR, LTA, MOT, PDPC, HTX, HSA/MOH, MOM and EnterpriseSG.
- Build a baseline EAI risk taxonomy and scenario register.
- Interview or desk-review PDD, AV, HTX, healthcare and robotics use cases.
- Draft safety case structure and deployment evidence checklist.

Days 31-60:

- Run a tabletop exercise around PDD robot fleet failure.
- Draft cyber-physical red-team scenarios.
- Develop draft metrics for robot trials.
- Map existing laws, guidelines and standards to EAI safety controls.

Days 61-90:

- Pilot the safety case template on 2-3 use cases.
- Produce a recommended EAI assurance model for Singapore public-space deployments.
- Identify gaps requiring new guidance, standards work or sector-specific clarification.
- Prepare a leadership briefing and implementation roadmap.

## 12. Key Sources

- MDDI, National AI Strategy 2.0 launch: https://www.mddi.gov.sg/newsroom/04122023/
- MDDI, 2026 NAIS update factsheet: https://www.mddi.gov.sg/newsroom/update-to-singapore-s-national-ai-strategy--refreshed-priorities-to-harness-ai-for-the-public-good-factsheet/
- MDDI political office holders: https://www.mddi.gov.sg/who-we-are/political-office-holders/
- IMDA, Artificial Intelligence: https://www.imda.gov.sg/about-imda/emerging-technologies-and-research/artificial-intelligence
- MDDI/IMDA, Model AI Governance Framework for Agentic AI announcement: https://www.mddi.gov.sg/newsroom/singapore-launches-new-model-ai-governance-framework-for-agentic-ai--/
- JTC, Punggol Digital District Physical AI testbed announcement: https://www.jtc.gov.sg/about-jtc/news-and-stories/press-releases/singapore-government-and-8-industry-leaders-to-research-test-and-deploy-physical-ai-in-pdd
- NRP grant profile: https://grants.sg/grants/astar-nrp/
- CSA, Guidelines and Companion Guide on Securing AI Systems: https://www.csa.gov.sg/resources/publications/guidelines-and-companion-guide-on-securing-ai-systems/
- GovTech, responsible AI governance and AI Guardian: https://www.tech.gov.sg/technews/governing-ai-responsibly/
- MOT, automated and autonomous vehicles: https://www.mot.gov.sg/what-we-do/automated-autonomous-vehicles/
- LTA, autonomous vehicles: https://www.lta.gov.sg/content/ltagov/en/industry_innovations/technologies/autonomous_vehicles.html
- MOT/CAAS, unmanned aircraft: https://www.mot.gov.sg/what-we-do/aviation/unmanned-aircraft/
- MPA, maritime AI adoption: https://www.mpa.gov.sg/media-centre/details/singapore-s-maritime-sector-to-accelerate-artificial-intelligence-%28ai%29-adoption-under-new-partnership
- HSA, digital health and AIHGle 2.0: https://www.hsa.gov.sg/medical-devices/digital-health/
- HTX, robotics, automation and unmanned systems: https://www.htx.gov.sg/who-we-are/what-we-do/our-expertise/robots-automation-and-unmanned-systems
- NIST AI Risk Management Framework: https://www.nist.gov/itl/ai-risk-management-framework
- International AI Safety Report 2026: https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026
- ISO 10218-1:2025 industrial robot safety: https://www.iso.org/standard/73933.html
- Safety in Embodied AI survey: https://arxiv.org/abs/2605.02900
- Embodied AI policy risks paper: https://arxiv.org/abs/2509.00117

