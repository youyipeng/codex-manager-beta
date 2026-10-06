# Apply, install, and run one task

Version: 0.1.0-beta. Free private beta; no payment signup. The runtime is distributed privately after checking eligibility.

## Eligibility

Windows x64 with PowerShell 5.1, Node.js >=22.18 and Git for Windows installed. You need a Desktop Work host with local stdio MCP and plugin support, and Codex CLI already signed in with available quota. Windows 11, Codex CLI 0.160.0 and Store host OpenAI.Codex 26.930.4958.0 were used internally. Capability checks run during installation. Web/mobile ChatGPT and desktops lacking local MCP/plugin support are outside this beta.

Allow about 500 MB free space. Fresh machines/accounts, Windows 10 and reboot/cold start remain unverified. Scripts are unsigned.

## Request the private kit

[Email the founder](mailto:yipengyou72@gmail.com?subject=Codex%20Manager%20Windows%20Beta) with your setup and a small task. Do not send source, passwords or tokens. The reply provides the ZIP, SHA256.txt and instructions.

The approved 0.1.0-beta Windows ZIP has SHA-256:

`9365ce13b104908dc2559cb0de8676b4e3b9d2012908adfd1dcf7a675851a183`

## Install

1. Verify the received ZIP against its checksum, then extract the whole archive.
2. Run INSTALL.cmd. It checks dependencies and registers this beta's local plugin/MCP.
3. Open a new local Work chat and select Codex Manager External Beta. Refresh/restart the host if requested.
4. Use the bundled DEMO-TASK.txt, then inspect the returned patch and check/review evidence.

STATUS.cmd checks setup; REPAIR.cmd repairs this beta's registration. UNINSTALL.cmd removes its services/registration while retaining results and backups. Read the ZIP README for exact authorization and lifecycle behavior.

## The measured real-repo trial

Choose a trusted, non-production Git repo with a commit, clean working tree and prepared dependencies. Fix the expected behavior, trusted checks and allowed source files before coding. Use the supplied AUTHORIZE.ps1 to authorize the exact root and files; keep tests/configuration protected. Do not use production access, credentials, customer records, trading actions or payment operations in the trial.

Give the requirement in your local Work chat. Keep the job ID, patch and evidence. After a connection drop, inspect that job rather than submitting a duplicate. Review the patch yourself before any separate application.

Measure dependency/login/download time separately from installation, and active supervision/review time separately from elapsed model time. Failure and escalation count as outcomes. There is no remote-control service implied by the invitation.
