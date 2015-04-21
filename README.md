# awesome-ggplot2
ggplot2に関連するパッケージは現在かなりの数があります。その中から「これはいいね」という素敵なパッケージを集めてまとめることにしました。なお現在試験的に作成しています。

## index
- [ggthemes](#ggthemes)
- [GGally](#GGally)
- [ggfortify](#ggfortify)
- [ggmcmc](#ggmcmc)

以下準備・検討中リスト

{ggmap},{ggdendro},{pitchRx},{RcmdrPlugin.KMggplot2},{eeptools},{ggparallel},{ggsubplot},{popgraph},{PairedData},{ggRandomForests},{xkcd},{COPASutils},{ggROC},{granovaGG},{PKreport},{ggExtra},{bdscale},{ggswissmaps},{MCMC.OTU},{gapmap},{ggenealogy},{Rz},{PKgraph},{mapDK},{orgR},{vdmR},{ggtern},{ggthemr}

## パッケージ紹介
### ggthemes
- サイトリンク
  - [GitHub](https://github.com/jrnold/ggthemes)
  - [CRAN](http://cran.r-project.org/web/packages/ggthemes/index.html)
- 概要
  - `ggplot2`にテーマ設定を簡単に当てることができるようになる拡張パッケージです
  - ` + theme_stata()`の様にtheme_(テーマ名)と追加するだけで変更可能
  - Scalesについてもカラーパターンが色々準備されています
  - ` + theme_excel()`であのグラフが眼前に蘇ります
- サンプルコードなど
  - 基本的な使い方およびサンプルコードは[GitHub](https://github.com/jrnold/ggthemes)を
  - 上のREADME.mdの内容は`vignette("ggthemes")でも確認できます(html)
- インストール
  - CRANよりインストール(Windowsでは事前に`Rtools`のインストールが必要)
```R
install.packages("ggthemes", dependencies=TRUE)
```

### GGally
- サイトリンク
  - [GitHub](https://github.com/ggobi/ggally)
  - [CRAN](http://cran.r-project.org/web/packages/GGally/index.html)
- 概要
  - `ggplot2`での作画を補助・拡張するパッケージです
  - `ggpairs()`でペアプロット図を`ggplot2`出力で描くことが可能
  - titleなどのオプションの指定は`ggplot2`とは異なり関数内オプションでそのまま記述
  - `ggnet()`は`ggplot2`を使って`igraph`or`network`classのオブジェクトからネットワークプロットを作成
- サンプルコードなど
  - 基本的な使い方は[`ggpairs()`のヘルプ](http://rpackages.ianhowson.com/cran/GGally/man/ggpairs.html)を
  - サンプル: [美しいペアプロット図を簡単に作る - My Life as a Mock Quant](http://d.hatena.ne.jp/teramonagi/20130412/1365767677)
  - サンプル: [美しいペアプロット図を簡単に作る - 驚異のアニヲタ社会復帰への道](http://d.hatena.ne.jp/MikuHatsune/20130412/1365774348)
- インストール
  - CRANよりインストール
```R
install.packages("ggmcmc", dependencies=TRUE)
```

### ggfortify
- サイトリンク
  - [GitHub](https://github.com/sinhrks/ggfortify)
- 概要
  - 一般的なRパッケージで`ggplot2`をスムーズに使えるようにしたパッケージです
  - カバーしているパッケージが非常に多く、また設定も簡単に行えます
- サンプルコードなど
  - 解説およびサンプルは上記GitHubのリンクを参照してください
  - サンプル: [RPubs - Concepts and Basics of ggfortify](http://rpubs.com/sinhrks/basics)
- インストール
  - GitHubよりインストール
```R
library(devtools)
install_github('sinhrks/ggfortify')
```

### ggmcmc
- サイトリンク
  - [GitHub](https://github.com/xfim/ggmcmc)
  - [CRAN](http://cran.r-project.org/web/packages/ggmcmc/index.html)
  - [サイト](http://xavier-fim.net/packages/ggmcmc/)
- 概要
  - `ggplot2`を使ってMCMCの実行結果を容易に可視化するパッケージです。
  - `JAGS`に加えて`MCMCpack`、`rstan`などの出力に対応しています。
- 解説・サンプルコードなど
  - 解説及びサンプルは上記サイトのリンクを参照してください
  - サンプル: [RPubs - Plotting Stan results with ggmcmc](http://rpubs.com/ssong/ggmcmc_stan)
- インストール
  - CRANミラーよりインストール
```R
install.packages("ggmcmc", dependencies=TRUE)
```
