# ChatOSS

**The fastest, most private way to run AI on your Mac.**

ChatOSS is a blazing-fast desktop app for chatting with the best local and cloud models — with **Kanban boards and a full coding agent built right in**. Your data never leaves your machine unless you choose a cloud model. No accounts, no tracking, no middleman reading your conversations.

---

## Why ChatOSS

- **🚀 Three apps in one.** Chat, Kanban, and a real agentic Code workspace — terminal, file tree, diff editor, and an AI agent that actually edits your project. Stop juggling five tabs.
- **🔒 Truly private.** Everything runs locally against your own Ollama. Your prompts, your code, your boards — yours alone.
- **🧠 Bring your own models.** Run any model you like, local or cloud. No per-message tax, no surprise metering.
- **⚡ Built for speed.** A native, minimal UI that gets out of your way. No bloat, no waiting on a web page to load.

---

## Get ChatOSS

Download the latest version below and drag it to your Applications folder. That's it — no installer wizard, no sign-in wall.

👉 **[Download the latest release →](https://github.com/pagecow/chat-oss-releases/releases/latest)**

---

## Stay up to date

ChatOSS checks for new versions automatically and shows an **Update** button the moment one's ready. One click, grab the new build, and you're on the latest.

---

## What's new

See the full changelog for each release on the [releases page](https://github.com/pagecow/chat-oss-releases/releases).

---

<!--
  Everything below is for maintainers and the app's auto-updater — not part of
  the marketing page. The manifest powers the in-app "Update" check; the
  publishing notes are for whoever cuts a new release.
-->

## `latest.json` (auto-updater manifest)

The app fetches this on launch to decide whether an update is available:

```json
{
  "version": "0.3.6",
  "downloadUrl": "https://github.com/pagecow/chat-oss-releases/releases/latest",
  "releaseNotesUrl": "https://github.com/pagecow/chat-oss-releases/releases/tag/v0.3.6",
  "publishedAt": "2025-01-01T00:00:00Z"
}
```

- `version` — latest released version (semver, no leading `v`).
- `downloadUrl` — the release page; the app opens it in the system browser.
- `releaseNotesUrl` — the specific release's notes.

## Publishing a release (maintainer)

Releases are published **automatically** by the GitHub Action
(`.github/workflows/publish-releases.yml`) in the source repo: the moment a
release is **published** there, it is mirrored here (assets + `latest.json`).

That cross-repo write needs a PAT with `contents:write` + `releases:write` on
this repo, stored as the secret **`RELEASES_REPO_TOKEN`** in the source
(private) repo's Settings → Secrets and variables → Actions. The default
`GITHUB_TOKEN` is scoped to the source repo and cannot write here.
