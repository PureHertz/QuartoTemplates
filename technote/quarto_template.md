---
title: Quarto Template
subtitle: テクニカルノート用
author: PureHertz
date: today
bibliography: quarto_template_assets/references.bib  # bibtexファイル
---

## 更新履歴 {.unnumbered}

+ 2025-08-14
  - 参考文献を設定
+ 2025-08-13
  - 最初のバージョン


## このテンプレートについて

Quartoのテンプレートです。Quartoについては、以下のリンクを参照してください。Quarto専用を含むMarkdownの表記方法も記載されています。

- https://quarto.org/

Quartoの他に以下のものが必要です。

- TinyTeX: Quartoインストール後に`quarto install tinytex`を実行してください。
- サンセリフフォント
  - Noto Sans
  - Noto Sans JP
- 等角フォント
  - PlemolJP

テンプレートのファイル構成は以下の通りです。

- `_metadate.yml`: YAMLヘッダーの設定ファイル
- `_preamble_technote.tex`: LaTeXのプリンブルファイル
- `quarto_template.md`: Markdownファイル
- `quarto_template_assets/`: 画像やその他の素材を格納するフォルダ
- `the-optical-society.cls`: 参考文献のスタイルファイル

Markdownファイルを作成し、YAMLヘッダーでタイトルなどを指定します。imageファイルなどの素材は、各章ごとに`quarto_template_assets`のようなフォルダを作成し、そこに配置して参照します。各章のMarkdownファイルと対応する素材フォルダを取り出せば、そのままbookテンプレートのひとつの章として使用できます。

全体の設定は`_metadata.yml`で行いますが、基本的には変更不要です。


## Section

`# xxx`は、Markdownではタイトルに使うことがあるので、`## xxx`を最上位の見出し（section）とする。

### Subsection

#### Subsubsection

Text

##### Paragraph

Text


## Tables

| Header 1 | Header 2 |
|----------|----------|
|          |          |
|          |          |
|          |          |

: 表の例 {#tbl-xxx}

@tbl-xxx は表の例です。


## Figures & Links

### Figures

![図の例](quarto_template_assets/image.png){#fig-xxx width="100%" fig-pos='H'}

@fig-xxx は図の例です。

### Links

[Quarto](https://quarto.org)


## Equations

$$
  f(x) = ax^2 + bx + c
$${#eq-xxx}

式(@eq-xxx)は式の例です。本文中で参照した式番号に括弧は自動ではつかないので、手動でつけて下さい。インライン数式は$f(x) = ax^2 + bx + c$です。


## List

- Item 1
- Item 2
- Item 3
  - Item 3-1
  - Item 3-2

1. Item 1
2. Item 2
3. Item 3
   1. Item 3-1
   2. Item 3-2


## Code blocks

`inline code block`

```python
# Code block example
print("Hello, World!")
```


## Citations

[@Hall2006;@Hansch2006] は引用の例です。


## Footnotes

Here is a footnote reference,[^1] and another.[^longnote]

[^1]: Here is the footnote.

[^longnote]: Here's one with multiple blocks.

Here is an inline note.^[Inlines notes are easier to write,
since you don't have to pick an identifier and move down to
type the note.]


## Page break

どうしてもレイアウト調整が必要な時に使います。

{{< pagebreak >}}


## HTML

HTMLへのレンダリングも可能です。プレビュー用なのでそれほど詳細な設定はしていません。


## 参考文献・資料{.unnumbered}

::: {#refs}
:::