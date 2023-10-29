![image](https://github.com/jphacks/NG_2309/assets/104612339/7fd2ef3c-8048-4fc5-b889-5ff5addcac68)# CalmEngineer

[![IMAGE ALT TEXT HERE](https://jphacks.com/wp-content/uploads/2023/07/JPHACKS2023_ogp.png)](https://www.youtube.com/watch?v=yYRQEdfGjEg)

## 製品概要
### 背景(製品開発のきっかけ、課題等）
厚生労働省[「令和三年　労働安全衛生調査(実態調査)結果」](https://www.mhlw.go.jp/toukei/list/dl/r03-46-50_kekka-gaiyo01.pdf)では各業界のメンタルヘルス不調による休業や退職状況についての集計をしています。この中でIT業界を指す「情報通信業」の集計結果はメンタル不調により「連続１ヶ月以上休業した労働者」がいた事務所は全体の26.7%(全業界中ワースト2位)。そして、「退社した労働者」がいた事業者は全体の11.7%(全業界中ワースト1位)と記録しており他業種から食らえてもメンタルヘルスに不調を抱えている人が多いことが伺えます。私たちはそれらの問題をコミットの感覚によってメンタルの不調具合を数値化することによって少しでも緩和できるのではないかと考えました。

### 製品説明（具体的な製品の説明）
githubのアカウントの情報を用いてgithubのcommitの間隔をAIに学習させてこれまでのcommitの間隔の周期性からどれだけ乖離しているかでストレス値を測りリポジトリに参加しているメンバー全員のストレス値とコミット数の遷移をグラフを一目で見れるようにしました。
### 特長
#### 1. リポジトリに参加している人全員のストレス値とcommit数が一覧で見れること。
#### 2. githubの認証を使っているのでセキュリティ的にも安全であること。
#### 3.　　AIから各々に合わせた適切なアドバイスをもらえること。

### 解決出来ること
- プロジェクトに参加している人を一目で管理できること
- AIからのアドバイスで今までのcommitを振り返られること
  
### 今後の展望
### 注力したこと（こだわり等）
* 
* 

## 開発技術
### 活用した技術
#### API・データ
* github api
* 

#### フレームワーク・ライブラリ・モジュール
* tensorflow
* numpy
* scipy
* flask
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
* /backend/main.py

#### 製品に取り入れた研究内容（データ・ソフトウェアなど）（※アカデミック部門の場合のみ提出必須）
* https://link.springer.com/article/10.1007/s41060-019-00186-0
* https://www.jstage.jst.go.jp/article/bjsiam/30/1/30_22/_pdf/-char/ja
