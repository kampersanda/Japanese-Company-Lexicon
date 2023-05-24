# 生成過程

まず、環境を準備する。

```shell
$ python -m venv venv
$ source venv/bin/activate
$ pip install -r requirements-own.txt
```

以下から、Unicode版の全国データをダウンロードしてくる。
（`wget`ではダウンロードできないので、ブラウザを介して）

https://www.houjin-bangou.nta.go.jp/download/zenken/#csv-unicode

zipファイルのまま、`data/hojin/zip`に置く。

その後、

```
$ bash scripts/download.sh
$ bash scripts/generate_alias.sh
```

結果、`data/dictionaries/output`にファイルが生成される。
