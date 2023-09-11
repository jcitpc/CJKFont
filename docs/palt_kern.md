# OpenType ‘palt’ and ‘kern’ Documentation Revision Proposal 
Nat McCully, Principal Scientist, Adobe 

## Introduction
For CJK font developers, the wording in the documentation of the ‘kern’ and ‘palt’  features is confusing.
This proposal aims to improve it so font developers will know how to define the features,
and application developers will know how to set default behaviors for those features. 

## The Problem
In the ‘kern’ documentation, it is stated: 
>*UI suggestion:* This feature should be active by default for horizontal text setting.
>Applications may wish to allow users to add further manually-specified adjustments to suit specific needs and tastes. 
>
>*Script/language sensitivity:* None. 
>
>*Feature interaction:* If 'kern' is activated, 'palt' must also be activated if it exists.
>If 'palt' is activated, there is no requirement that 'kern' must also be activated. 

Meanwhile, the ‘palt’ documentation states: 

>*UI suggestion:* This feature would be off by default.
>
>*Script/language sensitivity:* Used mostly in CJKV fonts. 
>
>*Feature interaction:* This feature is mutually exclusive with all other glyph-width features
>(e.g. 'fwid', 'halt', 'hwid', 'qwid' and 'twid'),
>which should be turned off when it’s applied.
>If 'palt' is activated, there is no requirement that 'kern' must also be activated.
>If 'kern' is activated, 'palt' must also be activated if it exists. See also 'vpal'. 


There are several issues with this: 
1. The UI suggestions conflict with the feature interactions:
  ‘kern’ is on by default; ‘palt’ is  off by default.
  However, when ‘kern’ is on, ‘palt’ must also be on.
  If ‘palt’ is off by default in CJK fonts, that implies ‘kern’ must also be off by default
  (at least for those glyphs affected by ‘palt’).  
3. The default options are complex:
   CJK fonts, containing both proportional Latin glyphs (which are, by default, kerned)
   and monospaced CJK glyphs (which can be set proportionally with ‘palt’ but not by default),
   seem to require several levels of default  behavior.
   Which should be the default behavior,
   and is that default font-wide,
   or specific to certain ranges of the font’s glyphs?
   For example, when optionally setting CJK glyphs proportionally,
   should kerning also be on by default?
   Should kerning only be considered default for the non-CJK glyphs in a CJK font? 

## Improvement Suggestions
I would improve the documentation with slight re-wording and addition of some more CJK-related information.

In the ‘kern’ documentation, change: 
>*UI suggestion:* This feature should be active by default for horizontal text ~~setting~~ **in scripts other than mono-spaced CJK**.
>Applications may wish to allow users to add further manually-specified adjustments to suit specific needs and tastes. 
>
>*Script/language sensitivity:* ~~None~~ **By default shall not be activated on monospaced (e.g. CJK script) glyphs,
>but may be activated on any proportional (e.g. non-CJK) glyphs.**
>
>*Feature interaction:* If 'kern' is activated, 'palt' must also be activated if it exists.
>If 'palt' is activated, there is no requirement that 'kern' must also be activated. 

In addition to the above, we could consider adding a note explaining 
that CJK fonts often contain both proportional Latin and monospaced CJK glyphs, 
which makes kerning the glyphs more complex than in the case of an all-proportional font. 
When the font contains proportional glyphs, 
addition of kerning pair information would mean only those pairs with kern adjustments would be set proportionally, 
making the number of pairs likely to be very high and the cost of production very high as well. 
Using ‘palt’ first to transform the widths of the monospaced glyphs to be proportional
and applying ‘kern’ deltas to a few pairs is much more sensible as a solution.

In the ‘palt’ documentation, change:
>*UI suggestion:* This feature would be off by default. 
>
>*Script/language sensitivity:* Used mostly in CJKV fonts **to transform the monospaced glyphs’ widths to be proportional.**
>
>*Feature interaction:* This feature is mutually exclusive with all other glyph-width features
>(e.g. 'fwid', 'halt', 'hwid', 'qwid' and 'twid'), which should be turned off when it’s applied.
>If 'palt' is activated, there is no requirement that 'kern' must also be activated.
>If 'kern' is activated, 'palt' must also be activated if it exists. See also 'vpal'. 

In addition to the above, we could consider adding a note explaining that 
due to the conventional practice of including proportional Latin glyphs 
in the same font as CJK monospaced glyphs, and the fact that CJK text 
(e.g. Japanese text) can be set either monospaced or proportionally, 
and be kerned in addition to the base proportional widths for even finer tuning, 
that special consideration of the default values for such fonts is needed. 
