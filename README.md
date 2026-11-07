# Chat-RefinedTPP

A task-specific agent harness for TMT-based Refined-TPP research.

Developed and maintained by **Haoru Song (宋昊儒)**.

[Visit the website](https://chat-refinedtpp.com/) · [Watch the demo](https://chat-refinedtpp.com/#demo) · [Report a bug](https://github.com/SongHaoru-max/Chat-RefinedTPP/issues/new/choose)

## Project

Chat-RefinedTPP provides a local workspace for experimental design, quality control, analysis and evidence-linked interpretation of TMT-based Refined-TPP data. The Agent assists with setup and interpretation. Researchers review the analysis plan before the fixed scientific pipeline runs.

The platform includes protein-level P2 analysis and N-glycosite Site Group G2 analysis.

## Public repository

This repository currently contains the project website and its 89-second promotional video. The analysis application source and installation packages have not been published here. Download availability and documentation will be announced on the website.

| Location | Content |
| --- | --- |
| `index.html` | Static project website |
| `assets/videos/` | Published demonstration video |
| `.github/ISSUE_TEMPLATE/` | Bug and feature request forms |
| `.github/PULL_REQUEST_TEMPLATE.md` | Change and review checklist |

Scientific analysis runs in the local application. When an external model provider is enabled, the dialogue and necessary context may be sent to that provider.

## Website development

The website uses plain HTML, CSS and JavaScript. To preview it locally with Python installed, run the following from the repository root and open `http://localhost:8080`.

```sh
python -m http.server 8080
```

Cloudflare Pages deploys the `main` branch. Proposed changes use a separate branch and a pull request. Before merging, wait for Codex bot to finish reviewing the latest changes, address its findings and verify the affected behavior. An AI review comment is distinct from a GitHub Approve decision. The maintainer authorizes the merge.

## Research and citation

The website provides the original Refined-TPP method reference and current software citation guidance. Platform publication details will be added when public. For analyses, record the exact software version and cite the method and platform as applicable.

## Community

- [Contributing](CONTRIBUTING.md)
- [Code of conduct](CODE_OF_CONDUCT.md)
- [Security reporting](SECURITY.md)
- [Accessibility](ACCESSIBILITY.md)

Public issues and pull requests are visible to everyone. Share small synthetic examples and redacted diagnostics when reporting problems.

## Licensing

Original website code and repository documentation are licensed under [MIT](LICENSE). The [logo](LOGO_LICENSE.md) and [video](assets/videos/LICENSE.md) have separate permission policies. Third-party material retains its applicable upstream terms. See [LICENSING.md](LICENSING.md) for scope and permission requests.

See [third-party notices](THIRD_PARTY_NOTICES.md) for platform and production-tool acknowledgements and [video credits](assets/videos/CREDITS.md) for the published demo's music source. These notices preserve the separate upstream terms.
