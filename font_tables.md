|table|分類|検討優先順位|CFF|TrueType|
|:---|:---|:---:|:---|:---|
|OS/2|共通|√|√|√|
|BASE|CFF|√|√|M-optional only if converted from CFF|
|VORG|CFF|issue|√||
|CFF|CFF||√||
|vmtx/vhea|共通|√|√|√|
|cmap|共通||√|√|
|GSUB|共通||√|√|
|GPOS|共通||√|DM (F?)|
|head|共通||√|√|
|hmtx/hhea|共通||√|√|
|maxp|共通||√|√|
|name|共通||√|√|
|post|共通||√|√|
|GDEF|共通|√|A-PAN CJK||
|glyf/loca|TT|||√|
|fpgm/prep/cvt|TT|||DF, M-optional for hinting|
|gasp|TT|||F, M-optional for hinting|
|EBDT/EBLC|Bitmap|||M-optional for bitmap|
|hdmx/VDMX/LTSH|TT|||M-exceptional for adjustments to improve rendering|
|DSIG|共通||A|M-exceptional for compatibility with some fonts|
|meta|TT?|||M-exceptional for compatibility with some fonts|
|kern|TT|||D M-exceptional for compatibility with old apps|
|mort|Apple|||F,M-exceptional for compatibility with old apps|

- The checkmark indicates that the table is used by all developers
- Capital letters indicate that the table is used by the designated developers, followed by optional comment after a hyphen
  - A: Adobe
  - D: Dynacomware
  - F: Fonrworks
  - M: Morisawa
