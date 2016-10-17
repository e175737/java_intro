# はじめに
このプロジェクトは「Java入門」のための解説＋コード例＋課題例について整理している。想定している前提は以下の通り。

- 前提
  - Pythonで基本的なプログラミング（関数、制御文、スコープ、ファイルI/O、ユニットテスト）はできるレベル。
    - 参考: [2016年度 : プログラミング1](https://ie.u-ryukyu.ac.jp/~tnal/2016/prog1/)
      - モジュールは教えている。
      - クラスは教えていない。オブジェクトについても詳細は教えていない。
      - メモリを意識せずにプログラミングできる環境。
      - コンパイラ言語や静的型付け言語についての知識ゼロ。
  - C言語で基本的なプログラミング（コンパイル、実行、型宣言、配列、関数、制御文、ループ文、構造体）
    - 参考: [2016年度 : C言語入門](https://github.com/naltoma/c_intro)
      - インタプリタとコンパイラの違いを教えている。
      - 静的型付けと動的型付けの違いを教えている。
      - Pythonプログラミングをベースとして最低限のC言語文法を、コード例をベースに解説済み。
- 目標
  - 別講義「[2015年度: オペレーティングシステム](https://ie.u-ryukyu.ac.jp/syllabus/2016/late/60105300.html)」で、実装をJavaで進めるため、一般的なJava開発プロセスを一通り終えておきたい。具体的な要求は次の通り。

```
File I/O、構成管理(gradle)、バージョン管理、ユニットテスト、、、
```
- 上記を踏まえ、以下の事柄を含めつつ、Python 3 or C言語のコードと比較する形でJavaの解説を行う。
  - (0) 参考文献、サイトの提示。
  - (1) Javaにおけるコンパイラの役目。（Cコンパイラとの違い）
  - (2) 静的型付け言語と動的型付け言語の違い。（入門編ではC言語と基本的には一緒だが、継承周りの説明を含む）
  - (?) Makefile（ファイル分割されたプログラムのビルド方法）
  - (?) 「C言語の配列」と「Pythonのリスト」比較によるメモリのイメージ付け。
  - (?) 統合環境・デバッガの利用。
    - [IntelliJ](https://www.jetbrains.com/idea/)