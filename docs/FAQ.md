# Questions before your first task

## Why not Cursor, Devin or Factory?
Use them if they already fit your workflow. [Cursor](https://cursor.com/docs) supports coding, debugging, review, hooks and cloud agents. [Devin](https://docs.devin.ai/essential-guidelines/when-to-use-devin) documents local CLI and cloud sessions, testing, review and automatic fixes. [Factory Droid](https://docs.factory.com/droid-cli/overview) runs through terminal/editor/Git workflows. These products already have verification and automation; this beta does not uniquely invent an agent repair loop.

Our narrow experiment is a ChatGPT-to-Codex handoff, one explicitly authorized local work copy, frozen acceptance checks, a separate review and a returned patch. Up to three attempts, one active task, Windows only. No head-to-head benchmark, no performance/safety superiority claim, no replacement editor. If your hooks/CI already handle this, the extra value may be zero. Measure your own supervision time.

## Does my code leave my PC?
Repo files, work copies, patches and evidence are stored locally. Authorized code context, prompts and check output are sent through signed-in Codex to its model service. ChatGPT also processes the conversation you give it. Local-first is not offline or zero cloud exposure. This kit has no added cloud feedback service or telemetry uploader. Do not send source or secrets in a beta application. Read [Privacy and safety](PRIVACY.md).

## Is installation difficult?
The private onboarding kit offers three grouped stages: extract, open START.cmd, approve the displayed demo on the local page. It detects prerequisites, installs/registers the beta and authorizes only the known sample. That shortcut submits the natural-language task through MCP outside ChatGPT. The conversational trial additionally needs a new local Work chat, possibly selecting the plugin, and sending the task. Missing dependencies, login, security dialogs and refresh are additional actions. There is no measured stranger installation rate or five-minute guarantee.

## Why Windows only?
Windows 11 x64 is the tested scope. This package uses Windows-specific background startup, local pipes and DPAPI. macOS/Linux, Windows 10, a new Windows account/VM and cold reboot are not validated by the current trial. No launch date is promised. A short recorded example is available to understand the workflow; it is not a substitute for a supported live trial.

## Do I need an API key?
The tested path uses an existing signed-in Codex CLI account with available access/quota. The installer does not ask for a new API key and does not read/copy your authentication files. You still need suitable Codex access, local host capabilities and model connectivity; availability is checked rather than inferred from a subscription name. Model usage is separate from any future Manager fee. This beta does not grant Codex access or support arbitrary providers.

## Why would I pay?
Only if the saved supervision and clearer acceptance evidence on your own tasks outweigh setup, review and failure costs. The private beta is currently free. $19/$29/$49 per month are research questions, not active plans. There is no checkout, paid entitlement or supported purchase flow. A demo passing tests does not justify a productivity or willingness-to-pay claim.

## What if it fails?
Failed checks can trigger bounded repair, up to the registered iteration budget. A final failed/rejected/escalated result stays that status and includes the available evidence. Quota/network errors can also stop progress. Keep the job ID and inspect/resume that job rather than duplicating it. Review the patch yourself. Passing tests can still miss defects; separate review can use the same model. No guaranteed success, refund policy or support SLA is implied by a free beta.

## What gets permission to run?
The installer grants narrow authorization to its known bundled demo. Another repo needs an exact path and editable source files registered by AUTHORIZE.ps1, plus acknowledgment of trusted local checks. Tests/configuration remain protected. Checks execute project code as the current Windows user; the isolation is a work copy, not an OS sandbox. Choose a trusted non-production repo, prepared dependencies and no secrets/customer data. Returned patches are not automatically applied, merged or pushed.

## How do I uninstall or roll back?
UNINSTALL.cmd removes this beta's host registrations and background startup, and stops its idle worker. It preserves repos, demo, patches, logs, backups, keys and release files. During an active task, lifecycle changes are refused; wait or cancel through the task tool first. REPAIR.cmd can restore this beta's registration after uninstall. The verified lifecycle covers same-version repair/update; cross-version rollback is not validated. Never restore an entire host config over other plugins. No original source patch is applied by default, so there is usually no code rollback to perform.

## What is public?
Documentation and sanitized internal evidence. The commercial core/runtime, prospect records, authentication files and raw local traces are not published. This independent beta is not an official OpenAI product.
