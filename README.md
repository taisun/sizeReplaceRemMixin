# sizeReplaceRemMixin

値をremに変更するmixinです。
関数型っく書いてみました。

configで設定します。

```css
//font
$font-size: 14px; // ベースとなるフォントサイズです

//margin base
$base-mrgin: 4px; // ベースとなるマージンです

$mgns: (　// 調整用マージンです
  xs: $base-mrgin,
  sm: $base-mrgin * 2,
  md: $base-mrgin * 4,
  lg: $base-mrgin * 8,
  xl: $base-mrgin * 12,
  xxl: $base-mrgin * 16,
);
```
第一引数で設定した引数の名前かサイズ(rem)を渡します。
第二引数CSSのプロパティを渡します。
第三引数は!importantの判定です。基本はfalseです。

**style.scss**

```css
@include sizeReplace($size, $prop, $boolean);
```
