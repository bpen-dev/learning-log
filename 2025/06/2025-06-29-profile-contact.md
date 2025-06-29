# 2025-06-29

## 今日やったこと・学んだこと
- 著者紹介ページを追加した
  - `app/writer/page.tsx`を作成し、静的なプロフィールページを実装した。
  - `app/writer/page.module.css`でページのスタイリングを行った。
  - ユーザー提供のテキストに合わせて、ページの内容を更新した。
- サイドバーと記事ページから著者ページへのリンクを設定した
  - `components/Sidebar/index.tsx`を修正し、プロフィール名と画像から著者ページへ飛ぶようにした。
  - `components/Sidebar/index.module.css`を修正し、プロフィール名をリンクのように青色＋下線で表示されるようにした。
  - `components/Article/index.tsx`を修正し、記事内の著者名から著者ページへリンクするようにした。
- 免責事項とプライバシーポリシーのページを追加した
  - `app/disclaimer/page.tsx`と`app/privacy-policy/page.tsx`を作成した。
  - 共通のスタイルとして`app/disclaimer/page.module.css`を作成・適用した。
  - `components/Footer/index.tsx`と`components/Footer/index.module.css`を修正し、フッターに各ページへのリンクを追加した。
- publicフォルダの役割について学んだ
  - プロフィール画像などの静的ファイルは`public`ディレクトリに配置することで、アプリケーションから直接参照できることを確認した。 (`public/images/profile.jpg`)

## 疑問・課題
- 

## メモ
-
