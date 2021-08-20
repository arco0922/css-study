# CSSを学ぶ

## コンテンツモデル

![contentsmodel](https://user-images.githubusercontent.com/52741042/130260672-11fe41ee-6911-4c3f-bac0-d063d9bde25e.PNG)

※[引用元](https://webgoto.net/html5/) ※[詳細参考url](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)

HTML5のタグには大きく分けて7つの種類があり，コンテンツモデルと言われている．詳細は[こちら](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)などを参照してほしいが，CSSを作るうえで大事になってくるのは

- Flow Content (フローコンテンツ) : ```<body>```タグ内で使用できる要素全体
- Phrasing Content (記述コンテンツ) : 文章とその中に含まれる要素全体
- Embedded Content (埋め込みコンテンツ) : 外部リソースを埋め込んで表示する要素全体

の3つである．注意すべきなのは，集合の包含関係としては，```Flow Content ⊃ Phrasing Content ⊃ Embedded Content``` になっているということである．

CSSを考える上で何故これが重要になるかというと，各タグがこの3つのどこに所属するかによって，その要素のデフォルトのdisplay属性が異なっているからである．

- Flow には属するが，Phrasing には属さない： ```div, h1 ~ h6, p, ul, header, footer, form``` → デフォルトは ```display : block```
- Phrasingには属するが，Embeddedには属さない： ```span, a, button, input, textarea``` → デフォルトは ```display : inline```
- Embeddedに属する： ```img, video, audio, iframe, canvas``` → デフォルトは ```display : inline-block```
  
以上の分類は非常に大事なので，是非頭の片隅に入れておいてもらいたい．
  
では次に，「ボックスモデル」という考え方を通じて，このdisplay属性が，スタイリングをするうえでどのような意味を持ってくるのかを説明する．
  
## ボックスモデル












