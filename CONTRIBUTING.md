# Contributing

Chat-RefinedTPP is developed and maintained by Haoru Song (宋昊儒). Contributions to the public website, documentation and issue reports are welcome.

## Scope

The public repository currently contains the static website and demonstration video. Keep proposals aligned with the files and features available here. Discuss substantial additions in an issue before implementation.

Describe reproducible bugs using the bug report form. Use the feature request form for suggestions, documentation improvements and accessibility concerns. Chinese and English reports are welcome.

Use synthetic data in examples. Remove API keys, passwords, personal identifiers, unpublished research data and private file paths from screenshots, logs and attachments. Follow [SECURITY.md](SECURITY.md) for suspected vulnerabilities.

## Change workflow

1. Create a focused branch from the latest `main`, such as `website/demo-video` or `docs/quick-start`. External contributors can use a fork.
2. Explain the change and its acceptance criteria in a pull request. Use the PR template and include the relevant verification evidence.
3. Check changed links and assets. For interactive changes, verify the normal flow, keyboard access and a narrow-screen layout. Video changes should include loading, playback, seeking and pause on dialog close.
4. Wait for the Cloudflare Pages preview deployment to succeed when the integration runs, then inspect the preview. Record any checks that could not be completed.
5. Request a review with `@codex review` if an automatic review has not started. Wait for completion on the latest changes and address findings. After further edits, request another review when needed.
6. Merge only after verification, AI review completion and explicit maintainer authorization.

A bot's summary comment can record an AI review without providing a formal GitHub Approve decision. Follow any additional branch protection requirements shown on the PR.

Keep changes small enough to inspect. Preserve the project's developer attribution and describe software versions accurately. Mark illustrative statistics clearly and activate downloads or subscriptions only when their backing services are ready.

## Licensing

Check the repository's licensing status before proposing reuse or redistribution of its assets. Do not add a project-wide license, replace third-party notices, or change the licensing of media and branding without an explicit maintainer decision.

## Conduct

Follow the [code of conduct](CODE_OF_CONDUCT.md) in issues, reviews and other project interactions.
