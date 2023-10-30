# CalmEnginer
![image](https://github.com/jphacks/NG_2309/assets/104612339/7fd2ef3c-8048-4fc5-b889-5ff5addcac68)

[![IMAGE ALT TEXT HERE](https://jphacks.com/wp-content/uploads/2023/07/JPHACKS2023_ogp.png)](https://www.youtube.com/watch?v=yYRQEdfGjEg)

## 製品概要
### 背景(製品開発のきっかけ、課題等）
厚生労働省[「令和三年　労働安全衛生調査(実態調査)結果」](https://www.mhlw.go.jp/toukei/list/dl/r03-46-50_kekka-gaiyo01.pdf)では各業界のメンタルヘルス不調による休業や退職状況についての集計をしています。この中でIT業界を指す「情報通信業」の集計結果はメンタル不調により「連続１ヶ月以上休業した労働者」がいた事務所は全体の26.7%(全業界中ワースト2位)。そして、「退社した労働者」がいた事業者は全体の11.7%(全業界中ワースト1位)と記録しており他業種から食らえてもメンタルヘルスに不調を抱えている人が多いことが伺えます。私たちはそれらの問題をコミットの間隔によってメンタルの不調具合を数値化することによって少しでも緩和できるのではないかと考えました。

### 製品説明（具体的な製品の説明）
githubのアカウントの情報を用いてgithubのcommit履歴を取得し、異常検知モデルに学習させ、これまでのcommitの間隔の周期性からどれだけ乖離しているかでストレス値を測ります。これにより本人が気付けていない疲労をAIが可視化し、働きすぎを防止することが出来ます。また、ストレス値に応じたAIからのメッセージを受け取ることが出来、ストレス値が高い場合はねぎらいの言葉を掛けてもらえます。これに加えて、他のユーザーのストレス値を確認することもでき、同じプロジェクトで働く同僚のストレスレベルを知ることによって、プロジェクトを円滑に進めることが出来ます。
### 特長
#### 1. Githubのコミット履歴からAIがストレス値を判定して通知してくれる。
#### 2. アプリを使用したことのある全員のストレス値とcommit数が一覧で見れる。
#### 3. AIからストレス値に応じて応援メッセージやアドバイスをもらえる。

### 解決出来ること
- 自らのストレス値を知ることによって、働きすぎを防止する。
- プロジェクトに参加している人のストレス値を一目で確認でき、危機に陥っているメンバーを助けることが出来る。
- プロジェクトメンバーのストレス値を確認することによって、適切な仕事の割り振りが出来る。
- AIからのアドバイスで今までのcommitを振り返られること
  
### 今後の展望
今回の開発では、気になる人のストレス値、一ヶ月のコミット総数などを検索する機能を追加したが、今後はこれを発展させ同じプロジェクトで働いている同僚などのストレス値を表示し、同じプロジェクトで働いている人同士互いにいたわり合う事を助ける機能を追加したい。
また、ストレス値の算出方法をより改善し、正確にITエンジニアのストレスを判定する機構を追加したい。


### 注力したこと（こだわり等）
* 教師無し学習でAIを訓練出来るように、異常検知モデルを採用した。コミット履歴を説明変数にする都合上、どうしても訓練データが不足するという問題に直面し、ストレス値の信頼性が低なってしまう。そこで、複数のコミット予測を出力し正答データと比べることによって、正答データよりも大きく乖離する確率を下げるようにした。
* githubのoath2でgithubアカウントを認証することによって、ユーザーが安心かつ、githubからアクセスキーを自ら取得する手間無くアプリが使えるようにした。これにより、アプリの使い勝手が大幅に向上した。

## 開発技術
### 活用した技術
#### API・データ
* github api
* openai api

#### フレームワーク・ライブラリ・モジュール
* tensorflow
* numpy
* scipy
* flask
* pygih
* pygithub
* mariadb
* openai

#### デバイス
* Mac
* Windows

### 独自技術
#### ハッカソンで開発した独自機能・技術
* 周期性のある自然現象の異常検知などに使われるdLSTMを、コミット履歴という規則性はあるが予測の難しいものの異常検知に使用した。
* 先行研究では十分な精度を確保するためにLSTMを含めて9層のノードがあったが、ログイン処理にあまり時間を掛けないために、総数を可能な限り少なくした。
### 最も力を入れたファイル
* /backend/model/model_create.py

#### 製品に取り入れた研究内容（データ・ソフトウェアなど）（※アカデミック部門の場合のみ提出必須）
* https://link.springer.com/article/10.1007/s41060-019-00186-0
* https://www.jstage.jst.go.jp/article/bjsiam/30/1/30_22/_pdf/-char/ja
