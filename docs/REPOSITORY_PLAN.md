# Repository structure and publication plan

**Planning document.** No application source, installation archive, real dataset or version tag is published by this documentation change. The current website remains at the repository root.

## Current public content

| Location | Current content |
| --- | --- |
| `README.md` | Platform introduction and current distribution status |
| `docs/` | Version notes, usage documentation, architecture and publication planning |
| `index.html` | Static project website deployed by Cloudflare Pages |
| `assets/videos/` | Promotional video, permission policy and credits |
| `.github/` | Issue forms and pull-request template |
| Root community and license files | Contribution, conduct, security, accessibility and scoped licensing |

## Target layout after source publication

The following paths are proposed future locations, not links to existing source. Keep the application's current root-level imports and launch assumptions intact rather than wrapping everything in another directory or duplicating a whole tree for each version.

| Proposed path | Purpose | Publication stage |
| --- | --- | --- |
| `README.md` | Main platform entry, supported versions and download links | Updated now |
| `docs/` | Usage, pipeline details, architecture and release notes | Documentation now; expand with source publication |
| `docs/assets/` | Approved architecture diagrams and redacted screenshots | After illustration review |
| `website/` | Website `index.html`, site-only assets and deployment notes | Separate migration before source publication |
| `backend/` | FastAPI service, Agent tools, state, jobs and reports | Withheld until source publication is authorized |
| `frontend/` | React source, package metadata and frontend build instructions | Withheld until source publication is authorized |
| `pipelines/native/p2/`, `pipelines/native/g2/` | Modular scientific stages | Withheld until source publication is authorized |
| `pipelines/original/` | Preserved reference scripts for provenance/regression | Withheld until source publication is authorized |
| `tools/`, `tests/` | Environment/maintenance utilities and meaningful regression tests | Withheld until source publication is authorized |
| Root setup/start/diagnostic/backup scripts and dependency files | Preserve the supplied application's root-relative entry points | Withheld until source publication is authorized |
| `examples/` | Small approved input examples, mapping, configuration and expected results | After dataset-specific approval |

## Version organization

Use version tags and releases for **v0.4.2-fix3** and **v0.5.0** when publication is authorized. The main source tree should follow the current version; the Demo stays reproducible from its own tag. Do not create parallel `v0.4.2/` and `v0.5.0/` source directories on `main`.

A future Demo tag must point to its actual Demo source tree, not a documentation-only commit on the current main branch. Prepare the historical source tree and its release record deliberately; retain the provided baseline and provenance. Any packaging changes need new checks and a clear record, not silent alteration of the historical package.

Do not rename v0.5.0 to v1.0.0 merely to match an old roadmap. Any later version change needs consistent package metadata, frontend version, manifest, documentation and a deliberate release decision.

## Publication sequence

1. **Documentation:** review this README, version roles, input contracts and repository plan; request Codex review and obtain maintainer merge authorization.
2. **Figures:** add approved architecture/pipeline illustrations and version-labelled screenshots. Keep pending assets out of README image links.
3. **Website isolation:** move only the current website and its assets into `website/` in a dedicated migration. Update site-relative links, license/credit references and the Cloudflare Pages build root/output configuration to publish only that directory. Verify preview, custom domains, video playback and production routes. Do this before adding application files.
4. **Publication audit:** confirm application licensing and dependency notices; inspect configuration examples, package contents, data and diagnostics for material not intended for publication. The current ZIPs include source, so uploading them is also a source publication decision.
5. **Source and version records:** import the approved source tree, preserve original pipeline provenance, run appropriate regression/build checks and create tags that identify the actual corresponding source. Publish application archives/checksums only when separately authorized.
6. **Availability:** synchronize README, version notes, website download controls and release records. An accepted version becomes publicly downloadable only after its actual asset exists and has been checked.

Until step 3 is complete, keep the current Cloudflare configuration and site paths unchanged. A root-directory static deployment must not be assumed to protect newly added application files.

## Examples and scientific records

For each future real example dataset, record its source, permission/publication status, branch, sample mapping, replicate design, expected input files, configuration, software version and expected QC/output summary. Give data its own explicit reuse terms; software licensing alone does not settle dataset permissions.

Small approved examples may be versioned under `examples/`; large datasets can use a suitable research data deposit with a stable identifier and checksums referenced by the example guide. Exclude live account databases, `.env`, API keys and private task/output directories. No real example is included at this stage.

## Release synchronization

Before a public application release, reconcile package-internal historical alpha/pending-acceptance wording with the maintainer's acceptance record, preserving history and documenting any changed package files. Confirm documentation, version metadata, environment requirements, known limitations and the actual distribution license agree. Do not expand the website's MIT scope through a README alone.
