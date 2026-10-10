# N64ModernRuntime repository instructions

This repository owns the N64 guest ABI and host runtime used by static recompilations. `librecomp/src` owns recompilation dispatch and translated libultra calls; `ultramodern/src` owns scheduling, events, messages and VI state. Consumers own game symbols and guest discovery in their separate repositories.

The current RACER acceptance runs on Steam Deck in the Arch distrobox. The accepted runtime revision is paired with RACER's `deck-runtime-accepted` branch. Preserve the original dirty checkout and inherited changes; use canonical Worktrunk worktrees for implementation. Changes must retain guest register sign extension and the native word-storage/XOR accessor conventions.

Validate runtime changes through the real consuming game build and observed gameplay, input and compositor output. Counters, fabricated guest state and standalone fake harnesses do not establish acceptance. Retain binary/source provenance and complete probe output, and name missing capabilities. Do not rerun unchanged probes or introduce unit tests or fixtures.

Both this file and `CLAUDE.md` are regular repository-owned files. Record substantive findings in the shared dated `docs/field-notes` file when there are new findings.
