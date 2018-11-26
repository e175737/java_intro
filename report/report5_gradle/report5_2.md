# 課題レポート5: Gradle＆JavaDocに慣れよう

- 前期からの変更点
  - 課題説明は「課題概要」のみで十分です。
  - 今回のレポート5についても「最大3ページ」に収めるようにして下さい。
    - ソースファイルはGitHubで確認できるので、レポートに全コードコピペ掲載する必要はありません。特に工夫した点のみを掲載した上で解説・考察しよう。

- ＜目次＞
- <a href="#abst">課題概要</a>
- <a href="#details">詳細仕様</a>
  - <a href="#details_step1">ステップ1: コードの準備。</a>
  - <a href="#details_step2">ステップ2: gradleによるjarファイルの作成。</a>
  - <a href="#details_step3">ステップ3: ソースコードとJavaDocドキュメントの関係について。</a>
- <a href="#report">取り組み方</a>
- <a href="#submit">提出方法</a>

<hr>

## <a name="abst">課題概要</a>
- 過去のレポート課題で作成したプロジェクトに、Gradleを導入してみよう。
- JavaDocによるドキュメンテーションに慣れよう。

<hr>

## <a name="details">詳細仕様</a>
### <a name="details_step1">ステップ1: コードの準備。</a>
- IntelliJでGradleプロジェクトを新規作成。
  - GroupID/ArtifactIdは「report5」とする。
  - プロジェクト名も上記同様。
- [課題レポート3](https://github.com/naltoma/java_intro/blob/master/report/report3_refactoring/report3.md)で作成したjavaファイルを、src/main/javaとsrc/test/javaに配置する。
  - src/main/java/package名/以下に置くべきファイル
    - LivingThing.java, Enemy.java, Hero.java, Main.java
  - src/test/java/package名/以下に置くべきファイル
    - EnemyTest.java
      - JUnit5パッケージを追加するため、Enemyクラスを開いた状態で、「Go to から create new test」を選択した方がベター。
  - 補足: **課題レポート3を終えてない人は、まずそれを終えよう**。
- 動作確認。
  - Main.javaが動作することを確認しよう。
  - EnemyTest.javaが動作することを確認しよう。
  - 上記2件が動作するなら、git管理に設定し、add+commit+push.
    - build.gradleも含めて、プロジェクト内の設定ファイルは全てaddすること。
    - push先のgithubリポジトリも作成しておこう。リポジトリ名は 「report5」とする。
      - report3時のリポジトリに上書きするのではなく、新規にreport5というリポジトリを作成し、そこにpushしよう。
- レポート報告事項
  - ステップ1に関しては、pushしたリポジトリURL（作業用URL）を報告するだけで良い。

<hr>

### <a name="details_step2">ステップ2: gradleによるjarファイルの作成</a>
- 仕様
  - build.gradleを編集し、jarファイルを生成するように設定せよ。
    - 条件1: mainメソッドを含むMain.javaをコンパイルするように設定すること。
    - 条件2: sourceCompatibilityを10にすること。
- 動作確認
  - IntelliJからでも、ターミナルからでもどちらでも構わないので、gradleを使ってjarファイルが生成できることを確認しよう。
  - jarファイル生成できたら、jarファイルを実行しよう。この出力結果がMainクラスと同等であることを確認しよう。
    - 動作確認できたら、add+commit+pushしよう。build.gradleのaddを忘れないように。
- レポート報告事項
  - jarファイルを実行した際の出力結果。

<hr>

### <a name="details_step3">ステップ3: ソースコードとJavaDocドキュメントの関係について。</a>
- 背景
  - 用意されたソースコードには、予めJavaDoc形式のドキュメントが埋め込まれている。IntelliJ, javadocコマンドどちらでも構わないのでドキュメントを生成し、以下の課題に取り組め。
- 課題1
  - ブラウザでLivingThingクラスを開いた状態のキャプチャをレポートに含めよ。キャプチャはメソッド概要の途中までを含むものとする。（最後まで含めなくて良い）
- 課題2
  - LivingThingクラスについて、ソースコード（LivingThing.java）とドキュメント（HTMLファイル）を比較し、対応関係について考察せよ。
    - レポートには気づいた点を5個以上列挙すること。
- 課題3
  - LivingThingクラスは各自で実装したクラスのため、ドキュメントが記述されていない箇所があると思われる。どこでも構わないので1箇所以上記述し、JavaDocドキュメントを生成して確認せよ。
    - 確認後、GitHubへpushせよ。
    - レポートには、変更点を述べるだけで良い。
    - 「どこでも構わない」とあるが、もし、最初からすべての要素（フィールド変数、コンストラクタ、メソッド）にドキュメント記述を終えている場合、無理に修正せず、その旨を報告するだけで良い。

<hr>

## <a name="report">取り組み方</a>
- ペアや友人らと話し合って取り組んで構わないが、コード解説を加えるなど「自分自身の報告書」となるように取り組むこと。試して分かったこと、自身で解決できなかった部分等についてどう取り組んだか、といった過程がわかるように示すこと。（考えを図表や文章を駆使して表現して報告する練習です）
- レポート作成は好きなツール（ソフトウェア）を使って構わない。ただし下記を含めること。
  - タイトル
    - 今回は「**プログラミング2、レポート課題5: 「Gradle＆JavaDocに慣れよう」**」。
  - 提出日: yyyy-mm-dd
  - 報告者: 学籍番号、氏名
    - 複数人で相談しながらやった場合、相談者らを「**協力者: 学籍番号、氏名**」として示そう。
  - 課題説明（概要のみでOK）
  - 結果と考察
    - **課題への取り組みを通し、課題の意義、課題から分かったこと、今後の展望などを述べる。失敗やつまづきがあれば、それらについての失敗分析を含めること。**
    - 参考リンク: [実験レポートの書き方](http://www.report.gusoku.net/jikken/jikkenreport.html)
  - その他
    - 通常は感想等をレポートには含めませんが、練習なので課題に取り組みながら何か感じたこと、悩んでいること等、書きたいことがあれば自由に書いてください。（なければ省略OK）

<hr>

## <a name="submit">提出方法</a>
- 提出物は「レポート」の1点である。
- レポートは電子ファイルで提出するものとする。
- 提出先:
  - 「Google ドキュメント」のreport5。
- 締切: 調整中。