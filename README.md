# CSSを学ぶ

## コンテンツモデル

![contentsmodel](https://user-images.githubusercontent.com/52741042/130260672-11fe41ee-6911-4c3f-bac0-d063d9bde25e.PNG)

※[引用元](https://webgoto.net/html5/) ※[詳細参考url](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)

HTML5のタグには大きく分けて7つの種類があり，コンテンツモデルと言われている．詳細は[こちら](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)などを参照してほしいが，CSSを作るうえで大事になってくるのは

- Flow Content: <body>タグ内で使用できるタグ全体
- Phrasing Content: テキストのセマンティクスを明示するタグ全体
- Embedded Content: 外部リソースを置換して表示するタグ全体

の3つである．注意すべきなのは，集合の包含関係としては，```Flow Content ⊃ Phrasing Content ⊃ Embedded Content``` になっているということである．

CSSを考える上で何故これが重要になるかというと，タグがこのどこに所属するかによって，その要素のデフォルトのdisplay属性が変わってくるからである．

- Flow には属するが，Phrasing には属さない： ```div, h1 ~ h6, p, ul, header, footer, form``` → デフォルトは ```display : block```
- Phrasingには属するが，Embeddedには属さない： ```a, button, input, textarea``` → デフォルトは ```display : inline```
- Embeddedに属する： ```img, video, audio, iframe, canvas``` → デフォルトは ```display : inline-block```
  
このdisplay属性が，スタイリングをするうえでどのような意味を持ってくるのかをまずは説明する．












