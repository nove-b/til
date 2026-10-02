
Macで.DS_Storeを作らない方法は、

``` bash
defaults write com.apple.desktopservices DSDontWriteNetworkStores True
killall Finder
```

上記を実行する。

なお、すでにあるファイルは

```bash
find . -name '.DS_Store' -type f -ls -delete
```

で削除できる。
