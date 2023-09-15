|table|分類|優先順位|CFF|TrueType|コメント|
|:---|:---|:---:|:---|:---|:---|
|OS/2|共通|1|√|√|山本さん：要注意<br>藤: 見ておいた方が良さそう -  (hhea, vhea, head, name などと共に) フラグやバーティカルメトリクスなどシビアな話題が多いため|
|BASE|CFF|1|√|M-optional only if converted from CFF|山本さん：要注意<br>藤: 見ておいた方がよさそう - 具体的なユースケースが理解されづらい印象がある、瑣末ですが平均字面と ICF という語彙の違いは気になる|
|VORG|CFF|**0**|√||木田：問題あり。optional と書いてあるが、縦書きに必須<br>藤: 見ておいた方が良さそう - そもそもの話題のため|
|CFF|CFF||?|||
|vmtx/vhea|共通|?|√|√|藤: 見ておいた方が良さそう - そもそもの話題のため、`vhea.lineGap` の仕様と実装の矛盾など|
|cmap|共通|?|√|√|藤: おそらく問題ないだろう - (name と共に) Macintosh 向けのフィールドを省く和文フォントも出てきていますが...|
|GSUB|共通|?|√|√||
|GPOS|共通|?|√|DM (F?)||
|head|共通|?|√|√||
|hmtx/hhea|共通|?|√|√||
|maxp|共通|?|√|√||
|name|共通|?|√|√||
|post|共通|?|√|√||
|GDEF|共通|?|A-PAN CJK|||
|glyf/loca|TT|?||√||
|fpgm/prep/cvt|TT|?||DF, M-optional for hinting||
|gasp|TT|?||F, M-optional for hinting||
|EBDT/EBLC|Bitmap|?||M-optional for bitmap||
|hdmx/VDMX/LTSH|TT|?||M-exceptional for adjustments to improve rendering||
|DSIG|共通|?|A|M-exceptional for compatibility with some fonts||
|meta|TT?|?||M-exceptional for compatibility with some fonts|藤: おそらく問題ないだろう - palt/kern の議論で「フォントのサポート言語」を明示するテーブルとして話題が出たため記入|
|kern|TT|?||D M-exceptional for compatibility with old apps||
|mort|Apple|?||F,M-exceptional for compatibility with old apps||

- The checkmark indicates that the table is used by all developers
- Capital letters indicate that the table is used by the designated developers, followed by optional comment after a hyphen
  - A: Adobe
  - D: Dynacomware
  - F: Fonrworks
  - M: Morisawa
