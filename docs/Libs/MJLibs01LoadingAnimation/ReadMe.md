# ローディングアニメーションの実装方法

## １．htmlファイルの<script>タグを使った実装方法
    <head>
      <script type="text/javascript" src="MJLibs01LoadingAnimation.js"></script>
      <script type="text/javascript">
        var lda = new MJLibs01LoadingAnimation({});
      </script>
    </head>
    <body>
      <button onclick="lda.Start()">再生</button>
      <button onclick="lda.Stop()">停止</button>
    </body>
外部スクリプトとして「MJLibs01LoadingAnimation.js」を読み込みます。  
「MJLibs01LoadingAnimation」メソッドをnewで変数の中にインスタンス化して格納します。  
 
あとはbuttonタグにonclickを設置し、インスタンスから「Start」メソッドおよび「Stop」メソッドを呼び出すだけです。 
 
上記の例では、「再生」ボタンを押すとアニメーションが始まり、「停止」ボタンを押すとアニメーションが終了します。

## ２．別の外部javascriptで実装
htmlファイルに外部スクリプトとして読み込みます。
    <!-- htmlファイル -->
    <script type="text/javascript" src="MJLibs01LoadingAnimation.js"></script>

別の外部
var lda = 