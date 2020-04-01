### React.js について

- facebook によって開発されたオープンソースのフロントエンドフレームワーク。 <br>
  リアクティブ・プログラミング（何かの値が変化するとすぐに反映される仕組み） <br>
  プログラム的に仮の DOM(仮想 DOM)を構築して、それを操作する。 <br>
  通常の DOM に比べ、かなり高速。 <br>

- 用意するもの <br>
  npm で Node.js をインストール <br>

- DOM の仕組み(p64) <br>

  - DOM は１つ１つのタグを javascript のオブジェクトとして表す <br>
    それぞれのタグには DOM のオブジェクトが用意されている <br>
    そこにタグの表示や属性が全て詰まっている <br>

    オブジェクト - エレメント - ノード（１版小さい単位） <br>

    `<div>` <br>
    `<p>Hello<p>` <br>
    `</div>` <br>

    ↑div の中に含まれているもの <br>
    ・p タグのエレメント <br>
    ・改行と半角スペースのテキストノード <br>

- プロジェクトの実行 <br>
  ① npm start <br>
  ② npm run build <br>

- 基本スクリプト　 P67 <br>
  -index.html <br>
  `<script src="https://unpkg.com/react@16/umd/react.development.js"></script>` <br>
  `<script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>` <br>
  ↑ この２行を必ず head 内に書き入れる <br>
  <br>
  -script.js <br>
  ① 組み込み用のタグの取得 <br>
  `let dom = document.querySelector( '#root' );` <br>
  <br>
  ② 仮想 DOM のエレメントの作成 <br>
  `let element = React.createElement(` <br>
  `'p', {}, 'Hello React'` <br>
  `);` <br>
  ↑React.createElement(タグ名、属性、中に組み込まれるもの) <br>
  また、３番目の引数にノードや配列を使った複数のオブジェクトを指定したり、 <br>更に createElement を組み込むこともできる(p70) <br>
  <br>
  ③ 仮想 DOM をレンダリングして表示 <br>
  `ReactDOM.render(element, dom);` <br>
  ↑ 第一引数に createElement で作ったエレメント、 <br>
  　第二引数にそれをはめ込むタグの本来の DOM

- JSX
  HTML のタグを直接 javascript のスクリプトに記述する仕組みのこと。
