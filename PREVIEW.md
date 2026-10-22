# Unofficial historical Surfpool preview

This branch contains the combined SVM Replay integration, not an upstream
Surfpool release. Proposed upstream PRs remain separate and unmerged.

Revision 2 embeds Studio's replaced-socket ownership fix and pairs with Anchor's
fixture-compatible preview. Surfpool's execution sources and the SVM Replay
workers are unchanged from the previous preview.

[Downloads and tested installation instructions](https://github.com/xternet/surfpool/releases/tag/svm-replay-0.2.0-preview.2)

Requires [SVM Replay 0.2.0](https://github.com/xternet/svm-replay/releases/tag/v0.2.0).
Historical data limits fail explicitly. Epoch travel is synthetic, not replay
of skipped blocks. Native Windows historical forks remain unsupported; use WSL2.
