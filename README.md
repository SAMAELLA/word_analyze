![Uploading 人間失格.png…]()


# word_analyze

このリポジトリは、青空文庫のテキストを取得し、日本語の単語出現頻度を分析して、ワードクラウドとして可視化するための Jupyter Notebook です。

## できること

- 青空文庫のZIP形式テキストをダウンロードする
- ルビ・注釈・本文以外のメタ情報を除去する
- MeCab で形態素解析を行う
- 連続する名詞や助数詞の組み合わせを整形する
- 出現頻度の高い語を表示する
- 日本語のワードクラウドを描画する

## 対象ファイル

- `word_analyze.ipynb` : メインの分析処理

## 必要な環境

- Python 3.10 以上
- Jupyter Notebook または VS Code の Python 拡張
- MeCab
- `matplotlib`
- `wordcloud`

## インストール

```bash
pip install jupyter matplotlib wordcloud mecab-python3
```

Windows では、ワードクラウドの描画用に日本語フォントが必要な場合があります。例として、`C:\Windows\Fonts\MEIRYO.TTC` を使用しています。

## 使い方

1. `word_analyze.ipynb` を開く
2. `URL` 変数に青空文庫の対象作品のZIP URLを設定する
3. ノートブックのセルを上から順に実行する
4. 作品名・作者名・上位頻出語が出力される
5. ワードクラウドが表示される

```python
URL = 'https://www.aozora.gr.jp/cards/000035/files/301_ruby_5915.zip'
```

## 例

- 作品本文の前処理
- ルビや注釈の除去
- 日本語の単語頻度の集計
- `wordcloud` による可視化

## 注意点

- このノートブックは青空文庫の公開作品を対象としており、URL を変えることで別作品も分析できます。
- `MeCab` の辞書やフォント環境が整っていないと、解析や描画が正常に動作しないことがあります。
- 文字コードは `shift_jis` を前提としているため、青空文庫の通常のテキスト形式に対応しています。
