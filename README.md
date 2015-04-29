# awesome-ggplot2
ggplot2に関連するパッケージは現在かなりの数があります。その中から「これはいいね」という素敵なパッケージを集めてまとめることにしました。なお現在試験的に作成しています。

## index (追加順)
- [ggExtra](#ggextra) - 散布図の周りに周辺分布(ヒストグラム)を同時出力するパッケージ
- [ggmap](#ggmap) - `ggplot2`で地図&位置データを活用したプロットを描写
- [ggdendro](#ggdendro) - デンドログラムや樹形図を描写
- [ggthemr](#ggthemr) - テーマ拡張
- [ggthemes](#ggthemes) - テーマ拡張
- [GGally](#ggally) - ペアプロットを`ggplot2`で描写など
- [ggfortify](#ggfortify) - 主要パッケージの出力をそのまま`ggplot`
- [ggmcmc](#ggmcmc) - mcmcの出力を簡単に`ggplot`へ

以下準備・検討中リスト

{pitchRx},{RcmdrPlugin.KMggplot2},{eeptools},{ggparallel},{ggsubplot},{popgraph},{PairedData},{ggRandomForests},{xkcd},{COPASutils},{ggROC},{granovaGG},{PKreport},{bdscale},{ggswissmaps},{MCMC.OTU},{gapmap},{ggenealogy},{Rz},{PKgraph},{mapDK},{orgR},{vdmR},{ggtern},{sjPlot},{choroplethr}

## パッケージ紹介
### ggExtra
- サイトリンク
  - [GitHub](https://github.com/daattali/ggExtra)
  - [CRAN](http://cran.r-project.org/web/packages/ggExtra/index.html)
- 概要
  - `ggplot2`で描写した散布図に、x and/or yの周辺度数の分布を加えてくれるパッケージ
  - メイン機能`ggMarginal()`に`ggplot()`で作成したオブジェクトを放り込むと作成可能
  - `> ggmarginal(data=mtcars,x="wt",y="mpg")`というようにデータから直接でも可能
- サンプルコード
  - 基本的な使い方は[GitHub](https://github.com/daattali/ggExtra)もしくはパッケージ内[vignette](http://cran.r-project.org/web/packages/ggExtra/vignettes/overview.html)を
  - デモとコード生成をしてくれるShiny appがありますのでぜひチェックしてください。
- インストール
  - CRANよりインストール
```R
install.packages("ggExtra")
```

### ggmap
- サイトリンク
  - [GitHub](https://github.com/dkahle/ggmap)
  - [CRAN](http://cran.r-project.org/web/packages/ggmap/index.html)
- 概要
  - `ggplot`で地図(GoogleMap, OpenStreetMapなど)を描く&地図上にプロットを描くパッケージ
  - `get_map()`でMapオブジェクト(表示させる地図データ)を設置
  - `ggmap()`でMapオブジェクトをplot
  - `geocode()`(地名から緯度経度を出力)や`revgeocode()`(緯度経度から住所を出力)も便利
  - `ggimage(hadley)`であの方が…
- サンプルコード
  - 極々基本的な使い方は[GitHub](https://github.com/dkahle/ggmap)を
  - サンプル: [地図を描きたい俺はgoogleVisパッケージかggmapパッケージかどちらを使おうか迷うが、静的な地図を描きたい場合はggmapで良いみたい](http://d.hatena.ne.jp/teramonagi/20140815/1408099162) 
- インストール
  - CRANよりインストール
```R
install.packages("ggmap")
```

### ggdendro
- サイトリンク
  - [GitHub](https://github.com/andrie/ggdendro)
  - [CRAN](http://cran.r-project.org/web/packages/ggdendro/index.html)
- 概要
  - `ggplot`を使ってデンドログラムや樹形図を描かせるパッケージ
  - 基本関数`ggdendrogram()`では、出力オブジェクトはggplotクラスで返します
  - `dendro_data()`関数を使えば、デンドログラムなどの出力結果を`ggplot()`に放り込めるデータ型へ変換
  - `hclust`や`tree`、`dendrogram`や`rpart`クラスに対応
- サンプルコードなど
  - 基本的な使い方はパッケージの[vignette](http://cran.r-project.org/web/packages/ggdendro/vignettes/ggdendro.html)を
  - 上記を参考に作成したサンプル: [RPubs - ggdendroのテスト](https://rpubs.com/kazutan/ggdendro_test)
- インストール
  - CRANよりインストール
```R
install.packages("ggdendro")
```
  
### ggthemr
- サイトリンク
  - [GitHub](https://github.com/cttobin/ggthemr)
- 概要
  - `ggplot`オブジェクトにテーマを自動的に割り当てることができる拡張パッケージです
  - 事前に`ggthemr('sea')`のようにテーマをセットすれば、以降自動的にそのテーマでggplotされます
  - 解除したいときは`ggthemr_reset()`を実行
  - 他にもレイアウトやスペースなどを設定可能
- サンプルコードなど
  - 各テーマの例は[GitHub](https://github.com/cttobin/ggthemr)を
  - メイン関数`ggthemr`については[How to use the ggthemr R function | Rdocumentation](http://www.rdocumentation.org/packages/ggthemr/functions/ggthemr)を
- インストール
  - GitHubよりインストール
```R
library("devtools")
install_github('ggthemr', 'cttobin')
```

### ggthemes
- サイトリンク
  - [GitHub](https://github.com/jrnold/ggthemes)
  - [CRAN](http://cran.r-project.org/web/packages/ggthemes/index.html)
- 概要
  - `ggplot2`にテーマ設定を簡単に当てることができるようになる拡張パッケージです
  - ` + theme_stata()`のようにtheme_(テーマ名)と追加するだけで変更可能
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
install.packages("GGally", dependencies=TRUE)
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
