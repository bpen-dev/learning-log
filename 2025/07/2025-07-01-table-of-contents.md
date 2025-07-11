# 2025-07-01

## 今日やったこと・学んだこと
- Next.jsブログの記事ページに、投稿内容に応じた目次を自動生成する機能を実装した。
- サーバーサイドでHTMLをパースするために`cheerio`ライブラリを導入し、リッチテキストからh2、h3見出しを抽出する方法を学んだ。
- 抽出した見出しタグに動的にユニークなIDを付与し、目次の各項目からページ内アンカーリンクで飛べるようにした。
- 抽出した目次データをpropsとして受け取る`TableOfContents`コンポーネントを新規に作成した。
- `page.tsx`でデータ加工（目次抽出・本文へのID付与）を行い、UIコンポーネントである`Article.tsx`に渡すことで、それぞれの役割を分離した。
- CSSの擬似要素(`::before`)のスタイリングを修正し、箇条書きのマーカーを上下中央揃えに調整した。

## 疑問・課題
- 現在、目次は常に表示された状態だが、将来的にはユーザーが開閉できるアコーディオン形式にすると、さらに使いやすさが向上しそう。
- 記事が長くなった場合、スクロールに追従するフローティング目次もUIの選択肢として考えられる。

## メモ
- `cheerio`でHTMLをロードする際、`{ decodeEntities: false }`オプションを使うと、コードブロック内の特殊文字などが意図せず変換されるのを防げる。
- CSSの`transform: translateY(-50%)`は、`position: absolute`と組み合わせることで、要素を親要素に対して正確に上下中央に配置するのに非常に便利。
