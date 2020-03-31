- React.js について
  facebook によって開発されたオープンソースのフロントエンドフレームワーク。
  リアクティブ・プログラミング（何かの値が変化するとすぐに反映される仕組み）
  プログラム的に仮の DOM(仮想 DOM)を構築して、それを操作する。
  通常の DOM に比べ、かなり高速。

- 用意するもの
  npm で Node.js をインストール

- DOM の仕組み(p64)

  - DOM は１つ１つのタグを javascript のオブジェクトとして表す
    それぞれのタグには DOM のオブジェクトが用意されている
    そこにタグの表示や属性が全て詰まっている

    オブジェクト - エレメント - ノード（１版小さい単位）

    `<div>`<br>
    `<p>Hello<p>`<br>
    `</div>`<br>

    ↑div の中に含まれているもの
    ・p タグのエレメント
    ・改行と半角スペースのテキストノード

- プロジェクトの実行
  * ① npm start
  * ② npm run build

- 基本スクリプト　 P67
  * ① 組み込み用のタグの取得<br>
   `let dom = document.querySelector( '#root' );`<br>
   
  * ② 仮想 DOM のエレメントの作成<br>
    `let element = React.createElement(`<br>
    `'p', {}, 'Hello React'`<br>
    `);`<br>
    ↑React.createElement(タグ名、属性、中に組み込まれるもの)
    また、３番目の引数にノードや配列を使った複数のオブジェクトを指定したり、更に createElement を組み込むこともできる(p70)
    
  * ③ 仮想 DOM をレンダリングして表示
    `ReactDOM.render(element, dom);`<br>
    ↑ 第一引数に createElement で作ったエレメント、
     第二引数にそれをはめ込むタグの本来の DOM
