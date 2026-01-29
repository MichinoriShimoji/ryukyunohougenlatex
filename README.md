# 『琉球の方言』LaTeX入稿用スタイルファイル

## ファイル構成

```
ryukyu-xelatex.sty    # XeLaTeX用スタイルファイル
ryukyu-platex.sty     # pLaTeX/upLaTeX用スタイルファイル
ryukyu-lualatex.sty   # LuaLaTeX用スタイルファイル

template_xelatex.tex  # XeLaTeX用テンプレート
template_platex.tex   # pLaTeX用テンプレート
template_lualatex.tex # LuaLaTeX用テンプレート
```

## 使い方

1. `.sty`ファイルを`.tex`ファイルと同じフォルダに置く
2. テンプレートをコピーして執筆開始


## 本文ルール（手動対応）

- **読点** → 全角カンマ（，）
- **句点** → 句点（。）のまま
- **カッコ** → 全角（「」『』（））
- **1桁数字** → 全角（１，２，３...）
- **2桁以上** → 半角（10，100...）

## グレースケールPDF出力

コンパイル後、以下のコマンドで完全なグレースケールに変換：

```bash
gs -sDEVICE=pdfwrite -dProcessColorModel=/DeviceGray -dColorConversionStrategy=/Gray -dPDFSETTINGS=/prepress -dNOPAUSE -dBATCH -dQUIET -sOutputFile=output_gray.pdf input.pdf
```

## スタイルファイルの場所（恒久的に使う場合）

TeX Liveのローカルディレクトリに置くと、どこからでも使える：

```bash
# Mac/Linux
mkdir -p ~/texmf/tex/latex/ryukyu
cp ryukyu-*.sty ~/texmf/tex/latex/ryukyu/
mktexlsr ~/texmf
```
