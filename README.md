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

The default search window starts in **January 2023**, with older foundational robotics safety, security and standards work included where relevant. The list is expanded using a review-led method: start from major surveys and systematic reviews, then add representative papers, benchmarks and systems chronologically. See [SEARCH_METHOD.md](SEARCH_METHOD.md) for the detailed curation method.

## Contents

- [Papers](#papers)
- [Benchmarks, Datasets and Evaluation](#benchmarks-datasets-and-evaluation)
- [Policy, Governance and Public Sector](#policy-governance-and-public-sector)
- [Security and Red Teaming](#security-and-red-teaming)
- [Standards](#standards)
- [Domain-Specific Safety](#domain-specific-safety)
- [Regional and Jurisdiction-Specific Resources](#regional-and-jurisdiction-specific-resources)
- [Related Awesome Lists](#related-awesome-lists)

## Papers

### 2026

#### June 2026

- [Cosmos 3: Omnimodal World Models for Physical AI](https://arxiv.org/abs/2606.02800) - NVIDIA open world model family for physical AI, spanning multimodal understanding, world simulation, action generation and embodied agent backbones. `world-model`, `physical-ai`, `foundation-model`
- [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://arxiv.org/abs/2506.18123) - Real-world evaluation framework for generalist robot policies. `benchmark`, `evaluation`, `robot-policy`
- [SAFE: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2506.09937) - Failure detector for generalist robot policies, evaluated on OpenVLA, pi0 and pi0-FAST in simulation and real robots. `failure-detection`, `vla`, `runtime-safety`
- [IS-Bench: Evaluating Interactive Safety of VLM-Driven Embodied Agents in Daily Household Tasks](https://arxiv.org/abs/2506.16402) - Benchmark for interactive safety of VLM-driven embodied agents in household scenarios. `benchmark`, `vlm`, `household`
- [AGENTSAFE: Benchmarking the Safety of Embodied Agents on Hazardous Instructions](https://arxiv.org/abs/2506.14697) - Benchmark for embodied agents responding to hazardous instructions. `benchmark`, `hazardous-instructions`, `embodied-agent`

#### May 2026

- [Safety in Embodied AI: A Survey of Risks, Attacks, and Defenses](https://arxiv.org/abs/2605.02900) - Survey covering attacks and defenses across perception, cognition, planning, action, interaction and agentic systems. `survey`, `security`, `risk`
- [Embodied AI with Foundation Models for Mobile Service Robots: A Systematic Review](https://arxiv.org/abs/2505.20503) - Systematic review on foundation models in mobile service robotics and deployment challenges. `survey`, `mobile-robot`, `foundation-model`
- [Embodied AI in Action: Insights from SAE World Congress 2026 on Safety, Trust, Robotics, and Real-World Deployment](https://arxiv.org/abs/2605.10653) - White paper on embodied AI deployment as a systems safety and governance challenge. `white-paper`, `deployment`, `trust`

#### April 2026

- [Vision-Language-Action Safety: Threats, Challenges, Evaluations, and Mechanisms](https://arxiv.org/abs/2604.23775) - Survey of VLA safety across attacks, defenses, evaluation and deployment. `survey`, `vla`, `safety`
- [Using Large Language Models for Embodied Planning Introduces Systematic Safety Risks](https://arxiv.org/abs/2604.18463) - Empirical work on safety risks in LLM-driven embodied planning. `planning`, `llm`, `safety`

### 2025

#### December 2025

- [Safe Learning for Contact-Rich Robot Tasks: A Survey from Classical Learning-Based Methods to Safe Foundation Models](https://arxiv.org/abs/2512.11908) - Survey of safe learning for contact-rich robot tasks, including foundation-model-enabled robots. `survey`, `contact-rich`, `safe-learning`
- [VLA-Arena: An Open-Source Framework for Benchmarking Vision-Language-Action Models](https://arxiv.org/abs/2512.22539) - Benchmarking framework exposing generalization, robustness, safety-constraint and long-horizon limitations in VLAs. `benchmark`, `vla`, `robustness`
- [An Anatomy of Vision-Language-Action Models: From Modules to Milestones and Challenges](https://arxiv.org/abs/2512.11362) - Survey of VLA model modules, milestones and open challenges, including safety and evaluation. `survey`, `vla`, `architecture`

#### September 2025

- [Can AI Perceive Physical Danger and Intervene?](https://arxiv.org/abs/2509.21651) - ASIMOV 2.0 benchmark work on physical danger perception and intervention for embodied AI. `benchmark`, `physical-safety`, `semantic-safety`
- [Embodied AI: Emerging Risks and Opportunities for Policy Action](https://arxiv.org/abs/2509.00117) - Policy-oriented framing of embodied AI risks and governance opportunities. `policy`, `risk`, `governance`

#### August 2025

- [Large VLM-based Vision-Language-Action Models for Robotic Manipulation: A Survey](https://arxiv.org/abs/2508.13073) - Survey of VLM-based VLA models for manipulation and their open challenges. `survey`, `vla`, `manipulation`

#### May 2025

- [A Comprehensive Survey on Physical Risk Control in the Era of Foundation Model-enabled Robotics](https://arxiv.org/abs/2505.12583) - Survey of physical risk control across pre-deployment, pre-incident and post-incident phases for foundation-model-enabled robotics. `survey`, `physical-risk`, `foundation-model`
- [Guided by Guardrails: Control Barrier Functions as Safety Instructors for Robotic Learning](https://arxiv.org/abs/2505.18858) - Uses CBF-based guardrails to shape safer robot learning behavior. `control-barrier-function`, `safe-rl`, `robot-learning`

#### April 2025

- [Large Language and Vision-Language Models for Robot: Safety Challenges, Mitigation Strategies and Future Directions](https://www.sciencedirect.com/science/article/pii/S0143991X2500056X) - Survey of safety challenges and mitigations for LLM/VLM-powered robotics. `survey`, `llm`, `vlm`, `robot-safety`

#### March 2025

- [Gemini Robotics: Bringing AI into the Physical World](https://arxiv.org/abs/2503.20020) - Robotics foundation model report with explicit discussion of semantic and physical safety considerations. `robot-foundation-model`, `semantic-safety`, `deployment`
- [Generating Robot Constitutions & Benchmarks for Semantic Safety](https://arxiv.org/abs/2503.08663) - Introduces ASIMOV benchmark and generated robot constitutions for semantic safety. `benchmark`, `semantic-safety`, `constitution`
- [SafeVLA: Towards Safety Alignment of Vision-Language-Action Model via Constrained Learning](https://arxiv.org/abs/2503.03480) - Safety alignment approach for VLA models. `vla`, `alignment`, `safety`
- [Towards Safe Robot Foundation Models](https://arxiv.org/abs/2503.07404) - Modular safety approach for robot foundation models. `robot-foundation-model`, `safety`, `architecture`

#### February 2025

- [Towards Robust and Secure Embodied AI: A Survey on Vulnerabilities and Attacks](https://arxiv.org/abs/2502.13175) - Survey of embodied AI vulnerabilities and attacks across physical and model-mediated attack surfaces. `survey`, `security`, `robustness`
- [EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://arxiv.org/abs/2502.09560) - Benchmark for evaluating MLLMs as embodied agents across vision-driven tasks. `benchmark`, `mllm`, `embodied-agent`

### 2024

#### December 2024

- [SafeAgentBench: A Benchmark for Safe Task Planning of Embodied LLM Agents](https://arxiv.org/abs/2412.13178) - Benchmark for safety-aware task planning in embodied LLM agents. `benchmark`, `task-planning`, `llm-agent`
- [Towards Generalist Robot Policies: What Matters in Building Vision-Language-Action Models](https://arxiv.org/abs/2412.14058) - Empirical study of design choices in building generalist robot policies. `vla`, `robot-policy`, `generalization`

#### November 2024

- [Embodied Red Teaming for Auditing Robotic Foundation Models](https://arxiv.org/abs/2411.18676) - Automated red-teaming method for discovering unsafe failures in language-conditioned robot models. `red-teaming`, `robot-foundation-model`, `evaluation`

#### October 2024

- [pi0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164) - VLA flow model for general robot control. `vla`, `flow-matching`, `robot-control`
- [Semantically Safe Robot Manipulation: From Semantic Scene Understanding to Motion Safeguards](https://arxiv.org/abs/2410.15185) - Combines semantic scene understanding with control-barrier-style motion safeguards. `semantic-safety`, `manipulation`, `control-barrier-function`
- [Jailbreaking LLM-Controlled Robots](https://arxiv.org/abs/2410.13691) - RoboPAIR attack showing that jailbreaks can elicit harmful physical actions from LLM-controlled robots. `jailbreak`, `llm-robot`, `security`

#### September 2024

- [SafeEmbodAI: a Safety Framework for Mobile Robots in Embodied AI Systems](https://arxiv.org/abs/2409.01630) - Safety framework for mobile robots using LLM-enabled embodied AI. `framework`, `mobile-robot`, `llm`
- [Foundation Models in Robotics: Applications, Challenges, and the Future](https://journals.sagepub.com/doi/10.1177/02783649241281508) - Survey of foundation models in robotics, including applications, challenges and future directions. `survey`, `robot-foundation-model`, `robotics`

#### July 2024

- [Aligning Cyber Space with Physical World: A Comprehensive Survey on Embodied AI](https://arxiv.org/abs/2407.06886) - Broad embodied AI survey spanning robots, simulators and multimodal/world-model approaches. `survey`, `embodied-ai`, `world-model`

#### June 2024

- [OpenVLA: An Open-Source Vision-Language-Action Model](https://arxiv.org/abs/2406.09246) - Open-source 7B VLA trained on diverse robot demonstrations, enabling wider VLA research and evaluation. `vla`, `open-source`, `robot-policy`
- [LLM-Driven Robots Risk Enacting Discrimination, Violence, and Unlawful Actions](https://arxiv.org/abs/2406.08824) - Study of harmful behavior risks in LLM-driven robots. `llm-robot`, `harm`, `bias`

#### May 2024

- [Octo: An Open-Source Generalist Robot Policy](https://arxiv.org/abs/2405.12213) - Open-source generalist robot policy trained on Open X-Embodiment data. `robot-policy`, `open-source`, `generalist`

#### April 2024

- [Learning Control Barrier Functions and their Application in Reinforcement Learning: A Survey](https://arxiv.org/abs/2404.16879) - Survey of learned CBFs and their use in safe reinforcement learning. `survey`, `control-barrier-function`, `safe-rl`

#### March 2024

- [3D-VLA: A 3D Vision-Language-Action Generative World Model](https://arxiv.org/abs/2403.09631) - 3D VLA world-model approach for embodied robotics. `vla`, `world-model`, `3d`
- [Splat-Nav: Safe Real-Time Robot Navigation in Gaussian Splatting Maps](https://arxiv.org/abs/2403.02751) - Safe-by-construction navigation pipeline using Gaussian splatting maps. `navigation`, `safe-planning`, `gaussian-splatting`

#### February 2024

- [A Survey on Robotics with Foundation Models: toward Embodied AI](https://arxiv.org/abs/2402.02385) - Survey of foundation models in robotics, including datasets, simulators, benchmarks and challenges. `survey`, `robotics`, `foundation-model`
- [Highlighting the Safety Concerns of Deploying LLMs/VLMs in Robotics](https://arxiv.org/abs/2402.10340) - Early safety analysis of LLM/VLM-controlled robotics under prompt and perceptual perturbations. `llm`, `vlm`, `robot-safety`
- [A Survey on an Emerging Safety Challenge for Autonomous Vehicles: Safety of the Intended Functionality](https://www.sciencedirect.com/science/article/pii/S2095809924000274) - Survey of SOTIF for autonomous vehicles. `survey`, `autonomous-vehicle`, `sotif`

#### January 2024

- [AutoRT: Embodied Foundation Models for Large Scale Orchestration of Robotic Agents](https://arxiv.org/abs/2401.12963) - Large-scale orchestration of robots using embodied foundation models. `robot-foundation-model`, `multi-robot`, `orchestration`

### 2023

#### November 2023

- [RoboFlamingo: Vision-Language Foundation Models as Effective Robot Imitators](https://arxiv.org/abs/2311.01378) - Adapts vision-language foundation models for robot imitation. `vlm`, `robot-imitation`, `foundation-model`

#### October 2023

- [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) - Cross-embodiment robot dataset and models across many robots, skills and tasks. `dataset`, `robot-learning`, `foundation-model`

#### September 2023

- [Q-Transformer: Scalable Offline Reinforcement Learning via Autoregressive Q-Functions](https://arxiv.org/abs/2309.10150) - Offline RL method for scalable multitask robotic manipulation. `offline-rl`, `robot-learning`, `transformer`

#### July 2023

- [RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818) - Paper that helped establish VLA models as a robotics paradigm. `vla`, `robot-control`, `foundation-model`

#### June 2023

- [RoboCat: A Self-Improving Generalist Agent for Robotic Manipulation](https://arxiv.org/abs/2306.11706) - Self-improving generalist robot manipulation agent. `generalist-agent`, `manipulation`, `robot-learning`
- [SPRINT: Scalable Policy Pre-Training via Language Instruction Relabeling](https://arxiv.org/abs/2306.11886) - Language-instruction relabeling for policy pre-training. `language`, `policy-learning`, `pretraining`

#### May 2023

- [VOYAGER: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291) - Open-ended LLM-powered embodied agent that builds a skill library in Minecraft. `llm-agent`, `open-ended`, `skill-learning`

#### March 2023

- [PaLM-E: An Embodied Multimodal Language Model](https://proceedings.mlr.press/v202/driess23a.html) - Embodied multimodal language model for robotics tasks and visual-language reasoning. `multimodal`, `robotics`, `foundation-model`
- [Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://arxiv.org/abs/2303.04137) - Diffusion-based visuomotor policy learning for robot manipulation. `diffusion-policy`, `visuomotor`, `manipulation`

#### February 2023

- [Describe, Explain, Plan and Select: Interactive Planning with LLMs for Open-World Agents](https://arxiv.org/abs/2302.01560) - LLM-based planning approach for open-world embodied agents. `planning`, `llm-agent`, `open-world`

### Foundational Pre-2023

- [RT-1: Robotics Transformer for Real-World Control at Scale](https://arxiv.org/abs/2212.06817) - Large-scale transformer policy for real-world robot control. `robot-transformer`, `foundation-model`, `control`
- [VIMA: General Robot Manipulation with Multimodal Prompts](https://arxiv.org/abs/2210.03094) - Multimodal prompting formulation for robot manipulation. `multimodal-prompting`, `manipulation`, `robot-policy`
- [ProgPrompt: Generating Situated Robot Task Plans using Large Language Models](https://arxiv.org/abs/2209.11302) - LLM-based programmatic prompting for situated robot task planning. `planning`, `llm`, `robotics`
- [Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/abs/2209.07753) - Uses code-generating language models to express robot policies. `llm`, `embodied-control`, `code-generation`
- [Inner Monologue: Embodied Reasoning through Planning with Language Models](https://arxiv.org/abs/2207.05608) - Uses language-model reasoning and feedback for embodied task planning. `llm`, `planning`, `embodied-reasoning`
- [Robots Enact Malignant Stereotypes](https://arxiv.org/abs/2207.11569) - Study showing harmful social biases in robots using large vision-language models. `bias`, `harm`, `robotics`
- [Gato: A Generalist Agent](https://arxiv.org/abs/2205.06175) - Generalist transformer agent spanning text, games and robotic control. `generalist-agent`, `robotics`, `foundation-model`
- [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/abs/2204.01691) - SayCan grounds language-model plans in robot affordances. `llm`, `affordance`, `planning`
- [Phantom of the ADAS: Securing Advanced Driver-Assistance Systems from Split-Second Phantom Attacks](https://dl.acm.org/doi/10.1145/3372297.3423359) - Physical sensor spoofing attack against ADAS perception. `autonomous-vehicle`, `sensor-spoofing`, `security`
- [Safety Gym: Benchmarking Safe Exploration in Deep Reinforcement Learning](https://arxiv.org/abs/1910.01708) - Benchmark suite for safe exploration in reinforcement learning. `benchmark`, `safe-rl`, `safe-exploration`
- [Control Barrier Functions: Theory and Applications](https://arxiv.org/abs/1903.11199) - Foundational overview of CBFs for safety-critical control. `control-barrier-function`, `safe-control`, `theory`
- [Robust Physical-World Attacks on Deep Learning Visual Classification](https://arxiv.org/abs/1707.08945) - Foundational physical adversarial-example work relevant to robot and AV perception. `physical-attack`, `perception`, `adversarial`
- [Is Deep Learning Safe for Robot Vision? Adversarial Examples Against the iCub Humanoid](https://arxiv.org/abs/1708.06939) - Early demonstration of adversarial examples against humanoid robot vision. `robot-vision`, `adversarial`, `humanoid`
- [Hidden Voice Commands](https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/carlini) - Foundational hidden-command attack against speech interfaces relevant to voice-controlled robots. `audio`, `voice-command`, `security`

## Benchmarks, Datasets and Evaluation

- [Open X-Embodiment](https://robotics-transformer-x.github.io/) - Cross-embodiment robotics dataset and RT-X models.
- [Embodied Arena](https://www.dfki.de/web/forschung/projekte-publikationen/publikation/16377) - Evaluation platform for embodied AI capabilities.
- [ASIMOV Benchmark](https://asimov-benchmark.github.io/) - Semantic and physical safety benchmarks for foundation models serving as robot brains.
- [SafeAgentBench](https://github.com/shengyin1224/SafeAgentBench) - Benchmark and environment for safety-aware task planning of embodied LLM agents.
- [Embodied Red Teaming](https://s-karnik.github.io/embodied-red-team-project-page/) - Project page for red-team evaluation of robotic foundation models.
- [VLA-SAFE](https://vla-safe.github.io/) - Failure detection for VLA policies, including OpenVLA and pi0-family policies.

## Policy, Governance and Public Sector

- [International AI Safety Report 2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026) - Broad AI safety synthesis; relevant for agentic systems, tool use, monitoring and containment.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General AI risk management framework useful for structuring EAI safety cases.
- [NIST: Challenges of Assured Autonomy](https://www.nist.gov/publications/challenges-assured-autonomy) - Assurance, verification and testing challenges for autonomous systems.
- [OECD AI Policy Observatory](https://oecd.ai/) - International AI policy tracker and governance resources.
- [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) - Risk-based AI regulation; relevant to physical-world high-risk AI systems.

## Security and Red Teaming

- [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/) - General AI application security guidance; useful input for EAI control planes and APIs.
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial threat landscape for AI systems.

## Standards

- [ISO 10218-1:2025](https://www.iso.org/standard/73933.html) - Safety requirements for industrial robots.
- [ISO 10218-2:2025](https://www.iso.org/standard/73934.html) - Safety requirements for robot applications and integration.
- [ISO/TS 15066:2016](https://www.iso.org/standard/62996.html) - Collaborative robot safety guidance.
- [ISO 3691-4:2023](https://www.iso.org/standard/83545.html) - Safety requirements for driverless industrial trucks and autonomous mobile robot-like systems.
- [ISO 21448:2022](https://www.iso.org/standard/77490.html) - Safety of the intended functionality for road vehicles, relevant to perception-heavy autonomous systems.
- [UL 4600](https://webstore.ansi.org/standards/ul/ul4600ed2023) - Safety standard for evaluating autonomous products through safety cases and lifecycle assurance.
- [IEEE 2846](https://standards.ieee.org/ieee/2846/6989/) - Assumptions in safety-related models for automated driving systems.

## Domain-Specific Safety

### Autonomous Vehicles

- [IEEE 2846](https://standards.ieee.org/ieee/2846/6989/) - Assumptions in safety-related models for automated driving systems.
- [ISO 21448:2022](https://www.iso.org/standard/77490.html) - SOTIF guidance for hazards caused by functional insufficiencies and foreseeable misuse.
- [UL 4600](https://webstore.ansi.org/standards/ul/ul4600ed2023) - Safety-case standard for autonomous products.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General risk management structure that can be adapted to AV and autonomous systems assurance.

### Drones and Unmanned Aircraft

- [JARUS](https://jarus-rpas.org/) - International expert group developing recommendations for remotely piloted aircraft systems.

### Maritime and Ports

- [IMO Maritime Autonomous Surface Ships](https://www.imo.org/en/MediaCentre/HotTopics/Pages/Autonomous-shipping.aspx) - International maritime regulatory work on autonomous shipping.

### Healthcare

- [FDA Artificial Intelligence and Machine Learning in Software as a Medical Device](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-software-medical-device) - Medical AI regulation context relevant to healthcare robots and embodied clinical systems.

### Public Safety

- [NIST Public Safety Communications Research](https://www.nist.gov/ctl/pscr) - Public-safety technology research context relevant to emergency response robotics and field systems.

## Regional and Jurisdiction-Specific Resources

- [Singapore Embodied AI Safety Resources](SINGAPORE.md) - Singapore-specific policy, governance, testbed and public-sector resources relevant to embodied AI safety.

## Related Awesome Lists

- [Awesome Embodied AI Safety](https://github.com/x-zheng16/Awesome-Embodied-AI-Safety) - Paper-heavy list associated with the 2026 embodied AI safety survey.
- [Awesome Embodied AI](https://github.com/haoranD/Awesome-Embodied-AI) - Broader embodied AI resource list.
- [Awesome Robotics](https://github.com/kiloreux/awesome-robotics) - General robotics resources.
- [Awesome AI Agents for Healthcare](https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare) - Reference style for domain-specific agentic AI curation.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This repository is licensed under [CC BY 4.0](LICENSE).
