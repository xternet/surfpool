# Unofficial historical Surfpool preview

This branch contains the combined SVM Replay integration, not an upstream
Surfpool release. Proposed upstream PRs remain separate and unmerged.

The current source limits historical account batches to 100 accounts before
acquisition and bounds archived block searches to four windows / 500001 slots.
Queries that exhaust that work bound fail explicitly; narrow the search.
Historical CLI keys must use `--key env:NAME` or `--key-file FILE`; literal keys
are refused. The normal RPC path, embedded Studio and SVM Replay workers remain
unchanged. Keep this unauthenticated development RPC private.

[Earlier snapshot downloads](https://github.com/xternet/surfpool/releases/tag/svm-replay-0.2.0-preview.2)
are pinned to that tag and do not include these latest source changes. Use this
branch for source review/builds; updated binary publication is separate.

Requires [SVM Replay 0.2.0](https://github.com/xternet/svm-replay/releases/tag/v0.2.0).
Historical data limits fail explicitly. Epoch travel is synthetic, not replay
of skipped blocks. Native Windows historical forks remain unsupported; use WSL2.
