# Search Method

This file documents the search and curation method for expanding Awesome Embodied AI (EAI) Safety.

## Curation Starting Point

The default search window starts in **January 2023**.

Rationale: 2023 is when embodied foundation models became a significant topic for safety work, with PaLM-E, RT-2 and Open X-Embodiment showing a clearer path from large multimodal models to robot reasoning and action. Older work is still included when it is foundational, especially robotics safety standards, human-robot interaction safety, autonomous vehicle safety, control theory, formal methods and cybersecurity.

## Source Types

- Academic search: arXiv, Semantic Scholar, Google Scholar, IEEE Xplore, ACM Digital Library, Science Robotics, IJRR, RSS, CoRL, ICRA, IROS, NeurIPS, ICML, CVPR, ACL and AAAI.
- Standards and guidance: ISO, IEC, IEEE, NIST, OECD, national AI safety institutes, sector regulators and public-sector guidance bodies.
- Repositories: GitHub topics and search for `embodied-ai`, `robotics-safety`, `vla`, `robot-foundation-model`, `humanoid-robot`, `autonomous-vehicles`, `robot-security`, `ai-assurance`.
- Benchmarks and datasets: project sites, Hugging Face, Papers with Code, Open X-Embodiment, embodied AI leaderboards and robot evaluation platforms.
- Deployment sources: government sandboxes, autonomous vehicle pilots, public robot testbeds, incident reports and credible technical blogs.

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
- `benchmark`
- `dataset`
- `incident`
- `assurance`
