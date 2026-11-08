# Contributing

Chat-RefinedTPP is developed and maintained by Haoru Song (宋昊儒). Contributions to the public website, documentation and issue reports are welcome.

## Scope

The public repository currently contains the static website, demonstration video and platform documentation. Documentation describes the accepted v0.5.0 and retained v0.4.2-fix3 Demo; application source and installation ZIPs are withheld. Both supplied ZIPs contain source, so do not upload them as a workaround for the source-publication boundary. Keep proposals aligned with the files and features available here. Discuss substantial additions in an issue before implementation.

Follow [version notes](docs/VERSIONS.md) and the [repository plan](docs/REPOSITORY_PLAN.md). Future platform source should preserve its existing backend/frontend/pipeline structure and use tags for versions. The website must be isolated into its own deployment directory before application files are added. This is a future migration, not a directory change in the current checkout.

Describe reproducible bugs using the bug report form. Use the feature request form for suggestions, documentation improvements and accessibility concerns. Chinese and English reports are welcome.

Use synthetic data in examples. Remove API keys, passwords, personal identifiers, unpublished research data and private file paths from screenshots, logs and attachments. Follow [SECURITY.md](SECURITY.md) for suspected vulnerabilities.

## Change workflow

1. Create a focused branch from the latest `main`, such as `website/demo-video` or `docs/quick-start`. External contributors can use a fork.
2. Explain the change and its acceptance criteria in a pull request. Use the PR template and include the relevant verification evidence.
3. Check changed links and assets. For platform documentation, check feature claims, input requirements, package commands, version labels and download availability against the relevant accepted package. Do not generalize P2/G2 into support for all eight draft branches. For interactive changes, verify the normal flow, keyboard access and a narrow-screen layout. Video changes should include loading, playback, seeking and pause on dialog close.
4. Wait for the Cloudflare Pages preview deployment to succeed when the integration runs, then inspect the preview. Record any checks that could not be completed.
5. Request a review with `@codex review` if an automatic review has not started. Wait for completion on the latest changes and address findings. After further edits, request another review when needed.
6. Merge only after verification, AI review completion and explicit maintainer authorization.

A bot's summary comment can record an AI review without providing a formal GitHub Approve decision. Follow any additional branch protection requirements shown on the PR.

Keep changes small enough to inspect. Preserve the project's developer attribution and describe software versions accurately. Mark illustrative statistics clearly and activate downloads or subscriptions only when their backing services are ready.

## Licensing

Follow [LICENSING.md](LICENSING.md) when proposing reuse or redistribution. Contributions to original website code and repository documentation are submitted under the [MIT License](LICENSE), unless separately agreed with the maintainer. Logo, video and third-party asset contributions need their own provenance and permissions. Obtain an explicit maintainer decision before changing licensing scope or third-party notices.

## Conduct

Follow the [code of conduct](CODE_OF_CONDUCT.md) in issues, reviews and other project interactions.
