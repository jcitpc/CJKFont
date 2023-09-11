# CJK Font specification realignment

The goal of this repository is to identify discrepancies between the actual implementation of CJK OpenType fonts
and what is outlined in the OpenType specifications.
Based on these findings, we will then formulate proposals to amend the OpenType specifications,
ensuring they accurately reflect the real-world implementation of these fonts.

## Steps
1. プロジェクトに参加する各社のフォントテーブルおよびレイアウトタグを持ち寄って、一つ一つ OpenType specification と比べてゆく
    - CJKフォントに独特なテーブルを優先的に見る
    - 検討したテーブル・タグごとに GitHub issue を一つ使う
2. 差異の見つかったテーブルについて違いを確定させ、規格文言の提案を開発し、OFFのGitHubで提案する
    - 規格文言は最小限必要な変更のみを行い、素早く規格に反映されることを優先する
    - 1 と 2 は並行で作業できる
    - kern/palt, VORG には既に問題が見つかっている
    - 提案ごとに docs フォルダの下にファイルを作り、変更をトラックできるようにする

副次的な目標として、上記の作業が終了後、その過程で見つかったフォントやUnicodeの問題点があれば、それらについて議論を行い、必要なら提案まで持ってゆく

## Tables
- [font_tables.md](https://github.com/jcitpc/CJKFont/blob/main/font_tables.md): List of font tables used by CJK fonts
- [GSUB.md](https://github.com/jcitpc/CJKFont/blob/main/GSUB.md): List layout tags that use the GSUB table
- [GPOS.md](https://github.com/jcitpc/CJKFont/blob/main/GPOS.md): List layout tags that use the GPOS table

## Proposal documents
- [palt_kern.md](https://github.com/jcitpc/CJKFont/blob/main/docs/palt_kern.md)
