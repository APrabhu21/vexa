# Evidence for Vexa #1866 — bot speech (`POST`/`DELETE /bots/{platform}/{native_meeting_id}/speak`)

Everything the PR's acceptance table cites. Base `790551b` (`codex/v0.13.4`), head `a5d40aa`.
Deployment: Vexa Lite from a fresh clone, Windows 11 + WSL2 Ubuntu 24.04, docker.io 29.1.3, Kokoro-FastAPI
v0.2.4 (CPU) as the TTS, voice `af_bella`. API keys, meeting passcodes and emails are redacted or absent
(scanned before publishing).

| Folder | What | Image / commit |
|---|---|---|
| `speak-validation.log` | Every protocol command with its HTTP status and body, all runs in order | — |
| `meet-final/` | A10 Google Meet, full L2–L9 + probe; screenshots; `timing.md` timing table | `sha256:002bb8f5…` at 6c35846 |
| `meet-recorded/` | L1: a separate full Meet run, **screen recording with system audio** (`recording-google_meet.mp4`, 3:28) and a timestamp index (`README.md`) | `sha256:3fbd38c1…` at b2c1f7e |
| `zoom/` | A12 Zoom web client, L2–L7 + transcript | `sha256:3b8f4ad8…` at 7812aba |
| `teams/` | A11 Microsoft Teams web, L2–L7 + transcript; `…run1-mic-unverified.log` is the first attempt that found the Teams mic-label defect | `sha256:3fbd38c1…` at b2c1f7e |
| `tests/` | A1–A9 red at base / green at head (`base-*.log`, `head-*.log`, `A9-*.log`); full `node scripts/gates.mjs all` on Linux at base and head; meeting-api on Linux at a5d40aa | — |

Per platform folder: `speaker-bot.log` / `listener-bot.log` (the bots' own logs), `speaker-bot-stamped-*.log`
(the speaker's speak/mic lines stamped with host UTC every 0.2 s — the bot's log has no timestamps),
`listener-transcript*.json` (the listening bot's transcript; the bot's lines only), `lite.log`
(`docker logs vexa-lite`, with meeting-api's `bot_speak_queued` / `bot_speak_refused` /
`bot_speak_stop_sent` audit lines).
