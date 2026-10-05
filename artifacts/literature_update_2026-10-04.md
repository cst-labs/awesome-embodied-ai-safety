# Weekly Embodied AI Safety Literature Update — 2026-10-04

## Scope and method

- Window searched: 27 September–4 October 2026, with late-indexed safety papers from 25–26 September treated as surfaced this week.
- Followed `SEARCH_METHOD.md`: targeted arXiv searches, official lab/company release pages, official project sites and GitHub resources; deduplicated against `README.md` and prior automation memory.

## Added to README

### Papers / capability releases

- **Praxis-1** — [official Runway release](https://runway.com/research/introducing-praxis-1). A video-pretrained world-action model for robot control across embodiments. The primary announcement says partner testing is under way and public weight release is planned for coming months; the entry does not represent it as available/open.
- **FP2: Equipping Robotic Foundation Models with Force Control** — [arXiv:2609.37433](https://arxiv.org/abs/2609.37433), submitted 29 September; [official project](https://force-policy.github.io/fp2/). A real-robot, feedback-driven force-regulation layer for foundation policies in contact-rich tasks.
- **PlanGuard** — [arXiv:2609.32801](https://arxiv.org/abs/2609.32801), submitted 26 September. Adds whole-plan physical-risk checking and the MSP-Safe dataset. Included as a late-indexed discovery; its code/data are explicitly future releases.
- **ConflictVLA-Bench** — [arXiv:2609.31792](https://arxiv.org/abs/2609.31792), submitted 25 September. Its paired rollout protocol exposes continued action toward invalid objectives (“Failed Persistence”) across tested VLAs. Included as a late-indexed discovery.

### Resources

- **ConflictVLA-Bench** — [official GitHub project](https://github.com/EmbodiedAISurvey/ConflictVLA-Bench), listed under Benchmarks, Datasets and Evaluation because the paper links it as the source for experimental data and implementation details.

## Excluded / held

- **EmbodiRSI** (arXiv:2609.38905): useful robot-adaptation work, but incremental capability progress without a safety, assurance or material frontier-release angle.
- **Light-O1**: only a press-release discovery in this window; no primary technical report, model card or durable code/weights source verified.
- **SEMI Doc 7490**: potentially relevant AMR-in-semiconductor safety guideline, but its standards activity began 9 July, outside this weekly window; held for a future standards-focused review rather than added as a new development.
- No qualifying in-window, final policy or standards publication was verified.

## Review notes

- Runway dates Praxis-1 only to September, not a day, and says weights remain pending. Its capability announcement is material, but availability and independent evaluation should be rechecked after the public release.
- PlanGuard and ConflictVLA-Bench predate the window by one and two days respectively; they were added because they surfaced in the current week’s targeted search, not as in-window publications.

## Validation

- `git diff --check` passed.
- No duplicate arXiv URLs found in `README.md`.
