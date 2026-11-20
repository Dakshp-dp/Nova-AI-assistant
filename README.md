# NOVA

**A little presence. A lot of possibility.**

NOVA is a Windows AI desktop companion created and customized by **Daksh (FanoF)**. Chat, talk, work with webpages, and get screen-aware help through a small animated companion.

## Beta 0.4.1

[Download NOVA beta 0.4.1](https://github.com/Dakshp-dp/Nova-AI-assistant/releases/tag/v0.4.1-public-beta.1) · [Complete setup guide](SETUP_GUIDE.md) · [Release notes](RELEASE_NOTES.md) · [Full history](CHANGELOG.md)

Choose **Nova-Setup.exe** to install the Windows x64 app. For browser tasks, also download **Nova-Browser-Extension.zip** and follow the one-time extension setup. Windows 11 is the tested target. This remains a beta; clean-PC installation and every provider combination have not been verified.

### What changed

- **Automatic browser tasks:** enable the Chrome/Edge extension once. When you ask NOVA to work in your browser, it starts from the active tab, continues across ordinary websites, and follows related tabs opened during its actions.
- **Less screenshot overhead:** compact page controls, real destination URLs and local result waiting let NOVA act without a model call for each click or unchanged page update. Existing Windows and screenshot tools remain the fallback.
- **Task-scoped access:** NOVA stops reading when the request finishes or is cancelled. Pause stops automatic browser access. Selecting an unrelated tab interrupts the task instead of silently retargeting it.
- **Better tab handling:** ordinary web navigation reuses the existing tab, including native fallback when the extension is unavailable. Arbitrary site popups are still subject to browser behavior.
- **Download inspection:** NOVA can check a named Downloads file, partial-file/size status and its Windows signature without running it. Downloaded does not mean installed; launching downloaded EXEs still requires a manual handoff under the existing safety rules.

The local Search → delayed results → matching result demo previously measured **3 model calls with the extension versus 6 with native tools**. Those small-fixture measurements are development evidence, not a speed guarantee for every website or model. The 0.4.1 regression checks also cover cross-site access, related tabs, task-end shutdown and Pause.

## What NOVA can do

- Type or voice chat, spoken replies when configured, and your choice of Orb or Anime Girl.
- Open apps and websites, work supported webpage controls, and use Windows mouse/keyboard tools where allowed.
- Read screen content when needed for your request; mark and explain supported screen areas.
- Save reminders and commitments through the companion.
- Connect supported AI accounts, Groq, local Ollama, or custom OpenAI-compatible API providers.

Capabilities depend on the model, provider, account access, Windows permissions and website. Canvas, restricted browser pages, some frames and trusted-input-only controls can require native tools or a user handoff. This is not unrestricted autonomous PC control.

## Setup

1. Install and launch **Nova-Setup.exe**.
2. Connect your own supported AI account or provider key. For Groq, use **Free-tier AI → Set up Groq**; quotas apply. The Groq option was suggested by **Soul**.
3. Configure voice if wanted. Microphone recognition downloads a local model; spoken replies currently need your own Fish Audio account/key.
4. Extract **Nova-Browser-Extension.zip** to a permanent folder. Load it through `chrome://extensions` or `edge://extensions` → Developer mode → Load unpacked.
5. Open the extension → **Enable automatic tasks** → approve Chrome/Edge's website-access prompt once. There is no per-tab Connect step after this.
6. Ask NOVA something such as “Search YouTube for a budget laptop review and open a suitable result.”

See the [complete setup and troubleshooting guide](SETUP_GUIDE.md), including upgrades from the old per-tab prototype. The default show/hide shortcut is **Ctrl + Shift + S**; your configured shortcuts may differ.

## Accounts and privacy

Every user supplies their own accounts/keys. Subscription eligibility, quotas and API billing are provider-specific; a connection option does not guarantee access for every account. Custom providers need an OpenAI-compatible Chat Completions endpoint, API key if required, and exact model ID. Tool calling and image support must match the chosen model. Ollama can be keyless when configured locally.

Automatic browser tasks require a one-time optional permission for ordinary HTTP/HTTPS websites. The permission remains enabled so you do not need a grant for each tab; NOVA's task controller stops page reads outside an active request. Password/payment/private fields and protected authentication/security pages remain excluded. Task messages and relevant page/screen content may be sent to your chosen AI provider. Pause or remove the extension to stop its access. Daksh's private credentials, settings and conversations are not included in the installer.

## Updates and editions

The shared installer is **Public edition**. It checks the signed NOVA update feed after startup and periodically while running. Use **About → Check for updates**, then **Install & restart** when offered. Updates restart NOVA, not your PC. Extension files loaded unpacked are separate: update their extracted files and reload the extension when the release guide calls for it.

Daksh's **Personal edition** stays locally managed. The Windows installer remains unsigned as a publisher package; the in-app updater signature is a separate integrity check, not a Windows publisher certificate.

## Feedback and source

[Report a bug](https://github.com/Dakshp-dp/Nova-AI-assistant/issues) with the version, task and actual result. Remove private messages and credentials from screenshots/logs.

Release assets include the installer, browser extension, corresponding **Nova-Source.zip**, setup guide and SHA256 checksums. Original license and third-party notices remain applicable: [LICENSE](LICENSE), [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
