# 2021-07-31 Twitch Streaming


> Subject: [Teach] Basic React Concept - React.js

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## React
### Revision
- Functional component, use UseState to change the state
  - cont [stateVariable, function] = useState(預設值)
    - `cont [visible, setVisible] = useState(false)`
    - let visible = false;
    - function setVisible(v) {visible = v}

- falsy value , truthy value

- useEffect
  - useEffect(function,array)
    - `useEffect(() => { callAPI();}, [])`
  - The block within useEffect will only run once (during the first render)
  - effect = side effect (I/O, Network related, including Call API, console log)

## Agenda

### Homework

- 使用 CRA 產生一個 React Project (react-todolist)
- 建立 Github repository
- 建立一個 Todos 的 Component
  - 使用 Todos API: https://jsonplaceholder.typicode.com/todos
  - 頁面上要顯示前三筆 Todo 的 title (分三行)
    - 預設顯示 `No Data`


## References

> API Call Example

```js
function callAPI() {
  const url = 'https://jsonplaceholder.typicode.com/todos/1';

  return fetch(url)
    .then(
      function(response) {
        if (response.status !== 200) {
          console.log('Looks like there was a problem. Status Code: ' +
            response.status);
          return;
        }

        // Examine the text in the response
        return response.json().then(function(data) {
          console.log('response data', data.title);

          return data;
        });
      }
    )
    .catch(function(err) {
      console.log('Fetch Error :-S', err);
    });
}
```

> useEffect() Example

```js
// 裡面的 block 只會在第一次 render 的時候執行
  useEffect(() => {
    callAPI()
      .then((data) => {
        console.log('#### sresponse data', data.title);
        setTitle(data.title);
      });
  }, []);
```