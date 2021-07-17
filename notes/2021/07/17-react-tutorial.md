# 2021-07-17 Twitch Streaming

Subject: [Teaching] React Basic Concept by using Create React App - TypeScript / React.js / Next.js / Monorepo

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

### Create React App (CRA)
- 變化較快
- 歷史演進
  - [JSX](https://zh-hant.reactjs.org/docs/introducing-jsx.html)
- 工具
  - 降低使用門檻
    - JSX、CSS etc.
  - 建立專案
    - https://zh-hant.reactjs.org/docs/create-a-new-react-app.html#create-react-app
    - `node -v`
    - `npm` vs `npx`
    - [[NodeJS] npx 是什麼? 跟 npm 差在哪?](https://medium.com/itsems-frontend/whats-npx-e83400efe7f8)
    - `npx create-react-app app-name`
![](https://i.imgur.com/rkhMUD7.png)
![](https://i.imgur.com/kyLqkED.png)
![](https://i.imgur.com/xkYmiJa.png)			
	- `yarn test`
	- what create react app do
	![](https://i.imgur.com/4tJOaCE.png)

- Syntax
  - { } = 動態
  - export = To let others to use something from the file
  - import = To use something from other files

- React component 的各種寫法
  - https://dev.to/chaituknag/creating-react-components-different-syntaxes-55o2 
    

- 常見錯誤
  - Invalid DOM property `class`. Did you mean `className`?
    - Reason: Class is a reserved keyword
    - Solution: Change 'class' to 'className'
  - JSX expressions must have one parent element.
    - Reason: JSX only accept one parent element
    - Solution: Wrap elements in one parent element
    - Example:
      - Multiple parent element: 
            `<p>First element</p>`
            `<p>Second element</p>`
      - One parent element:
            `<div>`
                `<p>First element</p>`
                `<p>Second element</p>`
             `</div>`

- 重要觀念
  - Question
    - Q: When does React render?
    - A: When state changed

    - Q: How to change state
    - A: Use the useState function from Basic Hooks
  - Functional component vs class 
    - Functional component
      - Trending in the market
      - Hooks
## References

[Create a New React App](https://reactjs.org/docs/create-a-new-react-app.html)










