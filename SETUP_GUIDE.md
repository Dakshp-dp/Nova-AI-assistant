# NOVA beta 0.4.1 — setup guide

## 1. Install or update NOVA

Download **Nova-Setup.exe** from the [0.4.1 beta release](https://github.com/Dakshp-dp/Nova-AI-assistant/releases/tag/v0.4.1-public-beta.1). Run it, then launch NOVA. Existing Public editions can also use **About → Check for updates → Install & restart**. Personal editions are updated locally.

You need Windows x64; Windows 11 is the development test environment. Internet may be needed for WebView2, sign-in, speech-model downloads and remote AI services. The installer is not publisher-signed; do not disable security software to install it.

## 2. Connect an AI provider

In the first-run **Give me a brain** screen, or later under **Model**, choose an account/provider you have access to. Follow its sign-in or enter your own key. Wait for Connected, select a model, and test a short message. Each friend uses their own account; no creator account/key is supplied.

- **ChatGPT / Claude:** account eligibility and subscription access depend on the provider. An authentication error is not fixed by repeatedly starting sign-in. Read the error and confirm the account is eligible.
- **Groq:** choose **Free-tier AI → Set up Groq**, create your own key through Groq, select a model, then **Test & connect**. Usage quotas apply; paid API usage can incur charges. Suggested by **Soul**.
- **Custom API:** **Model → Custom providers → Add custom provider**. Enter a name, OpenAI-compatible Chat Completions base URL, key if required, and exact model ID. Set tool/image support accurately. Test & save makes a real short provider request, which may use credits.
- **Local Ollama:** run Ollama with your downloaded model and configure its local compatible endpoint/model. Local hosting can be keyless. Small models and low-memory PCs may struggle with tool selection or screen understanding.

## 3. Configure voice and actions

Voice is optional. In **Voice**, download the microphone recognition model, allow the microphone in Windows, and choose the available input/reply options. Spoken replies currently use your own Fish Audio account/API key. Test text chat before troubleshooting voice. Check your configured push-to-talk shortcut; default show/hide is **Ctrl + Shift + S**.

Enable NOVA's app-action setting if you want it to click/type or perform other supported actions. Destructive actions still ask for confirmation. Browser permissions do not remove NOVA's safety checks, Windows UAC, download warnings or protected-page restrictions.

## 4. Enable browser tasks once

1. Launch NOVA at least once after installing 0.4.1. It registers its native browser host for the current Windows user automatically. Administrator rights are not needed for this registration.
2. Download **Nova-Browser-Extension.zip** from the same release.
3. Extract it into a permanent folder, for example `%LOCALAPPDATA%\NovaBrowserExtension`. Keep the extracted files there.
4. In Chrome open `chrome://extensions`; in Edge open `edge://extensions`.
5. Enable **Developer mode**, choose **Load unpacked**, and select the folder containing `manifest.json`.
6. The extension is **NOVA Browser Tasks**, version **0.4.1**, ID **ccaahmefakinfnnacgbfgjalhiomehjo**. Pin it if helpful.
7. Click its icon → **Enable automatic tasks**. Approve the browser's one-time website-access prompt if you want automatic cross-site work.
8. Wait for **Ready**. If NOVA was restarted, the extension reconnects automatically; it may take a short time. Use its popup to check status.

Do not install a second copy of the old prototype. Existing prototype users should replace the files in their current unpacked extension folder with 0.4.1, then click Reload on the extensions page. If using a new folder, remove the old entry first and load the new one. The extension's ID stays the same. The old **Connect this tab** popup should be replaced by **Enable automatic tasks**.

Enable it in the browser you want NOVA to use. One browser-extension connection is supported per NOVA instance; pause the extension in the other browser if Chrome and Edge compete for the connection. Chrome's [optional-permission API](https://developer.chrome.com/docs/extensions/reference/api/permissions) requires the initial permission request to come from your click; NOVA cannot silently approve it for you.

## 5. Use it normally

Open the webpage you want to work with and ask NOVA. There is no Connect click for each tab. Try:

- “Search YouTube for a budget laptop review and open a suitable result.”
- “Use this page's search and open the result about controllers.”
- “What are the choices on this page?”

NOVA starts a browser task on the active tab. It can keep access after ordinary cross-site navigation and follow related tabs opened during its browser actions. It waits locally for relevant results rather than asking the model repeatedly about unchanged state. Windows accessibility and screenshots remain available when DOM control is unsuitable.

Reading stops when the request finishes or is cancelled. Selecting an unrelated tab interrupts the task. Use **Pause / stop task** in the extension to cancel access and pause automatic tasks until you enable them again. Chrome's optional host grant remains saved so enabling does not require per-tab permission; you can revoke site access or remove the extension at any time.

## 6. Downloads and installations

Downloading a file and installing/running an application are different steps. NOVA can inspect a specifically named Downloads file for presence, size stability, partial-file state and Windows signature status. Those facts do not prove a file is safe, prove browser completion, or show that it is installed.

The extension cannot operate Windows installer/UAC windows by itself. Native tools cover supported desktop actions, but the existing rule blocking launch of downloaded executables remains. NOVA must state when a manual launch or confirmation is needed instead of pretending installation finished. It must not bypass browser warnings, Windows security or UAC.

## Troubleshooting

| Symptom | What to check |
| --- | --- |
| Still shows “Connect this tab” | Replace old extension files with 0.4.1 and Reload the extension. |
| Popup says paused | Click Enable automatic tasks; approve the website prompt if it appears. |
| Waiting for NOVA | Launch/restart NOVA 0.4.1. The native transport reconnects automatically. Verify app and extension run as the same Windows user. |
| Chrome says native host not found | Run NOVA once after installation. If needed, reinstall the current app and reload the extension; do not paste tokens into browser settings. |
| Permission declined or revoked | Enable again and approve the optional website grant, or use native browser control instead. |
| Task stops after switching tabs | Unrelated tabs are deliberately not adopted. Ask a new request on the tab you want NOVA to use. |
| Site needs a real mouse/key event, uses canvas or unsupported frames | NOVA should switch to Windows/screenshot tools where allowed. |
| Login, password, payment or security page | Complete the protected step yourself; the automatic task must not bypass it. |
| Download exists but app is not running | Inspect the exact filename. A manual launch may still be required; do not equate downloaded with installed. |
| Voice does not work | First test text chat, then check microphone permission, local recognition-model download and reply-voice credentials separately. |

## Updates and support

NOVA's signed updater updates the Public app. The unpacked browser extension is updated separately by replacing its extracted files and pressing Reload; a GitHub release cannot silently update an unpacked extension through Chrome's store mechanism.

For support, include NOVA/extension versions, the task, any error wording, and whether the extension popup says Ready/Working/Paused. Share screenshots only after removing private content. Never share API keys, tokens or sign-in callback URLs. [Report an issue](https://github.com/Dakshp-dp/Nova-AI-assistant/issues).
