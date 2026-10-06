# Install, see a checked result, then try your task

**Free Windows private beta · runtime 0.1.0-beta · onboarding kit revision 1**

## Check your fit before downloading

Windows x64, PowerShell 5.1, Node >=22.18, Git, a local Work Desktop host supporting stdio MCP and plugins, and a signed-in Codex CLI with available quota. Web/mobile ChatGPT and remote-connector-only hosts cannot run this package. Windows 11 x64 with Codex CLI 0.160.0 was tested internally. Allow approximately 500 MB free space. Fresh machines/accounts, Windows 10 and cold reboot remain unverified. Scripts are unsigned.

[Request the installation kit](mailto:yipengyou72@gmail.com?subject=Codex%20Manager%20Windows%20Beta&body=Windows%20version%3A%20%0ALocal%20Desktop%20Work%20and%20MCP%2Fplugin%20support%3A%20%0ACodex%20signed%20in%3A%20%0ASmall%20task%20%28no%20source%20or%20secrets%29%3A%20) with your setup and a small task. Do not attach source or tokens. We send the ZIP, its own SHA256.txt and instructions after confirming fit. No payment signup.

## Short first-success path

1. Verify the received ZIP against its accompanying SHA256.txt and extract it completely.
2. Open START.cmd.
3. Read and approve **Install and run demo** on the local page.

The page automates prerequisite detection, installation, plugin/MCP registration, authorization of the known demo, natural-language task submission, polling, evidence checks and result display. It shows job ID, final checks, separate review and an accepted patch download. It does not alter your original repo. Reopen START.cmd to resume the saved request/job after a connection problem; completed evidence is shown without a new task.

**This launcher demo uses the same MCP tools outside a ChatGPT chat.** For the actual ChatGPT conversational experience, open a new local Work chat, select the Beta plugin if needed and send the task provided on the page. Those additional actions are counted separately. Five minutes is a target, not a promise; model work and separate review can take longer. See [measured results](ONBOARDING-RESULTS.md).

The original INSTALL.cmd/DEMO.cmd route remains available. The onboarding ZIP has a different checksum from the original 0.1.0-beta ZIP despite using the identical Manager runtime. Use the checksum provided with the kit you received.

## First real task

Pick one trusted non-production Git repo with a commit, clean working tree and prepared dependencies. Agree on a small task with existing checks and exact editable source files. Explicitly authorize its exact root using AUTHORIZE.ps1; acknowledge trusted local execution. ChatGPT may prepare the command, but cannot infer consent to access a new repo. Keep tests/configuration protected. Never use production credentials, customer records, payment operations or a deployment as the first task.

Describe the task in the new local Work chat. Keep the job ID, patch and evidence. Let ChatGPT handle normal polling and bounded repair. Escalated/failed is an outcome, not a pass. Review before separately applying any patch.

## Record feedback without a cloud service

Open FEEDBACK.cmd or START.cmd. The local form records install time, actual stages and extra actions, install/demo outcome, first real task outcome, estimated minutes saved, friction, desired features, continued-use intent and $19/$29/$49 monthly feedback. Unknown customer answers remain null. It writes JSON and Markdown under <InstallRoot>/state/trial; export/share only if you choose. The demo is never counted as a customer task. No payments are processed.

## Recovery

Missing dependency/login: follow the installer message, then reopen START. A registration conflict is preserved rather than overwritten. STATUS.cmd checks setup; REPAIR.cmd repairs owned registration; UNINSTALL.cmd removes this beta's startup/registrations while retaining evidence and repositories. Do not overwrite your whole host config. For an active task, wait/cancel before lifecycle changes. [FAQ](FAQ.md) · [Privacy and safety](PRIVACY.md).
