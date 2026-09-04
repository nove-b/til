`npm insall`とは別に`npm ci`というのがあることを知った。

`npm install`は`package-lock.json`を参考にインストールすること。

`npm ci`は`package-lock.json`を厳密に再現しインストールすること。

つまり`npm install`だと`package-lock.json`があっても必要に応じて更新することがある。

## どう使い分ける？

ローカル開発では依存の追加・更新が日常的に発生するため、`lockfile`を更新する`npm install`が適切。

`CI`では「l`ockfile`に記録された依存を正確に再現する」ことが目的。`lockfile`を更新する`npm install`は、ビルドごとに異なる依存ツリーを生成するリスクがあるので`npm ci`が適切。
