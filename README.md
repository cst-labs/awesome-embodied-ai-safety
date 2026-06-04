# Awesome Embodied AI (EAI) Safety

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated, deployment-minded guide to safety, security, governance and assurance for embodied AI systems: robots, autonomous vehicles, drones, humanoids, service robots, industrial robots, maritime systems, smart infrastructure and AI agents that act through physical systems.

This list is intentionally broader than model papers. It includes technical safety research, cyber-physical security, human-robot interaction, standards, policy, evaluation, incident response, and deployment lessons.

## Scope

Embodied AI safety covers systems that can sense, reason, decide, communicate or act in the physical world. Relevant systems include:

- Vision-language-action models and robot foundation models
- Mobile robots and service robots
- Humanoids and collaborative robots
- Autonomous vehicles and autonomous shuttles
- Drones and unmanned aircraft
- Maritime and port automation
- Public safety, healthcare, logistics and smart-estate robots
- Agentic AI systems with access to physical-world tools, APIs or infrastructure

Out of scope by default: generic chatbot safety, ordinary LLM evaluations, purely virtual agents, and robotics papers without a safety, security, governance or assurance angle.

## Curation

The default search window starts in **January 2023**, with older foundational robotics safety, security and standards work included where relevant. See [SEARCH_METHOD.md](SEARCH_METHOD.md) for the detailed curation method.

## Contents

- [Surveys and Landscape Papers](#surveys-and-landscape-papers)
- [Policy, Governance and Public Sector](#policy-governance-and-public-sector)
- [Security and Red Teaming](#security-and-red-teaming)
- [Robot Foundation Models and VLA Systems](#robot-foundation-models-and-vla-systems)
- [Safety Frameworks and Technical Methods](#safety-frameworks-and-technical-methods)
- [Benchmarks, Datasets and Evaluation](#benchmarks-datasets-and-evaluation)
- [Standards](#standards)
- [Domain-Specific Safety](#domain-specific-safety)
- [Related Awesome Lists](#related-awesome-lists)

## Surveys and Landscape Papers

- [Safety in Embodied AI: A Survey of Risks, Attacks, and Defenses](https://arxiv.org/abs/2605.02900) - 2026 survey covering attacks and defenses across perception, cognition, planning, action, interaction and agentic systems.
- [Embodied AI: Emerging Risks and Opportunities for Policy Action](https://arxiv.org/abs/2509.00117) - Policy-oriented framing of embodied AI risks and governance opportunities.
- [A Survey on Predictive Safety in Embodied AI](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6562019) - 2026 survey focused on predictive safety across embodied systems.
- [Embodied AI with Foundation Models for Mobile Service Robots: A Systematic Review](https://arxiv.org/abs/2505.20503) - Systematic review on foundation models in mobile service robotics and deployment challenges.

## Policy, Governance and Public Sector

- [International AI Safety Report 2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026) - Broad AI safety synthesis; relevant for agentic systems, tool use, monitoring and containment.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General AI risk management framework useful for structuring EAI safety cases.
- [OECD AI Policy Observatory](https://oecd.ai/) - International AI policy tracker and governance resources.
- [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) - Risk-based AI regulation; relevant to physical-world high-risk AI systems.

## Security and Red Teaming

- [Safety in Embodied AI: A Survey of Risks, Attacks, and Defenses](https://arxiv.org/abs/2605.02900) - Includes adversarial, backdoor, jailbreak and hardware-level attacks across the embodied pipeline.
- [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/) - General AI application security guidance; useful input for EAI control planes and APIs.
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial threat landscape for AI systems.

## Robot Foundation Models and VLA Systems

- [PaLM-E: An Embodied Multimodal Language Model](https://proceedings.mlr.press/v202/driess23a.html) - 2023 embodied multimodal language model for robotics tasks and visual-language reasoning.
- [RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818) - 2023 paper that helped establish VLA models as a robotics paradigm.
- [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) - Cross-embodiment robot dataset and models across many robots, skills and tasks.
- [AutoRT: Embodied Foundation Models for Large Scale Orchestration of Robotic Agents](https://arxiv.org/abs/2401.12963) - Large-scale orchestration of robots using embodied foundation models.
- [The Foundation Model Path to Open-World Robots](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2024/EECS-2024-166.pdf) - 2024 technical report on requirements for robot foundation models.

## Safety Frameworks and Technical Methods

- [SafeEmbodAI: a Safety Framework for Mobile Robots in Embodied AI Systems](https://arxiv.org/abs/2409.01630) - Safety framework for mobile robots using LLM-enabled embodied AI.
- [SafeVLA: Towards Safety Alignment of Vision-Language-Action Model via Constrained Learning](https://arxiv.org/abs/2503.03480) - Safety alignment approach for VLA models.
- [Towards Safe Robot Foundation Models](https://arxiv.org/abs/2503.07404) - Modular safety approach for robot foundation models.
- [Using Large Language Models for Embodied Planning Introduces Systematic Safety Risks](https://arxiv.org/abs/2604.18463) - Empirical work on safety risks in LLM-driven embodied planning.

## Benchmarks, Datasets and Evaluation

- [Open X-Embodiment](https://robotics-transformer-x.github.io/) - Cross-embodiment robotics dataset and RT-X models.
- [Embodied Arena](https://www.dfki.de/web/forschung/projekte-publikationen/publikation/16377) - Evaluation platform for embodied AI capabilities.
- [RoboArena](https://arxiv.org/abs/2506.18123) - Distributed real-world evaluation of generalist robot policies.

## Standards

- [ISO 10218-1:2025](https://www.iso.org/standard/73933.html) - Safety requirements for industrial robots.
- [ISO 10218-2:2025](https://www.iso.org/standard/73934.html) - Safety requirements for robot applications and integration.
- [ISO/TS 15066:2016](https://www.iso.org/standard/62996.html) - Collaborative robot safety guidance.
- [IEEE 2846](https://standards.ieee.org/ieee/2846/6989/) - Assumptions in safety-related models for automated driving systems.

## Domain-Specific Safety

### Autonomous Vehicles

- [IEEE 2846](https://standards.ieee.org/ieee/2846/6989/) - Assumptions in safety-related models for automated driving systems.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General risk management structure that can be adapted to AV and autonomous systems assurance.

### Drones and Unmanned Aircraft

- [JARUS](https://jarus-rpas.org/) - International expert group developing recommendations for remotely piloted aircraft systems.

### Maritime and Ports

- [IMO Maritime Autonomous Surface Ships](https://www.imo.org/en/MediaCentre/HotTopics/Pages/Autonomous-shipping.aspx) - International maritime regulatory work on autonomous shipping.

### Healthcare

- [FDA Artificial Intelligence and Machine Learning in Software as a Medical Device](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-software-medical-device) - Medical AI regulation context relevant to healthcare robots and embodied clinical systems.

### Public Safety

- [NIST Public Safety Communications Research](https://www.nist.gov/ctl/pscr) - Public-safety technology research context relevant to emergency response robotics and field systems.

## Related Awesome Lists

- [Awesome Embodied AI Safety](https://github.com/x-zheng16/Awesome-Embodied-AI-Safety) - Paper-heavy list associated with the 2026 embodied AI safety survey.
- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI) - Broader embodied AI resource list.
- [Awesome Robotics](https://github.com/kiloreux/awesome-robotics) - General robotics resources.
- [Awesome AI Agents for Healthcare](https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare) - Reference style for domain-specific agentic AI curation.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This repository is licensed under [CC BY 4.0](LICENSE).
