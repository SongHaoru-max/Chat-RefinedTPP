# Third-party notices and production acknowledgements

This record distinguishes the platform integrations documented in the v0.5.0 source package from tools used to produce the public demonstration video. The public repository currently distributes the website and rendered MP4.

## Platform integrations

| Component | Recorded version | Upstream license | Source |
| --- | --- | --- | --- |
| @assistant-ui/react | 0.15.30 | MIT | https://github.com/assistant-ui/assistant-ui |
| @assistant-ui/react-markdown | 0.14.23 | MIT | https://github.com/assistant-ui/assistant-ui |
| thinking-orbs | 0.3.2 | MIT | https://github.com/Jakubantalik/thinking-orbs |
| LangGraph | 1.2.16 | MIT, as recorded in the source-package notices | https://github.com/langchain-ai/langgraph |

The source package retains the assistant-ui and thinking-orbs copyright and license texts under `frontend/third-party-licenses/`. Keep the notices with any distributions containing those components.

The source-package notices also acknowledge plotting design guidance from ChenLiu-1996/figures4papers. The plotting implementation is project-specific.

Source: https://github.com/ChenLiu-1996/figures4papers

This list records the integrations checked so far. A complete dependency and asset inventory is still pending before application-source and binary release.

## Demonstration production

The maintainer reports using onetake and video-shotcraft in the demonstration-production workflow.

### onetake

Identified upstream: https://github.com/feitangyuan/onetake

The upstream license checked on 7 November 2026 is PolyForm Noncommercial 1.0.0. It includes this required notice.

> Required Notice: Copyright (c) 2026 Patrick. onetake is free for noncommercial use only.

License: https://github.com/feitangyuan/onetake/blob/main/LICENSE

The terms describe permitted noncommercial, personal and organizational uses, including use by educational institutions and public research organizations. The upstream project offers a separate commercial license.

The exact production revision and any separate commercial authorization have not been recorded here. Preserve the applicable terms and required notice when distributing upstream software or portions of it. Permission to reuse the rendered film must be assessed using the applicable software, template and media terms.

### video-shotcraft

Upstream: https://github.com/Vincentwei1021/video-shotcraft

Code and documentation are published under Apache-2.0 in the upstream project.

License: https://github.com/Vincentwei1021/video-shotcraft/blob/main/LICENSE

The upstream documentation specifies separate terms for music, sound effects and Remotion. Record the exact production revision and any copied source or assets before distributing a video-source project. Preserve applicable license and NOTICE files for redistributed upstream code.

### Music

The supplied certificate identifies a Pixabay track by Tunetank. Full public credit details are in [the demo credits](assets/videos/CREDITS.md). The original certificate is retained separately and includes the downloader's account identifier.

## Project licensing

Upstream works retain their own terms. Original website code and repository documentation use the [MIT License](LICENSE). The [logo policy](LOGO_LICENSE.md) and [video policy](assets/videos/LICENSE.md) specify separate permission requirements. [LICENSING.md](LICENSING.md) defines the scope. The complete platform-source and dependency licensing review is deferred until publication of the analysis application.
