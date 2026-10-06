# Codex Manager — Windows Beta

**Give ChatGPT the task. Let it manage Codex until tests pass.**

Hand off one small repo task from a local ChatGPT Work chat to Codex. The local Manager fixes the editable scope and checks, verifies the result separately, requests bounded repairs, and returns a patch with evidence. Up to three attempts; success is not guaranteed.

**Windows x64 · local-first · free private beta · runtime 0.1.0-beta**

[Landing page](https://youyipeng.github.io/codex-manager-beta/) · [Request the installation kit](mailto:yipengyou72@gmail.com?subject=Codex%20Manager%20Windows%20Beta&body=Windows%20version%3A%20%0ALocal%20Desktop%20Work%20and%20MCP%2Fplugin%20support%3A%20%0ACodex%20signed%20in%3A%20%0ASmall%20task%20%28no%20source%20or%20secrets%29%3A%20) · [Install and first task](docs/INSTALL.md) · [Privacy and safety](docs/PRIVACY.md) · [FAQ](docs/FAQ.md)

Send your Windows setup, local Work/MCP/plugin availability, Codex sign-in status and a small task description. Do not send source or credentials. Compatible users receive the private ZIP and checksum. No checkout or payment signup.

## A real failed attempt, followed by repair

An internal Desktop run on October 5, 2026 began with one natural-language request for a duration parser:

**First attempt: 30/31 → Manager rejects and requests repair → Codex repairs → 31/31, separate review accepts.**

Lint, typecheck and build also passed. The failed case concerned leading/trailing ASCII spaces. The original repo stayed unchanged; the result was a patch. [Sanitized recorded result](demo/recorded-result.json) · [Evidence scope](docs/EVIDENCE.md) · [45-second demo plan](demo/RECORDING-SCRIPT.md).

This sequence was recorded on **Stage 5.1**, before beta packaging. The separately packaged External Beta demo passed **16/16 in one round**. Neither is an external customer success or a general reliability/productivity benchmark. The review is a separate call and can use the same model. A video has not yet been recorded.

## Get to a checked result with less setup

The new private onboarding kit automates dependency checks, registration, demo authorization, submission, polling and evidence display. Extract → open START.cmd → approve the displayed demo. It also collects local JSON/Markdown feedback.

The three-stage shortcut runs through the beta MCP **outside a ChatGPT chat**. To experience the conversational handoff, open a new local Work chat, select the plugin if your host requires it, and send the provided task. Those steps are additional. Five minutes is a target, not a guarantee. [Measured onboarding results](docs/ONBOARDING-RESULTS.md).

Required: Windows x64, PowerShell 5.1, Node >=22.18, Git, a local stdio-MCP/plugin-capable Desktop Work host, signed-in Codex with quota. Web/mobile and remote-only connector hosts are unsupported. No new API key is requested by the tested login path; model access and usage remain separate.

## Where your code goes

Repo files, work copies, patches and evidence stay on your PC. **Authorized code context, prompts and check output are sent to your signed-in model service.** ChatGPT processes your conversation. This is not fully offline or zero cloud exposure. The onboarding feedback has no added cloud service or automatic upload.

Real repos require exact-path/file authorization and trusted local checks. The demo authorizes only its known sample. Local checks execute project code as your Windows user; a work copy is not an OS sandbox. No automatic merge, push, deployment or payment. [Full privacy and safety boundaries](docs/PRIVACY.md).

## What this beta can and cannot replace

[Cursor](https://cursor.com/docs), [Devin](https://docs.devin.ai/essential-guidelines/when-to-use-devin) and [Factory Droid](https://docs.factory.com/droid-cli/overview) already offer coding-agent, review and automation workflows. We have no head-to-head benchmark or superiority claim. This experiment focuses on ChatGPT managing Codex in one authorized local Windows work copy, with frozen checks and a returned patch. It is not a replacement editor or a broad hosted agent platform. Existing hooks/CI may already solve your problem. [Honest comparison and FAQ](docs/FAQ.md).

## Current limits

- Windows 11 x64 tested; fresh machines/users, Windows 10, macOS/Linux and cold reboot unverified.
- One active task, at most three attempts, limited supported check syntax; complex monorepos and arbitrary providers unverified.
- Unsigned scripts; prerequisites and sign-in are still required. Model quota/network/review delays may exceed five minutes.
- No guaranteed success, automatic application to source, checkout, paid plan or supported payment flow.
- No completed external customer trial, measured customer time saved or validated pricing yet. $19/$29/$49 are research questions.

Public: documentation and sanitized internal evidence. Private: commercial core/runtime, raw traces, prospect records and credentials. This independent beta is not an official OpenAI product.
