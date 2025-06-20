# 2025-06-20

## 今日やったこと・学んだこと
- **カテゴリ機能の実装**
    - **データ取得ロジックの追加**: `libs/microcms.ts`に、カテゴリ一覧や詳細を取得するための関数を追加した。
    - **カテゴリ一覧ページの作成**: `/categories`に、microCMSから取得した全カテゴリを一覧表示するページを新規作成した。
    - **カテゴリ別記事一覧ページの作成**: `/categories/[categoryId]`という動的なページを作成し、特定のカテゴリに属する記事を一覧表示できるようにした。
    - **ページネーションの実装**: カテゴリ別記事一覧にページネーション機能を追加し、記事が多数ある場合にも対応できるようにした。
    - **サイドバーとの連携**: サイドバーに、microCMSから取得したカテゴリ一覧が動的に表示され、各ページへ正しくリンクするように修正した。

## 疑問・課題
- 実装したカテゴリ機能やデザインについて、さらに改善できる点がないか、今後運用しながら検討する。
- 次はアーカイブページや著者ページの実装を計画する。

## メモ
- URLの構造（例: `/p/2`）は、分かりやすさを意識して設計することが重要。
