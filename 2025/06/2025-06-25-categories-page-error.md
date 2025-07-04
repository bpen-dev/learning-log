2025-06-25
今日やったこと・学んだこと
Vercelのデプロイ時にのみ発生していたNext.jsのビルドエラーを解決した。

エラーの根本原因は、Next.js App Routerの動的ルートにおけるparamsプロパティの型定義の不整合であったことを突き止めた。

App RouterのServer Componentでは、paramsがPromiseとして渡される仕様であることを学んだ。

paramsの型をPromise<{...}>として定義し、awaitで解決するようにコードを修正することでエラーを解消した。

ローカル環境（npm run dev）と本番ビルド（npm run build）では、TypeScriptの型チェックの厳格さが異なることを理解した。

上記のエラー解決の過程をまとめたブログ記事を作成し、アイキャッチ画像とALTテキストも準備した。

DNSのTXTレコードがドメイン所有権の証明に使われること、そしてDNS設定画面の「エイリアス」がCNAMEレコードを指し、TXTレコードとは異なる役割であることを学んだ。

疑問・課題
なぜローカルの開発環境とVercelのビルド環境でparamsの扱いに差異が生まれるのか、そのアーキテクチャ的な背景を引き続き理解する必要がある。

npm run buildをローカルで定期的に実行し、デプロイ前の問題を早期に発見するワークフローを確立したい。

メモ
Next.js App Routerで動的ルートを扱う際は、page.tsxやlayout.tsxのparamsをPromiseとして扱うことを常に意識する。

「ローカルでは動くのにデプロイで失敗する」場合、環境間の差異（特に型チェックの厳格さ）を疑うのが定石。

DNSレコードの「エイリアス」は基本的にCNAMEを指しており、TXTレコード設定時には「いいえ」で問題ない。
