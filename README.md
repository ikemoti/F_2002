
# おしゃべじたぶる（iOS）

[![IMAGE ALT TEXT HERE](https://jphacks.com/wp-content/uploads/2020/09/JPHACKS2020_ogp.jpg)](https://www.youtube.com/watch?v=G5rULR53uMk)

## 製品概要
- F_2002　をご参照ください。
野菜と雑談を通じて、身近に感じながら家庭菜園の達成を補助するアプリです。
栽培キットの購入から一貫したUXで育成アシストをアプリが行い、雑談機能では水や温度のアラートも行ってくれます。
可愛いキャラクターとUIデザインにより、子供と一緒に育てる保護者や若い女性にとって家庭菜園の障壁を低くしました。

詳しい資料は下記の通りです。  
https://docs.google.com/presentation/d/13iaOR-fD3DBfOAS06PP9HBRrHrt1RHAH9nM_f6ilguU/edit?usp=sharing

サーバーはこちら
https://github.com/jphacks/F_2002_1

### 背景(製品開発のきっかけ、課題等）
まず私たちは、learning-sprintの期間中、miroを用いてアイデアだしを行いました。  
https://miro.com/app/board/o9J_khlVPbg=/

いくつかアイデアが出た段階で各々が良いと思うアイデアを選び、議論を通じて「アグリテック」分野に挑戦してみたいということになりました。
理由としては
- コロナ化で家庭菜園のブームがあるため、ニーズが増えている
- 他の案だと既にデジタル化したものをデジタル化することになるが、家庭菜園のテックは新しいデジタルであり、クロステックになる
- メンバーの1人の実家が種苗店のため、農業に関するリソースと知見がある
-メンバーの技能それぞれを生かし、IoTやアプリなど、複合的な技術で制作ができる
というものが挙げられました。

実際に調査やヒアリングをしていく中で、需要があることを確認しました。
そこで伺った課題、続かない理由としては
- 水やりの適切な量、タイミングがわからない、忘れてしまう。
- 植物の知識がないので、良い日当たりや病気などがわからず枯らしてしまう
- 飽きてしまい続かない
が挙げられ、これらはIoTとチャット機能で解決できると判断しました。

また、水耕栽培を行うやさい物語のような、IoT家庭栽培の競合は少数確かに存在していましたが、水耕に限定されていることと、
どれも無機質で「おしゃべりができる」ことによって植物を身近に感じるサービスはありませんでした。

しかし、無機質を好むような本当に合理的な人であれば育てず野菜を購入する場合が多いのではないでしょうか。
私たちおしゃべじたぶるは機能的であるのみならず、本来無駄であるはずの雑談を通して野菜を身近に感じてもらう、それが家庭菜園の醍醐味であり、継続に繋がると考えました。

### 製品説明（具体的な製品の説明）

UIモックはこちら
https://www.figma.com/file/MMyBJ2hDuRvYvxwRzm39d1/test?node-id=0%3A1  
野菜と雑談を通じて、身近に感じながら家庭菜園の達成を補助するアプリ。
購入機能…栽培に必要なセットを盛り込んだものを一つのキットにし、簡単に購入できます。
チャット機能…難解な言葉を使わず、仲良くなることをメインに雑談やアラートなどを行います。
カメラ機能を盛り込み、葉っぱなどの写真から病気を推測し、適切な助言をチャット機能から送ります。
IoT機能…適切な水分量と現状の水分量から、チャット機能と連動し水やりのアラートをします。

### 特長

#### 特長 1　キャラクター
親近感を持つ、仲良くなるために必要なキャラ付けを行い、セリフ回しに特徴が出るようにしました。キャラクターはどれもオリジナルです。
暖かみがあるカラーリングで制作しました。
#### 特長 2　チャット
難解な言葉を使わず、仲良くなることをメインに雑談やアラートなどを行います。
カメラ機能を盛り込み、葉っぱなどの写真から病気を推測し、適切な助言をチャット機能から送ります。
#### 特長 3　IoT
温度や水分量を機器で計測し、データとして集積します。規定値を下回った場合、アラートとしてチャットに連動します。

### 解決出来ること
家庭菜園に興味があるが続けられない人向けに、知識や経験をアプリを通して提供し、可愛いキャラクターで心理的障壁を取り除き、収穫まで育成させる。

### 今後の展望
野菜の種類を増やし、育成の選択肢を増やす。
このアプリで実際に育成しきれるかの実験。
雑談機能の文言追加や、診断機能の充実など対応項目の増量。

### 注力したこと（こだわり等）
- デザイン
  - 今回、三人のデザイナーで協力して制作したため、デザイントーンがずれないように認識のすり合わせを念入りに行った。
UIUX、デザインスタイルはヒアリングを元に、刺さるものを考案し制作した。
- 機能
  - 提供いただいた機材を元にできることを増やし、チャットに連動できるようにした。

## 開発技術

### 活用した技術

#### API・データベース・環境

- ドキュメント: OpenAPI v3.0.0
- モックサーバー: Postman
- データベース: MySQL v8.0
- 環境: Docker Compose v3

#### フレームワーク・ライブラリ・モジュール
- go v1.15.2
  - [echo/v4](https://github.com/labstack/echo)
  - [gorm](https://github.com/go-gorm/gorm)
  - [realize](https://github.com/oxequa/realize)

#### デバイス

-
-

### 独自技術

#### ハッカソンで開発した独自機能・技術

- 独自で開発したものの内容をこちらに記載してください
- 特に力を入れた部分をファイルリンク、または commit_id を記載してください。
