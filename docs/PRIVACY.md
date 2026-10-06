# Local-first, with model context sent to the model service

The Manager stores registered repositories, isolated work copies, patches, checks, review output and local feedback on the user's machine. The control connection is local. The optional onboarding/feedback page binds only to 127.0.0.1 on a random port, checks its access token and browser origin, and has no cloud analytics or feedback endpoint.

Codex sends the authorized source context, task and check output needed for model work to its signed-in model service. ChatGPT processes the conversation supplied to it. Local-first does not mean fully offline or that code never leaves the machine. The beta does not replace the provider's account, privacy or retention policies.

The installer checks login through the Codex CLI; it does not read, copy or distribute authentication files. Local state uses current-user permissions and DPAPI-protected control/storage keys. Do not share state/private, credentials, whole config backups, or unreviewed raw logs. Logs and patches can contain code.

Only explicitly registered repos/files and frozen acceptance commands are eligible. The included known demo has narrow installer authorization. A real repo requires exact-path authorization and acknowledgment that its local checks are trusted. A work copy protects the original source from automatic modification; it is not an operating-system sandbox. Project checks run with current-user permissions, can access local/network resources allowed to that account, and must be trusted.

Up to three attempts and one active task. No automatic patch application, merge, push, production deployment, payment, destructive data action or silent widening of scope. Failed/rejected/escalated results remain visible. Passing checks and separate model review do not prove all behavior is correct; human review remains necessary.

Unsigned Windows scripts; Windows 11 x64 is the tested scope. A clean config on an existing machine is not a fresh Windows SID, VM, account or cross-machine validation. No compliance certification, zero-data-exposure claim, provider-independent security guarantee or support SLA is asserted.

Feedback is local JSON/Markdown with no automatic upload. Use short comments without source, secrets or customer data. Sharing an export is a separate user choice. Uninstall preserves data, logs, keys and backups; removing those retained files is a separate user decision after confirming the exact path and retaining anything needed.
