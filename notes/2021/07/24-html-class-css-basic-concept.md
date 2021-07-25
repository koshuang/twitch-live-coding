# 2021-07-25 Twitch Streaming


> Subject: [Teach] Basic HTML Concept

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

- favicon (favorite icon)
  - https://medium.com/unalai/%E8%AA%8D%E8%AD%98-favicon-%E4%B8%A6%E4%BD%BF%E7%94%A8%E5%B7%A5%E5%85%B7%E5%8D%94%E5%8A%A9%E5%AE%8C%E6%95%B4%E6%80%A7-f41658955657
  - Free favicon: https://www.freefavicon.com/
  - 語法
```html
<link rel="icon" type="image/x-icon" href="favicon.ico" />
<link rel="icon" type="image/png" sizes="16x16" href="/images/favicon.png">
```

- 網頁
  - 觀念
    - 通用屬性
      - class
      - style
    - 常見標籤
      - a (anchor)
        - 屬性:
          - href: 放網址
          - target: _blank 代表開新的 tab

## CSS 觀念

- 例子： `color: red`
- 屬性 (Properties)
  - 修改屬性是改變你HTML元素的一種方法 . (在這範例中, color 是段落（p）元素的一種屬性.) 在CSS中, 你可以選擇哪些屬性用來影響 rule.
- 屬性值 (Property value)
  - 屬性值 就是位於屬性右邊，在冒號（:）之後，從眾多的可能樣式選出一個給予屬性（範例中就是從眾多的 color 樣式中選出 red）
- 常用屬性
  - 文字、字體類
    - color: 字體顏色
    - font-size: 字體大小
    - font-family: 字體
    - letter-spacing: 字距
    - line-height: 行高 (字體高度的倍數)
  - Box 類的
    - padding: 內距
    - margin: 外距
    - width: 寬度
    - height: 長度
    - border: 外框

## References

- 學習資源: https://developer.mozilla.org/zh-TW/docs/Learn/Getting_started_with_the_web/CSS_basics
- Google 字型: https://fonts.google.com/