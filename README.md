# awesome-ggplot2
ggplot2に関連するパッケージは現在かなりの数があります。その中から「これはいいね」という素敵なパッケージを集めてまとめることにしました。なお現在試験的に作成しています。

- [ggfortify](#ggfortify)
- [ggmcmc](#ggmcmc)

## ggfortify
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

## ggmcmc
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
