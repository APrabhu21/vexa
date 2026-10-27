# #1866 L1 — recorded run, Google Meet, Vexa Lite at b2c1f7e

`recording-google_meet.mp4` — 3:28, H.264 + AAC system audio, the host's Chrome window
(meeting `vkv-ocpi-thk`), recorded by the host with Windows Snipping Tool. Recording t=0 ≈ 21:25:12 UTC.

| Recording | UTC | Step | Bot log / API |
|---|---|---|---|
| ~0:50 | 21:26:05 | L3 both bots active, speaker mic off | `L3-both-bots-speaker-mic-off.jpg` |
| ~1:16 | 21:26:28 | L4 "This is Vexa speaking…" heard | started 21:26:19.730 · done 21:26:33.010 · mic=off |
| — | 21:26:4x | L5 five refusals, nothing heard | 409 · 404 · 422 · 422 · 422 |
| ~1:49–1:51 | 21:27:01–03 | L6 paragraph starts, cut | DELETE 21:27:03.445 · stopped 21:27:03.646 · mic=off |
| ~2:52–3:11 | 21:28:04–23 | L7 "Number one" … "Number four" | 6×200 + 429 retry-after 59; 5–6 queue_full |
| ~3:15 | 21:28:40 | L9 both bots leave | `L9-bots-left.jpg` |

Audio level per 10 s (RMS, mono 8 kHz): speech at 70 s, 100–120 s and 170–190 s, matching L4, L6
and L7; silence between. Sound at 10–40 s precedes the bots' first line (Meet join chimes; not
attributed). Listener transcript: `listener-transcript.json`; stamped bot lines:
`speaker-bot-stamped-recorded.log`.
