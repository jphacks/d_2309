# CalmEngineer

[![IMAGE ALT TEXT HERE](https://jphacks.com/wp-content/uploads/2023/07/JPHACKS2023_ogp.png)](https://www.youtube.com/watch?v=yYRQEdfGjEg)

## 製品概要
### 背景（製品開発のきっかけ、課題等）
厚生労働省[「令和三年　労働安全衛生調査(実態調査)結果」](https://www.mhlw.go.jp/toukei/list/dl/r03-46-50_kekka-gaiyo01.pdf)では各業界のメンタルヘルス不調による休業や退職状況についての集計をしています。この中でIT業界を指す「情報通信業」の集計結果はメンタル不調により「連続１ヶ月以上休業した労働者」がいた事務所は全体の26.7%(全業界中ワースト2位)。そして、「退社した労働者」がいた事業者は全体の11.7%(全業界中ワースト1位)と記録しており他業種から食らえてもメンタルヘルスに不調を抱えている人が多いことが伺えます。私たちはそれらの問題をコミットの感覚によってメンタルの不調具合を数値化することによって少しでも緩和できるのではないかと考えました。

### 製品説明（具体的な製品の説明）
githubのアカウントの情報を用いてgithubのcommitの間隔をAIに学習させてこれまでのcommitの間隔の周期性からどれだけ乖離しているかでストレス値を測りリポジトリに参加しているメンバー全員のストレス値とコミット数の遷移をグラフを一目で見れるようにしました。
### 特長
#### 1. リポジトリに参加している人全員のストレス値とcommit数の遷移が一目で見れること。
#### 2. githubの認証を使っているのでセキュリティ的にも安全であること。
#### 3. AIから各々に合わせた適切なアドバイスをもらえること。

### 解決出来ること
- プロジェクトに参加している人を一目で管理できること
- AIからのアドバイスで今までのcommitを振り返られること
  
### 今後の展望

- リポジトリに参加している人のストレス値とcommit数の遷移をグラフで見れるようにすること
- リポジトリに参加している人のストレス値とcommit数の遷移をAIが予測してくれるようにすること

### 注力したこと（こだわり等）

* 
* 

## 開発技術
### 活用した技術
#### API・データ
* github api
* 
* 

#### フレームワーク・ライブラリ・モジュール
* tensorflow
* numpy
* scipy
* flask
* pygih
* pygithub

pygithubはgithubのapiを叩くために使用しました。githubapiからcommitの行われた日付のデータを読みとり、そのデータをAIに学習させるために使用しました。

#### デバイス
* Mac
* Windows

### 独自技術
#### ハッカソンで開発した独自機能・技術

* 独自で開発したものの内容をこちらに記載してください
* 特に力を入れた部分をファイルリンク、またはcommit_idを記載してください。

#### 製品に取り入れた研究内容（データ・ソフトウェアなど）（※アカデミック部門の場合のみ提出必須）
* 
* 
