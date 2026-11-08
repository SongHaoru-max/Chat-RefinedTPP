# Figure and screenshot preparation

This is an asset brief, not a list of available image files. README image links will be added after the maintainer supplies or approves the images. Preferred delivery: an editable SVG/PDF plus a readable PNG; screenshots can be PNG. Use English labels for the main public README and identify the represented software version.

| Priority | Requested asset | Required content | Proposed future filename |
| --- | --- | --- | --- |
| 1 | Platform architecture | Local React workspace, FastAPI backend, Agent/LangGraph tools, explicit run review, fixed P2/G2 execution, local evidence storage and optional external provider | `docs/assets/platform-architecture.png` |
| 1 | Scientific pipeline overview | Separate P2 and G2 paths, required inputs, raw-Rm CV QC, ΔRm/statistics and result units; retain G2 protein-reference matching and ambiguity | `docs/assets/p2-g2-workflows.png` |
| 2 | Workspace screenshot | Actual accepted v0.5.0 task/input/review interface with safe sample data | `docs/assets/workspace-v0.5.0.png` |
| 2 | Results/report screenshot | Actual QC/results and report history or source-linked evidence view | `docs/assets/results-v0.5.0.png` |
| 3 | Standalone project logo | Approved brand artwork export; existing separate logo policy applies | `docs/assets/chat-refinedtpp-logo.png` |
| Later | Example-result panel | Approved dataset and exact version/configuration; label synthetic data when used | Determine with the example dataset |

## Content checks

- Distinguish the public information website from the local analysis application.
- Label the optional network boundary to the model provider; do not show raw data always remaining local when selected evidence can be transmitted.
- Show human confirmation before scientific execution. Do not imply autonomous statistical-method selection or arbitrary code execution.
- Show only P2/G2 as implemented. A broader eight-branch roadmap needs an explicit future-design label and should be separate from the current architecture.
- Use PQE and Site Group as the corresponding result units. Candidate sites are not all uniquely localized sites.
- Remove API keys, account identifiers, private paths and unpublished research values from screenshots. Confirm permission for any third-party diagrams.
- Include captions/alt text and sufficient contrast. Keep small labels readable at README width.

The actual stage definitions to use when preparing the pipeline image are in [ARCHITECTURE.md](ARCHITECTURE.md). Earlier Demo screenshots/video should be labelled **v0.4.2-fix3**, rather than presented as exact v0.5.0 captures.
