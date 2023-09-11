# CJKFont specification realignment

The goal of this repository is to identify discrepancies between the actual implementation of CJK OpenType fonts
and what is outlined in the OpenType specifications.
Based on these findings, we will then formulate proposals to amend the OpenType specifications,
ensuring they accurately reflect the real-world implementation of these fonts.

## Steps
1. プロジェクトに参加する各社が、フォントに使用しているテーブルをリストしたものを持ち寄って統合し、一つ一つ見てゆく作業を行う。
その際、日本語フォントに独特なテーブルを優先的に見てゆく。
2. 差異の見つかったテーブルについて違いを確定させ、規格文言の提案を開発し、OFFのGitHubで提案する。
規格文言は最小限必要な変更のみを行い、素早く規格に反映されることを優先する。1 と 2 は並行で作業する。
VORG, kern/paltには既に問題が見つかっており、作業が開始されている。
3. 上記が終了後、副次的な目標として、1&2の過程で見つかったフォントやUnicodeの問題点があれば、それらについて議論を行い、必要なら提案まで持ってゆく
