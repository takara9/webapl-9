# Istioテスト用のマルチレイヤなマイクロサービス

Istioを適用して、RESTサービス間の連携の様子を可視化できることを確認するためにのサンプルアプリです。
ヘッドとなるアプリは、v1とv2があり、機能の差は、カウンターの有無だけです。


* apl-head-v1 :  REST データキャッシュからランダムにデータを取り出して返す
* apl-head-v2 :  REST 上記の機能に加え、何回同じものを返したかのカウンタ値を追加する
* apl-cache :    REST データキャッシュ
* apl-counter :  REST アクセスカウンタ
* apl-dataload : キャッシュへ初期データをセットするためのバッチ処理コンテナ

それぞれのディレクトリでコンテナをビルドして Docker Hubへプッシュする。



