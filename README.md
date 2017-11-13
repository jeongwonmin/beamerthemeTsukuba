# beamerthemeTsukuba

筑波大学紫テーマのTeX beamer用オリジナルテーマです。研究集会などでご自由にお使いください。

## Usage
まず、テーマをbeamer themeがあるフォルダにコピーします。
例えば、macでbrew installしたtexlive 2017を使っている場合、beamerテーマのパスは次のようになります。

```
/usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes
```

このフォルダの下に、color, inner, outer, font, themeという5つのフォルダがあります。カラーテーマはcolorフォルダに、themeと画像ファイル(png, eps)はthemeフォルダの下にそれぞれコピーします。

```
$ sudo cp beamercolorthemeorchidUT.sty /usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes/color

$ sudo cp beamercolorthemewhaleUT.sty /usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes/color

$ sudo cp beamerthemeTsukuba.sty /usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes/theme

$ sudo cp imagine_white.png /usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes/theme

$ sudo cp tsukuba_logo_kanji.eps /usr/local/texlive/2017/texmf-dist/tex/latex/beamer/themes/theme
```

ファイルのコピーが終わったら、一回texをビルドする必要があります。ビルドのコマンドは次の通りです。

```
sudo mktexlsr
```

`\usetheme{Tsukuba}`して、デフォルトで入っている他のテーマのように使えます。

## 注意
macでは、特にパッケージをインポートしなくてもpng, eps両方使えます。しかしwindowsだと`\usepackage[dvipdfmx]{graphicx}してあげないとpngが使えないかもしれません。texlive2014だと、まだwindowsではpngが使えなかったりしたんですが、最近はどうでしょうか。

もしそのような問題が発生するならば、`beamerthemeTsukuba.sty` ファイルの `\RequirePackage[dvipdfmx]{graphicx}` をコメントアウトしてください。(文頭の%を消すことを「コメントアウト」と言います)

## ライセンス
texのオリジナルパッケージなどは、GNU General Public LicenceあるいはLaTeX Project Public Licenseの基で配布・改変することができます。
```
/usr/local/texlive/2017/texmf-dist/doc/latex/beamer/doc/licenses/LICENSE
```
にbeamerのライセンスがあります。(windowsの場合はパスが違うかもしれませんが、texmf-dist以下はほぼ同じかと思います。)

