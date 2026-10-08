# Real historical replay

This 80-second video is assembled from real internal Stage 5.1 artifacts recorded October 5, 2026. It is an edited historical replay, not a live screen recording or a new External Beta run. The designed layout displays original artifact excerpts and labeled translations, not simulated product UI. Original created-to-completed event span: 681.204 seconds (about 11m21s); video duration is not execution time.

Sources: prompt.txt, request.json, events.jsonl, round-1-worker.json, round-1-checks.json, round-1-review.json, round-2-worker.json, round-2-checks.json, round-2-review.json, changes.patch, task-result.json. SHA-256 values and sanitized excerpts are in historical-evidence.json. Local source hashes matched the previously audited inventory. Hashes are traceability, not third-party attestation.

First checks: 30 pass, one failure on ASCII edge spaces. First review: revise. Manager feedback sent to iteration 2. Second checks: 31 pass, zero failures; lint, typecheck and build pass. Second review: accept. The original repo remained unchanged. The first worker did not claim that checks passed; the video does not attribute such a claim to Codex.

The repair diff wraps the actual replacement line for legibility. English explanatory captions translate/summarize the original Chinese request/review; Chinese excerpt panels preserve original text. Reviewer is a separate call and can use the same model. External Beta 0.1.0-beta passed a separate 16/16 run; this is not the 31-test historical run. No external customer trial, paid customer, measured customer savings or general reliability benchmark is claimed.

Private runtime, full stack traces, absolute local paths, credentials, unrelated chat/desktop content and prospect identities are excluded. The video is deliberately silent with burned-in English captions; SRT and VTT are supplied. Public evidence: https://github.com/youyipeng/codex-manager-beta/blob/main/demo/repair-evidence-2026-10-08.json
