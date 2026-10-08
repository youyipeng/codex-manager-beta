[Watch the finished 80-second historical replay](https://youyipeng.github.io/codex-manager-beta/demo.html) · [Source notes](../demo/SOURCE-NOTES.md)

# Codex Manager duration parser repair evidence

On October 5, 2026, one internal Codex Manager Stage 5.1 Desktop task reached a failed acceptance check, requested a repair, and completed after the second attempt. The first implementation passed 30 of 31 tests. After feedback about leading and trailing ASCII spaces, the second passed all 31, with lint, typecheck and build also passing and a separate review returning `accept`.

This is one recorded internal case. The separately packaged External Beta 0.1.0-beta demo passed 16 of 16 tests in one attempt. The 31-test repair sequence was recorded before beta packaging; it is not a new beta execution or an external customer result.

## The requirement and frozen checks

The task implemented `parseDuration(value)`: normalize full-width text with NFKC, accept non-negative integer amounts with `ms`, `s`, `m` and `h`, accept uppercase units and ASCII spaces, reject duplicate units and invalid input, and return integer milliseconds within `Number.MAX_SAFE_INTEGER`.

The request allowed edits only to `src/duration.ts`. It registered lint, typecheck, build and test before implementation, with at most three attempts. Tests and configuration were outside the editable scope. The final result lists only `src/duration.ts` as changed.

## The failure that triggered repair

The first attempt passed lint, typecheck and build but returned `null` for the valid input `"  2H  3M "`, which should return `7380000`. The test command exited with code 1. Selected lines from the recorded output are:

```text
ℹ tests 31
ℹ pass 30
ℹ fail 1
  null !== 7380000
```

The stored review verdict was `revise`. Its feedback requested fixing only the implementation file, preserving rejection of pure spaces and newlines, and rerunning all four checks without modifying tests or acceptance configuration. The recorded event sequence contains this feedback followed by a second working iteration.

## The second attempt and delivery

The repair normalized the input and removed ASCII spaces at its edges. It retained the newline rejection required by the contract. All four registered checks then exited with code 0, and the separate review returned `accept`:

```text
ℹ tests 31
ℹ pass 31
ℹ fail 0
```

The result contains a patch for the single allowed file. The preserved integrity record reports that the original repository remained unchanged. The recorded created-to-completed event interval was 681.204 seconds, about 11 minutes 21 seconds. An 80-second edit of these records is not the execution time.

## What this case establishes

The useful behavior is the link between a check failure, concrete feedback, another implementation attempt and checked delivery. This case shows that loop once. Passing these tests does not establish completeness for other tasks, customer time saved, general reliability or validated pricing. The separate review can use the same model; it is not an independent third-party audit.

The [sanitized artifact projection](../demo/repair-evidence-2026-10-08.json) contains the check records, actual review text, event timestamps and hashes of the source artifacts. Local originals were compared with the preserved source inventory on October 8; all 18 inventoried files matched. Hashes support traceability, not third-party attestation. Absolute paths, stack traces, raw screenshots, prospect records and the private runtime are excluded.

See the [existing recorded summary](../demo/recorded-result.json), [evidence boundaries](EVIDENCE.md) and [80-second recording script](../demo/demo-first-80s-2026-10-08.md). The finished 80-second historical artifact replay is available above; it is not a new live run.

## Request one free bounded trial

If you currently use Windows x64, a local Desktop Work host with MCP/plugin support and signed-in Codex with quota, you can request one small, non-production repository task. We will agree the acceptance check before running it and record setup friction, active review time, missed requirements and the final result. The beta is free; model access and usage remain separate. Authorized code and check context go to the signed-in model service. No automatic merge, push or deployment.

[Request a trial without installing first](mailto:yipengyou72@gmail.com?subject=Demo-first%20trial%20GITHUB-D1&body=Windows%20version%3A%20%0ALocal%20Desktop%20Work%20and%20MCP%2Fplugin%20support%3A%20%0ACodex%20signed%20in%20with%20quota%3A%20%0ASmall%20non-production%20task%20%28description%20only%29%3A%20%0ACurrent%20review%20or%20rework%20burden%3A%20)

Send a task description and environment details only. Do not email source code, credentials or private records. This independent beta is not an official OpenAI product.
