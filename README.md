# ChatOSS Releases

Public release channel for the ChatOSS desktop app. This repo holds the
latest version manifest (`latest.json`) and downloadable installers attached
to each GitHub Release.

The source code lives in a **private** repo; this public repo is the channel
installed copies of ChatOSS poll for newer versions (`latest.json`) and
download from (Release assets).

## `latest.json`

```json
{
  "version": "0.3.6",
  "downloadUrl": "https://github.com/pagecow/chat-oss-releases/releases/latest",
  "releaseNotesUrl": "https://github.com/pagecow/chat-oss-releases/releases/tag/v0.3.6",
  "publishedAt": "2025-01-01T00:00:00Z"
}
```

- `version` — latest released version (semver, no leading `v`).
- `downloadUrl` — the release page; the app opens it in the system browser so
  the user picks the installer for their platform.
- `releaseNotesUrl` — the specific release's notes.

## Publishing a release (maintainer)

Releases are published **automatically** by the GitHub Action
(`.github/workflows/publish-releases.yml`) in the source repo: the moment a
release is **published** there, it is mirrored here (assets + `latest.json`).

That cross-repo write needs a PAT with `contents:write` + `releases:write` on
this repo, stored as the secret **`RELEASES_REPO_TOKEN`** in the source
(private) repo's Settings → Secrets and variables → Actions. The default
`GITHUB_TOKEN` is scoped to the source repo and cannot write here.
