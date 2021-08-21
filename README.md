# HTMLとCSSを学ぶ

## コンテンツモデル

![contentsmodel](https://user-images.githubusercontent.com/52741042/130260672-11fe41ee-6911-4c3f-bac0-d063d9bde25e.PNG)

※[引用元](https://webgoto.net/html5/) ※[詳細参考url](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)

HTML5のタグには大きく分けて7つの種類があり，コンテンツモデルと言われている．詳細は[こちら](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/Content_categories)などを参照してほしい．

- Flow Content (フローコンテンツ) : ```<body>```タグ内で使用できる要素全体．
  - 主に，文や要素のかたまりを表す要素```p, div, ul, form, header, footer, section```，見出しを表す要素```h1 ~ h6```，中身を記述する要素(次の「記述コンテンツ」)を含む．
- Phrasing Content (記述コンテンツ) : 文章や，その中に含まれる要素全体．
  - 主に，テキスト自身，テキストレベルのセマンティクスを表す要素```a, b, br, span```や，フォームを中身を構成する要素```input, button, textarea```，外部リソースを表示する要素(次の)などを含む．
- Embedded Content (埋め込みコンテンツ) : 外部リソースを埋め込んで表示する要素全体．
  - 主に画像や動画，音楽などを含む．

の3つである．注意すべきなのは，集合の包含関係としては，```Flow Content ⊃ Phrasing Content ⊃ Embedded Content``` になっているということである．

CSSを考える上で何故これが重要になるかというと，各タグがこの3つのどこに所属するかによって，その要素のデフォルトのdisplay属性が異なっているからである．

- Flow には属するが，Phrasing には属さない： ```div, h1 ~ h6, p, ul, section, header, footer, form``` 
  - デフォルトは ```display : block```
- Phrasingには属するが，Embeddedには属さない： ```span, a, b, button, input, textarea``` 
  - デフォルトは ```display : inline```
- Embeddedに属する： ```img, video, audio, iframe, canvas```
  - デフォルトは ```display : inline-block```
  
以上の分類は非常に大事なので，是非頭の片隅に入れておいてもらいたい．
  
では次に，「ボックスモデル」という考え方を通じて，このdisplay属性が，スタイリングをするうえでどのような意味を持ってくるのかを説明する．
  
## ボックスモデル












