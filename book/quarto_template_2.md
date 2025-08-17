---
title: Quarto Template 2
# subtitle: 
# author: PureHertz
# date: today
# bibliography: quarto_template_2_assets/references.bib  # bibtexファイル
---


## このテンプレートについて

Quartoのテンプレートです。Quartoについては、以下のリンクを参照してください。Quarto専用を含むMarkdownの表記方法も記載されています。

- https://quarto.org/

Quartoの他に以下のものが必要です。

- TinyTeX: Quartoインストール後に`quarto install tinytex`を実行してください。
- サンセリフフォント
  - Noto Sans
  - Noto Sans JP
- セリフフォント
  - Noto Serif (for book)
  - Noto Serif JP (for book)
- 等角フォント
  - PlemolJP

テンプレートのファイル構成は以下の通りです。

- `_quarto.yml`: Quartoの設定ファイル
- `_preamble_book.tex`: LaTeXのプリンブルファイル
- `***.md`: 各章のMarkdownファイル
- `***.qmd`: メインコンテンツ以外のMarkdownファイル
- `***_assets/`: 各章の画像やその他の素材を格納するフォルダ
- `refs.bib`: 参考文献のBibTeXファイル
- `the-optical-society.cls`: 参考文献のスタイルファイル
- `_book/`: 出力フォルダ

章ごとにMarkdownファイルを作成し、YAMLヘッダーで章のタイトルを指定します。テンプレートでは、`quarto_template_1.md`と`quarto_template_2.md`の2つの章を用意しています。imageファイルなどの素材は、各章ごとに`quarto_template_1_assets`や`quarto_template_2_assets`のようなフォルダを作成し、そこに配置して参照します。各章のMarkdownファイルと対応する素材フォルダを取り出せば、そのままtechnoteテンプレートでも使用できます。

上記以外に、まえがき`index.qmd`とあとがき`postface.qmd`のMarkdownファイルも用意しています。`index.qmd`が無いと`quarto render`が通らないので注意してください。参考文献と奥付は`references.qmd`で自動生成します。参考文献を使用しない場合は、このファイルを編集して参考文献部分をコメントアウトしてください。

全体の設定は`_quarto.yml`で行います。必要箇所を変更して使用してください。


## Section

`# xxx`は、Chapterに使うので、`## xxx`をChapterのひとつ下のレベルの見出し（section）とします。technoteテンプレートと共通化するため、章のタイトルはYAMLヘッダーで指定することにします。


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

: 表の例 {#tbl-yyy}

@tbl-yyy は表の例です。


## Figures & Links

### Figures

![図の例](quarto_template_2_assets/image.png){#fig-yyy width="100%" fig-pos='H'}

@fig-yyy は図の例です。

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

@Hansch2006 は引用の例です。


## Footnotes

Here is a footnote reference,[^2] and another.[^longnote2]

[^2]: Here is the footnote.

[^longnote2]: Here's one with multiple blocks.

Here is an inline note.^[Inlines notes are easier to write,
since you don't have to pick an identifier and move down to
type the note.]


## Page break

どうしてもレイアウト調整が必要な時に使います。
