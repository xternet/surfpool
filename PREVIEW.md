# Unofficial historical Surfpool preview

This branch contains the combined SVM Replay integration, not an upstream
Surfpool release. Proposed upstream PRs remain separate and unmerged.

The current source bounds historical account/candidate hydration to 100 accounts,
signature-status batches to 256, and archived block searches to four windows /
500001 slots. Oversized program writes fail before allocation in either mode.
Historical CLI keys use `--key env:NAME` or `--key-file FILE`; literal keys are
refused. Historical mode no longer funds the default CLI wallet implicitly;
explicit airdrop targets/keypairs remain available. Normal funding stays unchanged.

Native owner discovery still paginates before Surfpool's hydration guard and may
consume provider budget. Keep this unauthenticated development RPC private.
Never use real funded keys: recent signatures may be mainnet-valid, and durable
nonce signatures can remain valid until the on-chain nonce advances.

[Earlier snapshot downloads](https://github.com/xternet/surfpool/releases/tag/svm-replay-0.2.0-preview.2)
are pinned to that tag and do not include these latest source changes. Use this
branch for source review/builds; updated binary publication is separate.
Embedded Studio assets and SVM Replay workers are unchanged. Updated Studio
source is in the companion preview branch; no new UI assets are published here.

Requires [SVM Replay 0.2.0](https://github.com/xternet/svm-replay/releases/tag/v0.2.0).
Historical data limits fail explicitly. Epoch travel is synthetic, not replay
of skipped blocks. Native Windows historical forks remain unsupported; use WSL2.
