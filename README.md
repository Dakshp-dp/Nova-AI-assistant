# NOVA

**A little presence. A lot of possibility.**

NOVA is a Windows AI desktop companion created and customized by **Daksh**. Chat, use voice commands, open apps and websites, and get help with what's on your screen—all from a small animated companion.

## Download

### [Download NOVA for Windows](https://github.com/Dakshp-dp/Nova-AI-assistant/releases/tag/v0.1.34-public-beta.1)

Choose **Nova-Setup.exe** under the release's **Assets**. Send that installer to a friend or share the release link; the source archive is available separately.

**Public beta · Windows 11 · x64**

This is an initial test build without a Windows publisher certificate. Windows may show an unknown-publisher or reputation warning. Clean-PC installation and live AI-provider sign-in still need testing. **Signed in-app updates are enabled for the Public edition.**

## Meet your desktop companion

- **Choose your look.** Pick Orb or Anime Girl and adjust the companion's size. Orb watches your pointer, wanders, and hides after about 15 seconds without interaction.
- **Talk naturally.** Type a message or configure microphone input and spoken replies.
- **Bring your own provider.** Save custom OpenAI-compatible API connections using a base URL, API key and exact model ID. Test, switch, edit and remove profiles from Model settings or setup. Local Ollama can connect without a key.
- **Do everyday tasks.** Ask NOVA to open apps and websites and help with routine PC actions.
- **Work with your screen.** Ask about visible content or request supported mouse and keyboard actions.
- **Point things out.** Use screen marking and drawing while getting help.
- **Keep things simple.** A charcoal dashboard, mint accents, and guided setup.

Capabilities depend on your connected provider, chosen model, account access, and configuration.

## Get started

1. Download and run **Nova-Setup.exe** from the release assets.
2. Follow the setup guide and choose your companion.
3. Connect your own supported AI account or enter your own API key.
4. Configure microphone recognition and spoken replies if you want voice.
5. Open NOVA through its tray icon or configured shortcut. The default shortcut is **Ctrl + Shift + S**.

Internet access may be required for Microsoft WebView2, speech-model downloads, and AI services.

## AI, voice, and your data

Setup offers ChatGPT, Claude, and API-key connection options. Each user connects their own accounts. Provider eligibility, subscription requirements, usage limits, and API charges depend on the provider; showing a connection option does not guarantee that every account can use it.

For another OpenAI-compatible service, open **Model → Custom providers → Add custom provider** and enter its name, base URL, API key and model ID. Custom keys use Windows-encrypted storage. Advanced options declare model support for tool calling and screen images, and its context limit. The connection test makes a short API request, which can use credits. APIs with different protocols or authentication formats need a dedicated integration.

Microphone recognition uses a separately downloaded local speech model. Spoken replies currently require a **Fish Audio account and API key**.

Messages and screen content used for a task may be sent to the AI provider you connect. Daksh's personal credentials, conversations, and settings are not included in the Public installer.

## Editions and updates

The shared installer displays **Public edition**. Daksh's existing local installation remains **Personal edition**.

Public editions check NOVA's own update feed automatically after startup and every six hours. When a newer version is ready, open **About → Install & restart** or use the tray update item. You can also choose **Check for updates** manually. NOVA verifies the update's signature before installation and preserves your account data and settings. Checks need an internet connection and NOVA running; updates do not force a restart while you work.

The Personal edition stays locally managed. Installers also remain available from [Releases](https://github.com/Dakshp-dp/Nova-AI-assistant/releases).

## Feedback

[Report a bug or suggest a feature](https://github.com/Dakshp-dp/Nova-AI-assistant/issues). Include your NOVA version, what you tried, and what happened. Remove private messages, credentials, and account details from screenshots and logs.

## Source and licenses

The release includes **Nova-Source.zip**, containing the corresponding app source, build instructions, original license, and third-party notices. **SHA256SUMS.txt** contains checksums for the installer and source archive; **READ-ME-FIRST.txt** explains this test build.

NOVA includes adapted upstream and third-party components. Their original license and copyright notices remain applicable. See [LICENSE](LICENSE) and [third-party notices](THIRD_PARTY_NOTICES.md).
