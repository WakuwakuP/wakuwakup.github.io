---
layout: post
title: You're up and running!
category: Development
tag:
 - web
---

細かい見た目を変更しました．

### 修正点
 * スマートフォン表示で画像がはみ出る
 
### 修正方法

CSSに追記

```css:style.css
div#blogs img {
  max-width: 100%;
}
```

max-widthをすっかり忘れてた．

javascriptに追記

```javascript:main.css
$('div#blogs img').parent('p').css('text-align','center');
```

親要素を指定するCSSセレクタはまだないため苦労した．

そこそこ完成に近づいたと思う．

今後はjekyllのcategoryとtagを使う場所を設定したいですな．
