|layout tags|CJK独特|優先|PAN CJK|J|C|K|コメント|
|:---|:---:|:---:|:---|:---|:---|:---|:---|
|cpct|*|?|||√|||
|halt|*|?|√|√|√|√|藤: 見ておいた方が良さそう - vhal と共に備考に後述|
|kern||**0**|√|√|||木田：問題あり。CJK等幅グリフに対してデフォルトでOFFであるべき|
|mark|*|?|√|||||
|palt|*|?|√|√|||木田：問題あり。kernとの関わり合いで目的を明確化|
|vert|*|?|√|||||
|vhal|*|?|√|√|√|√||
|vkrn|*|?|√|√||||
|vpal|*|?|√|√|||
|vrt2|*|?|||||村田:追加
|vrtr|*|?|||||村田:追加

木田：村田さん、vrt2/vrtr はどこからも報告されていませんが、議論する必要があると言うことですか？

## Remarks

- chws/vchw (おそらく問題ないだろう, モリサワ藤)
  - [FONTPLUS](https://fontplus.jp/usage/services/chws-vchw) さんで実例おありかと思いますが為念 (藤)
    - 参照: [Contextual Spacing GPOS Features—Redux](https://ccjktype.fonts.adobe.com/2019/04/contextual-spacing-gpos-features-redux.html), [googlefonts/chws_tool](https://github.com/googlefonts/chws_tool)
- halt/vhal (見ておいた方が良さそう, モリサワ藤)
  - [半角に詰められないグリフ](https://github.com/kojiishi/east_asian_spacing/blob/main/docs/glyphlist-ja.md#半角に詰められないグリフ): 約物をゆったりと作っているフォントが存在する
  - 対象グリフがさほど自明ではない...?
  - 国外での普及度について: [全角半角碎碎念 (2018)](https://www.thetype.com/2018/02/14211/)  
    ```
    Jiang Jiang: 多中日字体是没有一致的标点符号特性支持的，比如 halt/hwid/palt 等支持都很差
    Jiang Jiang: 日文字体的 OpenType 支持其实也参差不齐，同一个厂商的字体都有很多不一致的问题
    Eric Liu: 但是一般水准还是比中国厂商好一大截，当然，这是另外一个问题了
    Eric Liu: 「halt/hwid/palt 等支持都很差」只反映目前中文字体厂商的不作为，毕竟 Opentype 规格都已经发布二十多年了；相比之下日文字库大多都支持这些特性
    ```
