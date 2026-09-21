# Codex computer use examples

*Unofficial community examples for Codex computer use. Not affiliated with OpenAI. All trademarks belong to their owners.*

Codex computer use is a feature of the Codex desktop app, not an API, so these examples are the artifacts you actually write when using it: prompts that trigger the right surface, an AGENTS.md snippet that tells Codex how to choose between Computer Use, the Chrome extension and plugins, and a checklist for the trust boundary. The prompts marked as sourced come from Jason Liu's write-up; the rest are my own, following the same pattern.

> If the task is "build me a page": [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=codex-computer-use-examples&utm_content=readme-top&utm_term=tier-r).

## Files

| Path | What it shows |
|---|---|
| `examples/prompts.md` | Prompt templates for @Computer tasks: native apps, polling, last-mile steps, iOS flows |
| `examples/AGENTS.md` | A snippet for your repository's AGENTS.md so Codex picks the right surface on its own |
| `examples/safety-checklist.md` | The pre-flight checklist before granting an app to Computer Use |

## Setup

1. Install the Codex desktop app (macOS or Windows).
2. In Codex open Settings, then Computer Use, then click Install.
3. Optionally install the official Codex Chrome extension for browser work.
4. Approve only the apps a task needs.

There are no environment variables or API keys; everything runs inside the app. The official reference is the [Computer Use page](https://developers.openai.com/codex/app/computer-use) in the Codex developer docs.

## examples/prompts.md

Each prompt names the surface explicitly with @Computer, states the one app or flow involved, and includes a boundary sentence ("do not change my account settings"). Two prompts are quoted from Liu's article: the Spotify Discover Weekly one and the iPhone Mirroring bug reproduction. The others follow the same shape for a polling task, a settings change and a last-mile upload. Copy one, replace the app name and the boundary, and paste it into a Codex thread.

## examples/AGENTS.md

Liu's article says the goal is to add guidance to AGENTS.md so Codex can choose the right surface itself. The snippet encodes that ordering: structured plugin or MCP first, the Chrome extension for multi-tab and authenticated browser work, Computer Use only for native apps, GUI-only flows, system settings or a missing action in an otherwise useful integration. It also tells the agent to stop and ask before anything financial, credential-related or security-related. Paste it into the AGENTS.md at the root of the repository you run Codex in and adjust the app list.

## examples/safety-checklist.md

A short checklist distilled from the source's warning that Computer Use is the broadest trust boundary of the three surfaces: one app or flow per task, sensitive apps closed, permission prompts reviewed, and a human present for payment, account, privacy and system-security changes. Run through it before approving a new app.

## When to use Begin.sh instead

Computer use is the right tool when the app has no other door: a native desktop app, an iOS simulator, a settings pane. It is the wrong tool when the outcome is a website or a mobile prototype and you are only automating a builder's UI to get there. For that, [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=codex-computer-use-examples&utm_content=readme-top&utm_term=tier-r). Write the prompt or paste a URL to clone, download the zip, and host it yourself; there is no hosting, backend or auth to set up, and no agent clicking through anything.
