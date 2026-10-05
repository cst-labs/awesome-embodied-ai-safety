# Awesome Embodied AI (EAI) Safety

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated, deployment-minded guide to safety, security, governance and assurance for embodied AI systems: robots, autonomous vehicles, drones, humanoids, service robots, industrial robots, maritime systems, smart infrastructure and AI agents that act through physical systems.

This list is intentionally broader than safety papers. It includes technical safety research, frontier embodied-AI capability papers, cyber-physical security, human-robot interaction, standards, policy, evaluation, incident response, and deployment lessons.

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

Out of scope by default: generic chatbot safety, ordinary LLM evaluations, purely virtual agents, and incremental robotics papers without a safety, security, governance, assurance or frontier embodied-AI capability angle.

## Curation

The default search window starts in **January 2023**, with older foundational robotics safety, security and standards work included where relevant. The list is expanded using a review-led method: start from major surveys and systematic reviews, then add representative papers, benchmarks and systems chronologically. See [SEARCH_METHOD.md](SEARCH_METHOD.md) for the detailed curation method and [RISK_TOPICS.md](RISK_TOPICS.md) for a topic-oriented risk and reading map.

## Contents

- [Papers](#papers)
- [Benchmarks, Datasets and Evaluation](#benchmarks-datasets-and-evaluation)
- [Policy, Governance and Public Sector](#policy-governance-and-public-sector)
- [Security and Red Teaming](#security-and-red-teaming)
- [Standards](#standards)
- [Domain-Specific Safety](#domain-specific-safety)
- [Regional and Jurisdiction-Specific Resources](#regional-and-jurisdiction-specific-resources)
- [Related Awesome Lists](#related-awesome-lists)
- [Risk Topics and Reading Map](RISK_TOPICS.md)

## Papers

### 2026

#### September 2026

- [Rethinking Safety for Generalist Robots](https://arxiv.org/abs/2609.06326) - Perspective proposing a lifecycle-wide risk taxonomy and research agenda for context-dependent hazards, user intent and physical consequences in generalist robots. `perspective`, `robot-foundation-model`, `physical-risk`
- [Humanoid Safe Stop via Learned Stoppability Value](https://arxiv.org/abs/2609.02358) - Combines a learned stopping policy with stop-probability and reach-avoid estimators to choose between stopping and a damping fallback after a humanoid emergency-stop command. `humanoid`, `safe-control`, `runtime-assurance`
- [Do Better Imagined Rollouts Mean Better Robot Control? A Controlled Study of World-Model Evaluation Under Feedback](https://arxiv.org/abs/2609.02811) - Controlled mobile-robot study showing that offline estimator rankings can diverge from closed-loop tracking performance when evaluation omits deployment-time sensing corrections. `evaluation`, `world-model`, `mobile-robot`, `robustness`
- [Sensing Which Modality Matters: Evidence-Gated Regularization for Robust VLA Policies](https://arxiv.org/abs/2609.03142) - Introduces a sensor-corruption benchmark and evidence-gated training objective for VLA robustness under occlusions, distractors and single-sensor fallback, with simulation and real-robot evaluation. `benchmark`, `vla`, `robustness`, `perception`
- [Benchmarking Robots for Everyday Environments: From Lab Experiments to Real-World Operations](https://arxiv.org/abs/2609.26490) - Interdisciplinary evaluation framework incorporating safety, interaction quality and operational feasibility across public-space cleaning and library-assistance deployments. `benchmark`, `human-robot-interaction`, `deployment`, `service-robot`
- [NavSafe-∞: Benchmarking Closed-Loop Driving Safety in Photorealistic Environments](https://arxiv.org/abs/2609.26618) - Closed-loop driving benchmark with 280 scenarios across 28 event types, examining safety failures that open-loop policy scores can miss. `benchmark`, `autonomous-vehicle`, `safety`
- [LIBERO-RECOVER: Beyond Task Success Towards Failure Recovery in Robotic Manipulation Models](https://arxiv.org/abs/2609.05178) - Benchmark built from robot-policy execution failures in LIBERO to evaluate retries, action adaptation, object-state recovery and environmental recovery. `benchmark`, `vla`, `failure-recovery`
- [FailureSpot: Label-Efficient Timestamp-Level Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2609.04277) - Combines action-derived weak supervision with selective timestamp annotation to localize VLA execution failures while reducing dense-label requirements. `failure-detection`, `vla`, `runtime-safety`
- [CALM: Configuration-Aware Human Intervention Boundaries During Robot Approach](https://arxiv.org/abs/2609.07430) - Human study models how humanoid arm configuration affects intervention distances during approach, distinguishing behavioral boundaries from physical safety guarantees. `human-robot-interaction`, `humanoid`, `safe-planning`
- [Safety-Critical Scenarios Emerge from Initial Scenes](https://arxiv.org/abs/2609.20103) - AdvScene generates realistic initial driving scenes that expose black-box policies to more ego-fault collisions and low-time-to-collision events in closed-loop simulation. `autonomous-vehicle`, `red-teaming`, `scenario-generation`
- [SafeStage: Evaluating Safety Before, During, and After Vision-Language-Conditioned Robot Manipulation](https://arxiv.org/abs/2609.21223) - Lifecycle-structured benchmark with 97 risk scenarios that separates task success from initial-state, execution-time and final-state safety violations. `benchmark`, `vla`, `physical-safety`
- [VLA-Scope: Shift-Aware Failure Prediction for Vision-Language-Action Models](https://arxiv.org/abs/2609.21246) - Predicts OpenVLA failures under distribution shift by combining input-shift categories, action prefixes and execution progress. `failure-detection`, `vla`, `distribution-shift`
- [ProTracer: Proprioception-Guided Failure Diagnosis in Robot Manipulation](https://arxiv.org/abs/2609.21369) - Training-free VLM framework and FailTime benchmark for failure detection, categorization, explanation and onset localization using synchronized vision and proprioception. `failure-detection`, `benchmark`, `multimodal`
- [CommitFlow: Semantic Commitment Verification and Local Correction for Long-Horizon Robot Manipulation VLA Execution](https://arxiv.org/abs/2609.21908) - Monitors whether required physical conditions hold before a VLA advances task stages and applies local corrective actions with the base policy frozen. `vla`, `runtime-assurance`, `failure-recovery`
- [LIMBO: Learning and Internalizing Model-Free Barrier Objectives for Agile and Safe Whole-Body Control](https://arxiv.org/abs/2609.22075) - Learns a state-action control barrier function from black-box transitions and distills it into humanoid task policies demonstrated on hardware without an online safety filter. `safe-control`, `control-barrier-function`, `humanoid`
- [RAFAIL: Relationship-Aware Failure Detection for Robotic Manipulation](https://arxiv.org/abs/2609.18324) - Detects real-robot manipulation failures from anomalies in task-relevant entity relationships without failure training data or runtime VLM inference. `failure-detection`, `runtime-safety`, `manipulation`
- [VLPSA: Vision-Language-Poisson-Safe Actions for Full-Body Safety of Learned Policies](https://arxiv.org/abs/2609.22462) - Perception-driven Poisson safety functions filter VLA actions for robot-body and grasped-object collision avoidance, evaluated in SafeLIBERO and on a Franka FR3. `vla`, `safe-control`, `control-barrier-function`
- [Toward Human-in-the-Loop Robot Failure Recovery: Bridging Communication Gaps in Human-Robot Collaboration](https://arxiv.org/abs/2609.24055) - LD-HRI benchmark measures how differences in listener knowledge affect the usefulness of robot requests for human assistance during failure recovery. `benchmark`, `human-robot-interaction`, `failure-recovery`
- [Safety-Constrained Model Predictive Control for an Omnidirectional Walking Assistive Robot Using Control Barrier Function](https://arxiv.org/abs/2609.25994) - Combines CBF collision constraints with predictive control for walking assistance, evaluated with 12 healthy participants. `healthcare`, `human-robot-interaction`, `control-barrier-function`
- [BranchDrive: A Branch-Structured Dataset for Action-Conditioned Driving Prediction](https://arxiv.org/abs/2609.27275) - CARLA benchmark pairing shared driving histories with alternative intervention futures for offline outcome prediction and decision evaluation, with closed-loop safety improvement still unestablished. `benchmark`, `dataset`, `autonomous-vehicle`, `evaluation`
- [Turning Safety into Competence: Minimally Exploitable Robot Policies via Safety-Filtered Reinforcement Learning](https://arxiv.org/abs/2609.27312) - Separates adversarial safety-filter learning from competitive task learning and evaluates exploitability in simulated games and hardware stress tests. `safe-rl`, `safe-control`, `adversarial`
- [LEAP-CBF: A Safety Filter for Uncertain Systems with Least-Effort Adversarial Potentials](https://arxiv.org/abs/2609.28364) - Learns safety certificates for disturbances with bounded cumulative effort, with simulation and quadruped and quadrotor hardware evaluations. `safe-control`, `control-barrier-function`, `drone`
- [CrossSafe: Towards Cross-Embodiment Latent Safety Filters](https://arxiv.org/abs/2609.28984) - Morphology-conditioned latent reachability filters reduce whole-body collisions across bimanual manipulation embodiments, including a held-out robot. `safe-control`, `runtime-assurance`, `cross-embodiment`
- [ConflictVLA-Bench: Benchmarking Behavioral Responses of Vision-Language-Action Models to Premise Conflicts](https://arxiv.org/abs/2609.31792) - VLA benchmark that finds “Failed Persistence”: models often continue pursuing an invalid objective despite task failure, so outcome-only evaluation cannot demonstrate disengagement. `benchmark`, `vla`, `semantic-safety`, `failure-analysis`
- [PlanGuard: A Guardrail for Multi-Step Plan Safety in Embodied Agents](https://arxiv.org/abs/2609.32801) - Pre-execution physical-risk detector for complete embodied task plans, with the MSP-Safe dataset and a compact distilled guardrail model; code and data are announced but not yet released. `planning`, `physical-safety`, `guardrail`, `benchmark`
- [FP2: Equipping Robotic Foundation Models with Force Control](https://arxiv.org/abs/2609.37433) - Adds a high-frequency, feedback-driven force-control interface to task-adapted robot foundation policies, evaluated across four real-world contact-rich manipulation tasks. `safe-control`, `force-control`, `robot-foundation-model`, `contact-rich`
- [Praxis-1](https://runway.com/research/introducing-praxis-1) - Runway technical release describing a video-pretrained world-action model for multi-embodiment robot control; it is in partner testing and the announced weights are not yet publicly available. `world-action-model`, `robot-foundation-model`, `physical-ai`, `early-access`
- [FLUX 3 Action](https://bfl.ai/models/flux-3-action) - Technical report on an open-weight 7B world-action model jointly predicting video and robot actions, with embodiment adaptation and inference-efficiency evaluations. `world-model`, `robot-foundation-model`, `open-release`
- [Helix 2.5: Zero-Shot 30-Home Generalization](https://www.figure.ai/news/helix-2-5-zero-shot-30-home-generalization) - Figure technical report on human-data pretraining and three adapted whole-body humanoid behaviors evaluated in 30 unseen homes, with company-reported generalization results. `robot-foundation-model`, `humanoid`, `frontier-capability`, `technical-report`
- [PopNavShift: Stress-Testing Social Navigation under Behavioral Population Shift](https://arxiv.org/abs/2609.21838) - Matched simulation framework showing that pedestrian-population shifts can reverse social-navigation controller rankings, especially on pedestrian-burden metrics. `benchmark`, `social-navigation`, `human-robot-interaction`

#### August 2026

- [Particle-Based Conformal Prediction for Contact-Aware Uncertainty Calibration in Stratified Configuration Spaces](https://arxiv.org/abs/2608.09166) - Contact-aware conformal uncertainty calibration for manipulation and planning, improving coverage and task success in contact-rich robot settings. `safe-control`, `uncertainty`, `contact-rich`
- [SAFE-CHEM: Uncertainty-Aware Policy Switching for Robust Robotic Chemistry](https://arxiv.org/abs/2608.09303) - Ensemble-based uncertainty monitor that switches robotic chemistry tasks to a rule-based backup controller before unsafe out-of-distribution actions. `runtime-safety`, `uncertainty`, `chemistry`
- [Toward the Cognitive-Physical Limits of Foundation Models in Autonomous Racing](https://arxiv.org/abs/2608.10618) - Evaluates whether current frontier models can support low-latency, safety-critical autonomous racing with onboard perception, prediction and control, exposing embodied world-model and planning limits under real physical constraints. `autonomous-vehicle`, `world-model`, `assurance`
- [Isaac 0.5: Percepts Scale Control](https://pub-d90b81cad7254a1aa6b148ac18153c0c.r2.dev/isaac-0.5.pdf) - Perceptron technical report on a 36B open-weight model combining video understanding, embodied reasoning and robot control, with released adaptation and evaluation code but a proprietary video-training objective. `robot-foundation-model`, `vla`, `open-release`, `world-model`
- [Introducing S1: In-Context Learning for Robotics](https://skild.ai/blogs/s1) - Skild AI technical article reporting execution of unseen long-horizon manipulation tasks from a single video demonstration without task-specific weight updates. `robot-foundation-model`, `in-context-learning`, `long-horizon`

#### July 2026

- [Neuro-Symbolic Safety Guidance for Vision-Language-Action Models via Constrained Flow Matching](https://arxiv.org/abs/2607.01378) - Predictive collision-avoidance layer for flow-matching VLAs that corrects unsafe trajectories during denoising rather than only filtering the next action. `vla`, `safe-control`, `neuro-symbolic`, `runtime-safety`
- [ACE-Brain-0.5: A Unified Embodied Foundational Model for Physical Agentic AI](https://arxiv.org/abs/2607.04426) - Closed-loop embodied foundation model that unifies spatial reasoning, action, self-monitoring and self-improvement, materially raising the capability and recovery baseline for physical AI agents. `robot-foundation-model`, `physical-ai`, `self-monitoring`
- [RoboDojo: A Unified Sim-and-Real Benchmark for Comprehensive Evaluation of Generalist Robot Manipulation Policies](https://arxiv.org/abs/2607.04434) - Sim-and-real benchmark spanning 42 simulation tasks and 18 real-world tasks for diagnosing robustness, memory, precision, long-horizon execution and open-vocabulary manipulation. `benchmark`, `evaluation`, `robot-policy`
- [RoboVista: Evaluating Vision Language Models for Diverse Robot Applications](https://arxiv.org/abs/2607.04610) - Cross-domain robotics benchmark for VLM reasoning across industrial, agricultural, domestic, surgical and driving use cases, exposing persistent gaps between robot reasoning and execution. `benchmark`, `vlm`, `cross-domain`
- [From Fixed to Free Cameras: Calibration-Free View-Robust Vision-Language-Action Model](https://arxiv.org/abs/2607.05396) - Calibration-free VLA that improves robustness to camera remounting and viewpoint shifts, reducing a practical deployment fragility in real robot setups. `vla`, `robustness`, `deployment`
- [From Foundation to Application: Improving VLA Models in Practice](https://arxiv.org/abs/2607.06403) - LingBot-VLA 2.0 extends generalist VLA capability toward whole-body, cross-embodiment and long-horizon mobile manipulation with predictive dynamics modeling. `vla`, `mobile-robot`, `frontier-capability`
- [Xiaomi-Robotics-U0: Unified Embodied Synthesis with World Foundation Model](https://arxiv.org/abs/2607.11643) - World foundation model for robot-centric multi-view scene generation, embodied transfer and video synthesis, with reported downstream gains from generated training data. `world-model`, `physical-ai`, `dataset`
- [Masked Visual Actions for Unified World Modeling in Autonomous Driving](https://arxiv.org/abs/2507.19343) - Introduces a unified driving world-model stack that jointly predicts visual futures and low-level actions, materially extending simulation and planning capability for safety-critical AV evaluation. `autonomous-vehicle`, `world-model`, `simulation`
- [ABot-World-0: Infinite Interactive World Rollout on a Single Desktop GPU](https://arxiv.org/abs/2607.19191) - Real-time action-conditioned interactive world model aimed at long-horizon closed-loop physical-AI simulation on modest hardware. `world-model`, `physical-ai`, `simulation`
- [NavVerse: Benchmarking Indoor-to-Outdoor Embodied Navigation in Continuous Robot Simulation](https://arxiv.org/abs/2607.19695) - Navigation benchmark spanning indoor, outdoor and transition episodes with executable robot interfaces and explicit safety metrics, exposing major cross-context failures for current VLAs. `benchmark`, `navigation`, `safety-metrics`
- [KineBench: Benchmarking Embodied World Models via IDM-Free Kinematic Grounding](https://arxiv.org/abs/2607.19876) - Closed-loop benchmark for embodied world models that removes inverse-dynamics confounds and adds robot-centric kinematic safety and plausibility metrics. `benchmark`, `world-model`, `evaluation`
- [SceneActBench: Can Agents Act on the 3D Scenes They See?](https://arxiv.org/abs/2607.22393) - Benchmark for visually conditioned action on full 3D scenes, showing large failure gaps when VLM agents must act rather than only describe or classify environments. `benchmark`, `3d-scenes`, `agent-evaluation`

#### June 2026

- [Safe Embodied AI for Long-horizon Tasks: A Cross-layer Analysis of Robotic Manipulation](https://arxiv.org/abs/2606.05660) - Cross-layer survey framing long-horizon manipulation safety across capability backbones, safeguards and evaluation gaps. `survey`, `manipulation`, `long-horizon`, `safety`
- [Cosmos 3: Omnimodal World Models for Physical AI](https://arxiv.org/abs/2606.02800) - NVIDIA open world model family for physical AI, spanning multimodal understanding, world simulation, action generation and embodied agent backbones. `world-model`, `physical-ai`, `foundation-model`
- [Kairos: A Native World Model Stack for Physical AI](https://arxiv.org/abs/2606.16533) - Cross-embodiment world-model stack for physical AI that unifies world understanding, generation and action prediction with deployment-aware long-horizon state tracking. `world-model`, `physical-ai`, `robot-foundation-model`
- [Benchmarking Vision-Language-Action Models on SO-101: Failure and Recovery Analysis](https://arxiv.org/abs/2606.08881) - Real-world low-cost robot benchmark for VLA robustness, with structured failure taxonomy and recovery-aware evaluation metrics. `benchmark`, `vla`, `failure-analysis`
- [ActProbe: Action-Space Probe for Early Failure Detection of Generative Robot Policies](https://arxiv.org/abs/2606.08508) - Lightweight action-space detector for early failure prediction in generative robot policies, including transfer to real-robot deployment. `failure-detection`, `robot-policy`, `runtime-safety`
- [Embedding ISO 10218 Safety Compliance in Robots via Control Barrier Functions for Human-Robot Collaboration](https://arxiv.org/abs/2606.13203) - Control-barrier-function safety filter for human-robot collaboration that targets ISO 10218-style speed-and-separation compliance. `safe-control`, `control-barrier-function`, `standards`
- [Embodied-R1.5: Evolving Physical Intelligence via Embodied Foundation Models](https://arxiv.org/abs/2606.11324) - Open embodied foundation model release with closed-loop planning, grounding and self-correction plus real-robot transfer and evaluation infrastructure. `robot-foundation-model`, `physical-ai`, `open-release`
- [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://arxiv.org/abs/2506.18123) - Real-world evaluation framework for generalist robot policies. `benchmark`, `evaluation`, `robot-policy`
- [SAFE: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2506.09937) - Failure detector for generalist robot policies, evaluated on OpenVLA, pi0 and pi0-FAST in simulation and real robots. `failure-detection`, `vla`, `runtime-safety`
- [RoboSemanticBench: Diagnosing Semantic Grounding in Action Prediction for VLA Models](https://arxiv.org/abs/2606.02277) - Benchmark showing that many VLA policies grasp reliably but fail to map instruction semantics to the correct physical target. `benchmark`, `vla`, `semantic-safety`
- [IS-Bench: Evaluating Interactive Safety of VLM-Driven Embodied Agents in Daily Household Tasks](https://arxiv.org/abs/2506.16402) - Benchmark for interactive safety of VLM-driven embodied agents in household scenarios. `benchmark`, `vlm`, `household`
- [AGENTSAFE: Benchmarking the Safety of Embodied Agents on Hazardous Instructions](https://arxiv.org/abs/2506.14697) - Benchmark for embodied agents responding to hazardous instructions. `benchmark`, `hazardous-instructions`, `embodied-agent`
- [PACT: Self-Evolving Physical Safety Alignment for Diffusion Policies in Embodied Manipulation](https://arxiv.org/abs/2606.08414) - Post-training method for safer diffusion robot policies that projects trajectories toward feasible constraint regions while reducing violations in real and simulated manipulation. `safe-control`, `manipulation`, `diffusion-policy`

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

- [Feedback-Aware Evaluation of Predictive Robot Models](https://github.com/rdharini2001/Robot_World_Model) - Mobile-robot simulation testbed comparing offline prediction and closed-loop tracking across sensing degradations, with evaluation scripts, checkpoints and reference results.
- [Perceptron Isaac](https://github.com/perceptron-ai-inc/isaac) - Isaac 0.5 adaptation, inference and evaluation resources with [open weights](https://huggingface.co/PerceptronAI/Isaac-0.5); uses a dedicated LeRobot integration with documented additional runtime requirements.
- [Xiaomi-Robotics-U0](https://github.com/XiaomiRobotics/Xiaomi-Robotics-U0) - Open training and inference framework for embodied scene and video synthesis, with September 2026 releases of 4B and sequence checkpoints, including [4B-Sequence weights](https://huggingface.co/XiaomiRobotics/Xiaomi-Robotics-U0-4B-Sequence).
- [RoboHarm](https://robocurve.org/roboharm/) - Five fixed-scene real-robot refusal tasks with trial-level results and [benchmark code](https://github.com/robocurve/roboharm), distinguishing refusal from failed execution; the repository documents replication gaps and does not bundle raw rollouts.
- [PhAIL](https://phail.ai/about) - Physical AI evaluation and leaderboard layer that adds real-robot validation, hidden test splits and safety-oriented generalization checks beyond simulator-only scoring.
- [VLA Evaluation Harness](https://github.com/allenai/vla-evaluation-harness) - AllenAI evaluation harness for reproducible VLA benchmarking across tasks, prompts and execution settings.
- [FLUX 3 Action weights](https://huggingface.co/collections/black-forest-labs/flux-3-action) - Base, SO-101 and DROID checkpoints for reproducing and evaluating world-action policies, released under the FLUX Kommunity license and requiring application-level motion safety limits.
- [OopsieVerse](https://robin-lab.cs.utexas.edu/oopsieverse/) - Damage-aware simulation and benchmark suite that scores household manipulation by physical harm, not just task completion, across mechanical, thermal and fluid failure modes.
- [RoboDojo](http://robodojo-benchmark.com/) - Unified sim-and-real benchmark with standardized real-world evaluation and leaderboard for generalist robot manipulation policies.
- [RoboVista](https://arxiv.org/abs/2607.04610) - Cross-domain benchmark for robot-facing VLM reasoning over industrial, agricultural, domestic, surgical and driving scenarios.
- [NavVerse Benchmark](https://huggingface.co/datasets/tccoin/navverse-benchmark) - Indoor-to-outdoor embodied navigation benchmark dataset for physically grounded evaluation across object, place and vision-language navigation tasks.
- [SceneActBench](https://github.com/Feinaldo2/SceneActBench) - Benchmark harness for VLM agents acting on full 3D scenes across layout, pose, articulation, reconstruction and dynamic-scene tasks.
- [Open X-Embodiment](https://robotics-transformer-x.github.io/) - Cross-embodiment robotics dataset and RT-X models.
- [Embodied Arena](https://www.dfki.de/web/forschung/projekte-publikationen/publikation/16377) - Evaluation platform for embodied AI capabilities.
- [ASIMOV Benchmark](https://asimov-benchmark.github.io/) - Semantic and physical safety benchmarks for foundation models serving as robot brains.
- [EmbodiedEvalKit](https://github.com/pickxiguapi/EmbodiedEvalKit) - Unified evaluation framework for 25+ embodied benchmarks with API, Hugging Face and vLLM backends.
- [RoboArena](https://robo-arena.github.io/) - Community-run real-world benchmark for generalist robot policies with distributed pairwise evaluation on DROID.
- [NVIDIA Cosmos](https://github.com/NVIDIA/Cosmos) - Open platform of world models, datasets, evaluation tools and robot policy assets for physical AI.
- [SafeAgentBench](https://github.com/shengyin1224/SafeAgentBench) - Benchmark and environment for safety-aware task planning of embodied LLM agents.
- [Embodied Red Teaming](https://s-karnik.github.io/embodied-red-team-project-page/) - Project page for red-team evaluation of robotic foundation models.
- [VLA-SAFE](https://vla-safe.github.io/) - Failure detection for VLA policies, including OpenVLA and pi0-family policies.
- [SAFE](https://github.com/vla-safe/SAFE) - Official code for multitask failure detection on VLA policies.
- [IS-Bench](https://github.com/AI45Lab/IS-Bench) - Official data and code for interactive safety evaluation of VLM-driven household embodied agents.
- [ConflictVLA-Bench](https://github.com/EmbodiedAISurvey/ConflictVLA-Bench) - Public benchmark implementation and experimental details for testing VLA premise-conflict responses and “Failed Persistence.”

## Policy, Governance and Public Sector

- [International AI Safety Report 2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026) - Broad AI safety synthesis; relevant for agentic systems, tool use, monitoring and containment.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General AI risk management framework useful for structuring EAI safety cases.
- [NIST: Challenges of Assured Autonomy](https://www.nist.gov/publications/challenges-assured-autonomy) - Assurance, verification and testing challenges for autonomous systems.
- [OECD AI Policy Observatory](https://oecd.ai/) - International AI policy tracker and governance resources.
- [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) - Risk-based AI regulation; relevant to physical-world high-risk AI systems.
- [EU AI Act FAQ on AI Agents](https://digital-strategy.ec.europa.eu/en/faqs/questions-and-answers-ai-agents) - August 2026 Commission FAQ clarifying how AI agent rules map to transparency duties now and to later high-risk obligations when deployed into regulated physical systems.
- [Commission Guidelines on High-Risk AI Systems](https://digital-strategy.ec.europa.eu/en/library/commission-guidelines-high-risk-ai-systems-ai-act) - Operational guidance on when AI becomes part of a high-risk product stack, useful for robotics, industrial machinery and autonomous-system compliance planning.
- [EU AI Act Implementation Timeline](https://ai-act-service-desk.ec.europa.eu/en/ai-act/eu-ai-act-implementation-timeline) - Official milestone tracker clarifying that transparency obligations and enforcement started on 2 August 2026, which matters for robots and physical AI systems interacting with people.

## Security and Red Teaming

- [NIST SP 800-82 Rev. 4: Guide to Operational Technology Security — Initial Public Draft](https://csrc.nist.gov/pubs/sp/800/82/r4/ipd) - September 2026 draft guidance for securing physical control systems while accounting for safety and reliability, including industrial, transportation and maritime OT.
- [ROSClaw](https://github.com/ros-claw/rosclaw) - Open runtime and control-plane project for embodied agents with sandbox safety, capability routing, safety validation and evidence-bearing execution traces. `runtime-security`, `physical-ai`, `open-source`
- [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/) - General AI application security guidance; useful input for EAI control planes and APIs.
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial threat landscape for AI systems.

## Standards

- [Commission Implementing Decision (EU) 2026/2015](https://www.boe.es/doue/2026/2015/L00001-00010.pdf) - Published 7 September 2026, adds EN ISO 10218-1:2025 and EN ISO 10218-2:2025 to harmonised machinery-standard references under Directive 2006/42/EC; official Spanish-language text.
- [ISO 10218-1:2025](https://www.iso.org/standard/73933.html) - Safety requirements for industrial robots.
- [ISO 10218-2:2025](https://www.iso.org/standard/73934.html) - Safety requirements for robot applications and integration.
- [ISO/TS 15066:2016](https://www.iso.org/standard/62996.html) - Collaborative robot safety guidance.
- [ISO 3691-4:2023](https://www.iso.org/standard/83545.html) - Safety requirements for driverless industrial trucks and autonomous mobile robot-like systems.
- [ISO 21448:2022](https://www.iso.org/standard/77490.html) - Safety of the intended functionality for road vehicles, relevant to perception-heavy autonomous systems.
- [ITU-T F.748.66](https://www.itu.int/rec/T-REC-F.748.66/en) - International framework standard for embodied AI systems covering functional architecture, capability boundaries and safety-related deployment considerations.
- [UL 4600](https://webstore.ansi.org/standards/ul/ul4600ed2023) - Safety standard for evaluating autonomous products through safety cases and lifecycle assurance.
- [IEEE 2846](https://standards.ieee.org/ieee/2846/6989/) - Assumptions in safety-related models for automated driving systems.

## Domain-Specific Safety

- [Intrinsic Core](https://github.com/intrinsic-ai/intrinsic-core) - Open industrial robotics runtime, SDK, digital twin and hardware-independent real-time control framework, providing a reusable platform for deployment and assurance research.

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

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This repository is licensed under [CC BY 4.0](LICENSE).
