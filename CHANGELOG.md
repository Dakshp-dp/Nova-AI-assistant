# NOVA development and release history

Release dates below are verified against GitHub. Earlier local work is grouped by milestone; historical experiments are not all present in the current companion app.

## Beta 0.4.1 — 21 November 2026

- Automatic browser tasks after a one-time Chrome/Edge extension permission.
- Cross-site access and related task-opened tabs without per-tab reconnection.
- Page access ends on task completion/cancellation; Pause stops access. Unrelated tab switches interrupt the task.
- Compact page control maps, resolved link/image URLs, bound structured actions and local relevant-result waits.
- Same-tab extension navigation and native Windows fallback; screenshot tools retained.
- Structured download inspection with file stability/partial status and Windows signature lookup. Downloads are not treated as installations; manual executable-launch handoffs remain.
- Current-user native-host registration included in the Windows app.
- Updated installer, corresponding source, separate unpacked extension ZIP and complete setup guide.

## Browser-control research — 20–21 November 2026

- First active-tab extension prototype integrated with the existing sidecar tool runner.
- Local Search → delayed results → matching link test, including unrelated page updates that do not trigger model work.
- Real model/native comparison on the small fixture; 3 versus 6 model calls in the measured task. No general performance guarantee.
- Repairs for same-tab routing, misleading loading errors, stale elements/documents, cancellation, cross-site handoffs and download checks.
- The manual Connect-this-tab prototype was replaced by task-scoped automatic access in 0.4.1.

## Public beta 0.1.35 — 18 November 2026

- Guided Groq setup on Model and the first-run Give me a brain screen.
- Own-key setup using encrypted provider storage and test-before-save.
- Provider/account isolation and quota/failure handling.
- Groq suggestion credited to Soul. Usage limits apply; live combinations vary.

## Public beta 0.1.34 — 11 November 2026

- Custom OpenAI-compatible provider profiles: name, base URL, exact model ID and key.
- Test & save, edit, switch and remove; multiple separate profiles.
- Keyless local Ollama support where configured.
- Tool/image/context capability settings and Windows-encrypted key storage.

## Public beta 0.1.33 — 11 November 2026

- First published public beta in this repository.
- Public/Personal edition separation and a shareable Windows installer.
- Signed update feed, startup/periodic checks, manual checks and Install & restart.
- Signature verification, retry/error states, active-task installation guard, source archive and checksums.

## Personal companion phase — 10 November 2026

- NOVA branding, creator credit and the geometric transparent logo/icon pipeline.
- Modern Graphite dashboard and a matching guided first-run experience, replacing the retro styling.
- Smooth Orb with cursor gaze, blinking, expressions, voice-reactive glow, wandering and idle hiding.
- Orb/Anime Girl appearance choices and preview/renderer fixes; other characters retired from the UI.
- AI account registration/reconnection fixes and clearer callback status without changing authentication checks.
- Voice recognition/reply repairs, more flexible command routing, screen viewing and Windows mouse/keyboard actions.
- Drawing and marking improvements, capture-visible overlays and tab-cleanup work through natural-language tasks.
- Existing third-party license and copyright notices retained.

## Earlier local prototypes — before the public companion releases

- Corner launcher for frequently used apps/websites, study music and everyday shortcuts.
- Compact translucent/frosted UI, color/appearance customization and smoother panel/event transitions.
- Experiments with timers, local calendar/time planning, multiple notes and password-lock ideas.
- Startup/search integration, persistent screen-time experiments and switching between two local users.
- Early app-closing/game-mode experiments were paused or changed as the app evolved.
- Local-model benchmarking and exploration of voice/AI-driven PC actions led into the later companion architecture.

These entries record the project's progression, not a current feature checklist. See the current README and setup guide for what the distributed beta supports.
