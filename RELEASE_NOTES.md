# NOVA beta 0.4.1

Browser control now starts from your request, with a one-time extension setup instead of connecting each tab.

- Automatic task start from idle; no page reads while the extension is simply Ready.
- Cross-site access and related tabs opened during NOVA browser actions stay in the task.
- Local waiting for navigation/results, compact control maps and real link destinations reduce screenshot/model overhead.
- Task end, cancellation and Pause stop page access. An unrelated tab interrupts the task instead of becoming a silent new target.
- Same-tab native fallback when the extension is unavailable; Windows/screenshot tools remain available.
- Structured inspection of downloaded files without launching them or mistaking a download for an installation.
- Automatic current-user native-host registration in the Windows app.

## Install / upgrade

1. Install **Nova-Setup.exe**, or update the Public app through About.
2. Extract **Nova-Browser-Extension.zip** to a permanent folder. Load it unpacked in Chrome/Edge; existing users replace the old extension files and click Reload.
3. Launch NOVA, then open the extension → **Enable automatic tasks** → approve its one-time website-access permission.
4. Ask NOVA to work in your current browser tab. No per-tab Connect step is needed.

Read **SETUP_GUIDE.md** for provider, custom API, Groq, Ollama, voice, browser and troubleshooting instructions. Every user supplies their own provider/voice accounts or keys. Groq's option was suggested by Soul; quotas apply.

## Important beta limits

Website access is an optional, persistent browser permission; NOVA's controller limits actual reads to active tasks. Authentication/security pages and sensitive fields remain protected. Same-window tabs opened during browser actions are supported; arbitrary unrelated tabs and some popups/frames/canvas controls may need native tools or a new user request. Launching downloaded EXEs remains a manual handoff. The unpacked extension must be updated/reloaded separately from the app updater.

This remains an unsigned Windows publisher build. The signed in-app update mechanism is a separate integrity check. Automated local tests passed for task start/end, related tabs, cross-site navigation, cancellation, Pause, stale controls, delayed results, irrelevant updates and native fallback; clean-PC installation and arbitrary real-site/provider combinations are not all verified. Previous development fixture timings are not a general speed guarantee.
