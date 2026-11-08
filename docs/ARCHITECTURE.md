# Platform architecture and workflows

Describes the supplied v0.5.0 and v0.4.2-fix3 packages. Application source is not published by these documents. Tables below describe implemented responsibilities; proposed illustration assets are listed in [FIGURES.md](FIGURES.md).

## Local application

| Layer | Implementation and responsibility |
| --- | --- |
| Interface | Built React frontend, assistant-ui conversation components and thinking-orbs visual elements; local task, input, parameter and result views |
| API and task state | FastAPI backend; local authentication, task/run ownership, saved drafts and SQLite persistence |
| Agent harness | Lightweight LangGraph turn orchestration and defined application tools for design, configuration and evidence access |
| Scientific execution | Fixed P2/G2 native pipeline stages; original scripts retained in the packages for provenance and regression comparison |
| Background work | Separate analysis, figure and report jobs, with state, limits, cancellation and interruption handling |
| Scientific records | Run-specific inputs/configuration, result tables, figures, metadata, logs and reports in the local data directory |
| Optional provider | User-configured online model for dialogue and interpretations; receives relevant context through the local backend |

LangGraph orchestrates dialogue turns; it is not the scientific calculation engine. Application state is persisted by the platform, not a LangGraph checkpointer. Local accounts enforce application-level ownership, not protection from the computer's administrator. Subprocess separation is not a complete container sandbox.

## Review before execution

Conversation helps capture design and suggest a supported branch. The user confirms task creation and uploads within that task. Proposals update a draft; they do not start analysis. Saved files, parameters and design are preflight-checked and reviewed before a confirmation permits execution. A changed draft must not redefine the parameters of a historical run.

Tools and API handlers enforce supported operations and ownership. The model has no arbitrary Python, shell, SQL or unrestricted filesystem tool. Statistical method selection follows the fixed scientific program and its configured rules.

## Input contracts

| Branch | Inputs | Important mapping constraint |
| --- | --- | --- |
| P2 | Protein reporter CSV | Explicit treatment/Vehicle mapping |
| G2 | Protein reporter CSV, enriched peptide reporter CSV and matching UniProt FASTA | Separate protein/peptide mapping; exactly one protein sample named `control` |

The supported reporter layout uses `Sample N` / TMT126–131 fields. Both branches require three matched biological replicate pairs, 129/126, 130/127 and 131/128. The design, not channel labels alone, establishes biological replication. The application generates PQE and Site Group intermediate tables.

## P2 stages

| Stage | Scientific operation |
| --- | --- |
| 1 | PQE construction and completeness QC |
| 2 | PQE Rm calculation and Vehicle-anchored panel normalization |
| 3 | Raw-Rm biological-replicate CV QC |
| 4 | Treatment-wise mean ΔRm population normality assessment |
| 5 | Statistical significance analysis |
| 6 | Run metadata and completion summary |

## G2 stages

| Stage | Scientific operation |
| --- | --- |
| 1 | Protein PQE QC |
| 2 | PQE Rm calculation and replicate-median normalization |
| 3 | N-glycopeptide evidence collapse and sequence/site mapping |
| 4 | Site Group aggregation, PQE-reference resolution and completeness QC |
| 5 | Resolve fully quantified Site Groups to unique complete control PQE references |
| 6 | Raw Rm CV QC, normalized Rm and mean ΔRm using matched PQEs |
| 7 | Joint Site Group / matched-PQE raw-Rm CV filtering |
| 8 | Mean ΔRm population distribution and normality assessment |
| 9 | Statistical significance analysis |
| 10 | Save run metadata |

These stage descriptions follow the supplied native stage definitions. Do not replace them with a generic eight-branch diagram or imply that CV filtering is performed on ΔRm instead of the specified raw-Rm quantities.

## Evidence and interpretation

Reports reference a selected run's frozen data and configuration. Factual reports remain available without a model. Model interpretations may be generated separately and require scientific review; citations establish source references, not automatic validation of every claim.

v0.5.0 adds report snapshots, selected-run model history, task decision excerpts and compatible-run set comparisons. Candidate glycosites and PQE members remain explicit; a reference match does not resolve every localization ambiguity. Snapshot history is not a separate backup of all scientific inputs. See [version differences](VERSIONS.md).
