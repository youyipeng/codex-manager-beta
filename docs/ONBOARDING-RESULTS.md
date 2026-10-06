# Measured onboarding results — October 6, 2026

Runtime 0.1.0-beta, onboarding kit revision 1. Final ZIP verified by CRC and content hashes; commercial Manager runtime and existing installer/control code are unchanged.

| Measurement | Old clean-config test | Revised first test | Final ZIP clean-config test |
|---|---:|---:|---:|
| Installation, seconds | 42.261 | 48.058 | 39.356 |
| Real demo, seconds | 391.068 | 367.655 | 372.226 |
| Install through first checked result, seconds | 433.329 | 416.452 | 412.348 |
| Known demo outcome | 16/16, accept | 16/16, accept | 16/16, accept |

Final ZIP extraction plus launcher elapsed: 414.953 seconds. The original baseline excluded extraction, so this number is reported separately. Final installation and first success timers include actual model/check/review/evidence retrieval; they exclude download, user interaction, prerequisite setup and sign-in. The launcher starts with automated test consent immediately; a stranger's hesitation/actions are not observed.

**The five-minute goal was not met.** The final run differed from the old baseline by 20.981 seconds; a few same-machine samples cannot establish a reliable speedup. Model planning, implementation and review dominate elapsed time. No core capability, model policy or acceptance gate was changed to reduce it.

The old four grouped stages were extract, run installer, select plugin in new chat, send task. The new **launcher-only** route is extract, START, approve the displayed known-demo task: three stages, automatically handling dependency detection, registration, sample authorization, polling and checked-result display. This is an alternative MCP entry outside ChatGPT, not proof of a reduced complete ChatGPT conversational journey. Opening a new Work chat, selecting the plugin if needed and sending the task are still separate actions; the full conversational path may still take four or more stages. Actual stranger step count remains unmeasured.

Clean validation uses fresh HOME/USERPROFILE/APPDATA/LOCALAPPDATA/TEMP/TMP/CODEX_HOME and Manager/repo paths on the existing Windows 11 computer. It shares the Windows SID, installed dependencies, Desktop and existing signed-in Codex authentication home, without reading/copying credentials. It is not a fresh machine/user/VM/account or a new ChatGPT UI end-to-end recording. The final task completed in one iteration, 16/16 checks, separate review accept, intact artifacts and unchanged original repo.

The local feedback collector is ready, but customer install time, real task success, time saved, friction, feature priorities, continue-use intent and prices remain unknown until a customer tries it. No outreach, X/Reddit/HN posting or payment work was added.
