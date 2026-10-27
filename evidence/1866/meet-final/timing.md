# #1866 live run 3 — Google Meet, Vexa Lite at 6c35846 (image sha256:002bb8f5f075…), Kokoro-FastAPI v0.2.4 CPU, voice af_bella

Clocks: POST / DELETE from the caller's shell; bot lines stamped by a 0.2 s poller of the bot's log
(speaker-bot-stamped-final.log); "first word" is the listener bot's transcript segment start (no screen
recording was made — L1 not provided), so it is approximate.

| step | request_id | POST (UTC) | bot `started` | first word (listener) | end | end kind |
|---|---|---|---|---|---|---|
| L4 | 8a89b6f6f990… | 19:24:52.738 | 19:24:52.847 | 19:24:57.511 (+4.8 s) | 19:25:01.797 | done ms=8377 |
| L6 (stop after 3 s) | 58964830cbce… | ~19:25:29.9 | 19:25:30.173 | none — stop landed before the first audio | 19:25:33.104 | stopped (DELETE 19:25:32.957, +0.15 s) |
| L7 #1 | 022a19649b2a… | 19:29:01.093 | 19:29:01.232 | 19:29:05.070 (+4.0 s) | 19:29:05.245 | done |
| L7 #2 | c14744c6ce2a… | 19:29:01.124 | 19:29:05.768 | 19:29:10.964 | 19:29:11.318 | done |
| L7 #3 | 0648b405211b… | 19:29:01.150 | 19:29:11.600 | 19:29:16.846 | 19:29:17.389 | done |
| L7 #4 | bb8c7e3f9ddb… | 19:29:01.176 | 19:29:17.648 | 19:29:21.205 | 19:29:21.649 | done |
| L7 #5 | f2efdbec77fe… | 19:29:01.200 | — | — | 19:29:01.232 | dropped queue_full |
| L7 #6 | b6abd3d8743d… | 19:29:01.223 | — | — | 19:29:01.509 | dropped queue_full |
| L7 #7 | — | 19:29:01.248 | — | — | — | 429, Retry-After: 59 |
| L6 retry (8 s) | 6d3dd832abca… | 19:31:01.0 | 19:31:01.122 | none | 19:31:01.652 | failed mic_unverified (finding → d97832c) |
| check | accdbcb296a9… | 19:31:44.5 | 19:31:44.615 | 19:31:48.669 | 19:31:49.061 | done |
| L6 (stop after 8 s) | 13afa532a416… | 19:31:58.5 | 19:31:58.607 | 19:32:02.758 (+4.2 s) | 19:32:06.699 | stopped (DELETE 19:32:06.614, +0.09 s) |

Gap POST→first word ≈ 4–5 s is Kokoro CPU synthesis of the first chunk; the bot adds ~0.1 s.
