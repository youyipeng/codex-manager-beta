# Install, see a checked result, then try your task

**Free Windows private beta · runtime 0.1.0-beta · onboarding kit revision 2**

## Check your fit before downloading

Windows x64, PowerShell 5.1, Node >=22.18, Git, a local Work Desktop host supporting stdio MCP and plugins, and a signed-in Codex CLI with available quota. Web/mobile ChatGPT and remote-connector-only hosts cannot run this package. Windows 11 x64 with Codex CLI 0.160.0 was tested internally. Allow approximately 500 MB free space. Fresh machines/accounts, Windows 10 and cold reboot remain unverified. Scripts are unsigned.

[Request the installation kit](mailto:yipengyou72@gmail.com?subject=Codex%20Manager%20Windows%20Beta&body=Windows%20version%3A%20%0ALocal%20Desktop%20Work%20and%20MCP%2Fplugin%20support%3A%20%0ACodex%20signed%20in%3A%20%0ASmall%20task%20%28no%20source%20or%20secrets%29%3A%20) with your setup and a small task. Do not attach source or tokens. We send the ZIP, its own SHA256.txt and instructions after confirming fit. No payment signup.

## Short first-success path

Download, verify the ZIP checksum and extract it completely. Then:

1. Open **START.cmd**.
2. Click **OK** in the first-run consent window.

No extra start button on the local page is required. Missing Node/Git are downloaded from official releases, verified against pinned SHA-256 hashes, and kept inside this installation; system PATH is not changed. Desktop, sign-in and model quota are prerequisites. Registration, demo creation/limited authorization, the displayed natural-language task, polling and result display are automatic. Original repositories are unchanged.

**Two actions means after extraction.** Download, extraction, Windows warnings, login and protocol confirmations count additionally when present. Automated tests do not observe a stranger's actions or waiting time. Use the checksum supplied with this revision.

The result page contains **Open prepared ChatGPT task**, also saved as OPEN-CHATGPT.cmd. It preloads the Beta plugin and existing demo job. The Desktop user sends the draft; switching to Work may also be needed. This retrieves the same launcher result, without another demo. It does not validate a complete new-task ChatGPT handoff. [Official launch-link behavior](https://learn.chatgpt.com/docs/app/commands#deep-links).

Reopen START to resume the saved request/job. Completed results are displayed without another model call. Initial failure runs STATUS / REPAIR / STATUS and writes DIAGNOSIS.txt. Changed authorization, a damaged package or another installation's registration never gets silently overwritten.

The core/runtime and frozen demo checks are unchanged. An installation-only adapter configures HTTPS for Codex exec against the official endpoint with the same signed-in account, default model and original restrictions. [Actual internal measurements](ONBOARDING-RESULTS.md) describe measured and unmeasured costs; they are not a universal five-minute promise.

## First real task

Pick one trusted non-production Git repo with a commit, clean working tree and prepared dependencies. Agree on a small task with existing checks and exact editable source files. Explicitly authorize its exact root using AUTHORIZE.ps1; acknowledge trusted local execution. ChatGPT may prepare the command, but cannot infer consent to access a new repo. Keep tests/configuration protected. Never use production credentials, customer records, payment operations or a deployment as the first task.

Describe the task in the new local Work chat. Keep the job ID, patch and evidence. Let ChatGPT handle normal polling and bounded repair. Escalated/failed is an outcome, not a pass. Review before separately applying any patch.

## Record feedback without a cloud service

Open FEEDBACK.cmd or START.cmd. The local form records install time, actual stages and extra actions, install/demo outcome, first real task outcome, estimated minutes saved, friction, desired features, continued-use intent and $19/$29/$49 monthly feedback. Unknown customer answers remain null. It writes JSON and Markdown under <InstallRoot>/state/trial; export/share only if you choose. The demo is never counted as a customer task. No payments are processed.

## Recovery

Missing dependency/login: follow the installer message, then reopen START. A registration conflict is preserved rather than overwritten. STATUS.cmd checks setup; REPAIR.cmd repairs owned registration; UNINSTALL.cmd removes this beta's startup/registrations while retaining evidence and repositories. Do not overwrite your whole host config. For an active task, wait/cancel before lifecycle changes. [FAQ](FAQ.md) · [Privacy and safety](PRIVACY.md).
