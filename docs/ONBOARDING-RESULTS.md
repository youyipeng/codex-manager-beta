# Measured onboarding results — October 6, 2026

Runtime 0.1.0-beta; onboarding kit revision 2. The same final ZIP was used in both measured runs. The Manager core/runtime and frozen demo files are byte-for-byte unchanged. These are internal same-computer tests, not stranger usability measurements.

| Measurement | Round 1: dependencies present | Round 2: portable Node/Git download |
|---|---:|---:|
| ZIP extraction | 2.468 s | 2.562 s |
| Dependency preparation | 0.099 s | 52.280 s |
| Installation and registration | 41.419 s | 79.823 s |
| Real demo, checks and review | 58.285 s | 42.349 s |
| Extraction through first checked local result | **103.468 s (1:43)** | **179.000 s (2:59)** |
| Tests / independent review | 16/16 / accept | 16/16 / accept |
| Final-run failures | None | None |

The totals include launcher overhead. Both use fresh HOME, USERPROFILE, APPDATA, LOCALAPPDATA, TEMP/TMP, CODEX_HOME and Manager/repo directories. Background model work also uses the temporary user directories. Round 2 actually downloads checksum-verified official portable Node and MinGit; system dependencies are not used for those tools. The tests share the existing Windows SID, installed Desktop/native Codex CLI and signed-in authentication home without reading/copying credentials. They are not new Windows accounts, VMs or fully new computers. The two measured rounds ran consecutively on the same host; these samples do not establish reliability or typical performance.

**The local-launcher five-minute target was met in both tests. The complete download-to-ChatGPT journey remains unverified.** Initial ZIP download, Desktop setup/login, human reading/actions, security/protocol prompts and new-task ChatGPT interaction are excluded. Automated consent is used in the test harness. Manual actions are designed as two after extraction (open START, approve the first-run window); actual stranger click counts are unobserved. Download and extraction add at least two stages.

The previous launcher measurement was 412.348 seconds excluding extraction; the prior extraction-to-result measurement was 414.953 seconds. A separate native CLI probe observed five WebSocket retries before HTTPS fallback at 112.564 seconds. An installation-scoped HTTPS provider adapter removed that wait in the probe (7.138 seconds total versus 119.503 seconds). The unchanged Manager still performs planning, implementation, real checks and separate review with its existing signed-in account/default model and original tool restrictions. The concise launcher task has the same README requirements and frozen tests. These few observations do not isolate a statistically reliable speedup.

Installation and dependency preparation are now the largest measured setup costs. Setup detects paths, fills configuration, installs/registers owned MCP/plugin entries, creates and narrowly authorizes the supplied demo, submits one natural-language request, resumes the saved job and displays actual checks/review/patches. No original source is modified. The final task in each round completed in one iteration with intact artifact hashes.

The prepared Desktop link preloads a Beta plugin mention and the existing job. Sending the draft remains a user action; switching to Work may add one action. Plugin visibility/refresh after a cold host startup and a complete new-task Desktop workflow have not been tested. The local result page is browser-verified. [Visual guide](FIRST-STEPS.html). [Official launch-link behavior](https://learn.chatgpt.com/docs/app/commands#deep-links).

First installation failure invokes STATUS → REPAIR → STATUS once and produces a readable diagnosis. Development validation exposed and fixed Windows PowerShell JSON decoding of non-ASCII paths, dependence on a module unavailable in a temporary profile, and ownership handling of an interrupted registration. A later candidate also exposed ambiguous demo wording (implementation incorrectly waited for later check evidence) and an assumed review artifact that may be absent; the demo wording and terminal display were corrected without changing core acceptance gates. That pre-release failure is retained, not counted as a successful first run. Damaged packages, changed authorization and foreign registration ownership remain errors rather than being overwritten. A controlled one-time native plugin-registration failure was recovered automatically (status exit 1 → repair exit 0 → status exit 0). The subsequent real demo passed 16/16 but independent review escalated; it remained unsuccessful and its patch was not presented as accepted. Full controlled run: 101.359 seconds. No fixture is shipped in the kit.

The kit is ready for an assisted first real-user trial; the standard “a stranger reliably succeeds without guidance” has not yet been demonstrated. No cold outreach, payment development or community posting was added. Customer time saved, conversion and pricing evidence remain unknown.
