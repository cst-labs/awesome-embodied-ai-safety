# Search Method

This file documents the search and curation method for expanding Awesome Embodied AI (EAI) Safety.

## Curation Starting Point

The default search window starts in **January 2023**.

Rationale: 2023 is when embodied foundation models became a significant topic for safety work, with PaLM-E, RT-2 and Open X-Embodiment showing a clearer path from large multimodal models to robot reasoning and action. Older work is still included when it is foundational, especially robotics safety standards, human-robot interaction safety, autonomous vehicle safety, control theory, formal methods and cybersecurity.

## Source Types

- Review backbones: recent surveys and systematic reviews are used first to identify the field boundaries, recurring taxonomies and high-signal papers.
- Academic search: arXiv, Semantic Scholar, Google Scholar, IEEE Xplore, ACM Digital Library, Science Robotics, IJRR, RSS, CoRL, ICRA, IROS, NeurIPS, ICML, CVPR, ACL and AAAI.
- Standards and guidance: ISO, IEC, IEEE, NIST, OECD, national AI safety institutes, sector regulators and public-sector guidance bodies.
- Repositories: GitHub topics and search for `embodied-ai`, `robotics-safety`, `vla`, `robot-foundation-model`, `humanoid-robot`, `autonomous-vehicles`, `robot-security`, `ai-assurance`.
- Benchmarks and datasets: project sites, Hugging Face, Papers with Code, Open X-Embodiment, embodied AI leaderboards and robot evaluation platforms.
- Deployment sources: government sandboxes, autonomous vehicle pilots, public robot testbeds, incident reports and credible technical blogs.

## Review-Led Expansion Method

The repository should be expanded from survey and review papers before broad keyword search. This keeps the list more systematic and avoids over-weighting whatever happens to rank highly in search results.

### Step 1: Seed From Literature Reviews

Use these review backbones first:

- Safety in Embodied AI: A Survey of Risks, Attacks, and Defenses
- Vision-Language-Action Safety: Threats, Challenges, Evaluations, and Mechanisms
- Towards Robust and Secure Embodied AI: A Survey on Vulnerabilities and Attacks
- A Comprehensive Survey on Physical Risk Control in the Era of Foundation Model-enabled Robotics
- Embodied AI with Foundation Models for Mobile Service Robots: A Systematic Review
- Foundation Models in Robotics: Applications, Challenges, and the Future
- A Survey on Robotics with Foundation Models: toward Embodied AI
- Large Language and Vision-Language Models for Robot: Safety Challenges, Mitigation Strategies and Future Directions

For each review, extract papers that fall into at least one of these buckets:

- Direct safety, security, robustness, alignment or governance contribution.
- Benchmark or dataset for embodied safety, failure detection, robustness or evaluation.
- Foundational VLA, robot foundation model or embodied agent paper that changes deployment risk.
- Domain paper with direct physical-world safety relevance: autonomous vehicles, drones, humanoids, service robots, healthcare, public safety, industrial robots or maritime systems.

Coverage targets for the first comprehensive pass:

- Surveys and landscape papers.
- VLA and robot foundation model anchors.
- Embodied LLM/VLM planning and agent papers.
- Safety benchmarks and failure-detection methods.
- Red-teaming, jailbreaking, prompt-injection and adversarial evaluation.
- Physical-world perception attacks and defenses.
- Classical safe control, safe RL, CBFs, shielding, runtime assurance and reachability.
- Human-robot interaction and social harm papers.
- Domain-specific safety for autonomous vehicles, drones, humanoids, healthcare, industrial/service robots and maritime systems.
- Standards, assurance frameworks and safety-case resources.

### Step 2: Deduplicate and Tag

Deduplicate by title and arXiv ID/DOI. Keep the earliest public version date for chronological placement. Add lightweight tags such as `survey`, `vla`, `benchmark`, `red-teaming`, `failure-detection`, `policy`, `robot-foundation-model`, `physical-risk`, or `semantic-safety`.

### Step 3: Add Chronologically

Place papers in the README under `Papers` by year and month. Within each month, put surveys first, then benchmarks/evaluation papers, then methods/systems. Keep descriptions to one sentence.

### Step 4: Promote Stable Resources

Move durable non-paper resources into thematic sections:

- Benchmarks, datasets and evaluation platforms.
- Policy and governance.
- Security and red-teaming resources.
- Standards.
- Domain-specific references.
- Regional or jurisdiction-specific pages.

### Step 5: Re-run Monthly

Each month, repeat targeted searches on arXiv, Semantic Scholar, Google Scholar, Papers with Code, Hugging Face Papers and GitHub. Add newly discovered papers to the chronological list. If a monthly batch is large, add only high-confidence entries first and mark uncertain items for later review in an issue.

## Core Queries

Use combinations of:

```text
"embodied AI" safety
"embodied AI" risks attacks defenses
"vision-language-action" safety
"VLA" robot safety alignment
"robot foundation model" safety
"LLM-driven robot" safety
"embodied agent" safety
"physical AI" safety
"robotics" "AI safety"
"humanoid robot" cybersecurity
"mobile robot" "LLM" safety
"autonomous robot" assurance
"human-robot interaction" safety "foundation model"
"robot" prompt injection
"sensor spoofing" robot "AI"
"embodied AI" policy
"embodied AI" governance
"cyber physical" AI security robot
```

Jurisdiction-specific queries:

```text
[country or region] "physical AI"
[country or region] "embodied AI"
[country or region] robotics safety AI
[country or region] autonomous robot public path
[country or region] robot testbed AI safety
[country or region] AI safety institute robotics
[country or region] securing AI systems robotics
[country or region] agentic AI framework physical AI
[country or region] autonomous vehicle AI safety
[country or region] healthcare robot AI safety
```

## Inclusion Criteria

Include a resource when it does at least one of the following:

- Describes hazards, attacks, failures or unsafe behavior in embodied AI.
- Proposes safety, alignment, control, monitoring, red-teaming or assurance methods for robots or physical-world agents.
- Covers robot foundation models, VLA models or embodied agents with safety implications.
- Provides benchmarks, datasets, evaluations or leaderboards relevant to safe deployment.
- Sets standards, governance, regulation or operational guidance for physical AI.
- Documents real-world deployment, incidents, sandboxing or testbed governance.
- Is relevant to policy, public-sector deployment, regulation or assurance in any jurisdiction.

## Exclusion Criteria

Exclude or de-prioritise:

- Generic robotics papers without safety, security or governance relevance.
- Generic LLM safety papers with no physical-world agency connection.
- Vendor announcements without technical detail, unless useful for tracking deployment trends.
- Duplicative blog summaries when the original paper or official source is available.
- Hype pieces that do not improve technical or policy understanding.

## Tagging

Suggested tags:

- `survey`
- `policy`
- `governance`
- `standards`
- `jurisdiction`
- `cybersecurity`
- `red-teaming`
- `vla`
- `robot-foundation-model`
- `humanoid`
- `mobile-robot`
- `autonomous-vehicle`
- `drone`
- `maritime`
- `healthcare`
- `public-safety`
- `human-robot-interaction`
- `safe-control`
- `safe-rl`
- `control-barrier-function`
- `runtime-assurance`
- `semantic-safety`
- `physical-attack`
- `benchmark`
- `dataset`
- `incident`
- `assurance`
