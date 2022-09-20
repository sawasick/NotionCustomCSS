# NotionCustomCSS
## Notionアプリにカスタムcssを実装する
---
## Usage
### macの場合
- Notion.app > Contents > Resources > app > renderer > preload.jsを開く
- ファイル末尾に下記コードを記載
```js
function AddCustomCSS(){
  const link = document.createElement("link");
  link.href = "https://sawasick.github.io/NotionCustomCSS/main.css";
  link.rel = "stylesheet";
  document.getElementsByTagName("head")[0].appendChild(link);
}

document.addEventListener('DOMContentLoaded', function () {
  AddCustomCSS();
});
```
