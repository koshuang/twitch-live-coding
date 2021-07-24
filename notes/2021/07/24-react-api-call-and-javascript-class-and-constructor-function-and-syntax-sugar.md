# 2021-07-24 Twitch Streaming

> Subject: [Teach] Basic React Concept - TypeScript / React.js / Next.js / Monorepo

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

- Teach
  - How to create your own github website
  - Basic React Concept

## React
### Revision
- `export` : to export module from current file (so can be used in other files)
- `import` : to import module from other files and use it
- `useState` : React render only when the state changed

### New Item
- `useEffect`
- [React Component Syntax](https://dev.to/chaituknag/creating-react-components-different-syntaxes-55o2)
  - Recommended way to write function
    - Arrow function statement
```javascript=
const Component = () => {
  return <h1>Hello World</h1>
}
```
- Class Component
```typescript=
class User {
    name: string;
    
    constructor(name: string) {
    this.name = name;
    }
    
    sayHi(){
    console.log(`Hi ${this.name}`);
    }
}
const user = new User('Kos') // instance
```
- Constructor function
```javascript=
function Car() {
    this.name = 'Kos Car';
    this.printcar = () => {
        console.log(`Your car is ${this.name}`);
    }
}
const car = new Car(); // instance
```

### 一串葡萄法
- 把程式碼模組化
- 做法：A import B -> B import C, so A can use whats in C
- 例子：


```
src
  modules
    app
      App.js
        before
        import { MoodReaction } from '../mood/components/MoodReaction';
        after 一串葡萄
        import { MoodReaction } from '../mood';
    mood
      index.js
      components
        index.js
        MoodReaction.jsx
```

### Call API 的方式

- XMLHttpRequest
```javascript=
var xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
       // Typical action to be performed when the document is ready:
       document.getElementById("demo").innerHTML = xhttp.responseText;
    }
};
xhttp.open("GET", "filename", true);
xhttp.send();
```
- jQuery ajax: 底層其實是 `XMLHttpRequest`
```javascript=
$.ajax({
  accepts: {
    mycustomtype: 'application/x-some-custom-type'
  },
 
  // Instructions for how to deserialize a `mycustomtype`
  converters: {
    'text mycustomtype': function(result) {
      // Do Stuff
      return newresult;
    }
  },
 
  // Expect a `mycustomtype` back from server
  dataType: 'mycustomtype'
});
```
- HTML5: fetch
```javascript=
fetch('./api/some.json')
  .then(
    function(response) {
        // 判斷status
      if (response.status !== 200) {
        console.log('Looks like there was a problem. Status Code: ' +
          response.status);
        return;
      }

      // Examine the text in the response
      response.json().then(function(data) {
        console.log(data);
      });
    }
  )
  .catch(function(err) {
    console.log('Fetch Error :-S', err); // string template
  });
```

## JavaScript 知識

### Syntax Sugar for `&&` and `||`

```js
function showFalsyValues() {
    // falsy values
    console.log(Boolean(null));
    console.log(Boolean(undefined));
    console.log(Boolean(''));
    console.log(Boolean(0));

    // truthy
    console.log(Boolean('false')); 
    console.log(Boolean([]));

    // 小技巧
    // console.log(params.debug === 'true'); // http://localhost:3000/debug=false
}

const handsome = false;
const isKos = true;

// 第一個變數是 faslsy value ，就會被回傳第一個變數
const isKosHandsome = handsome && isKos; 

// 第一個變數是 truthy value ，就會被回傳第一個變數
// 第一個變數是 falsy value ，就會被回傳第二個變數
const isKosOrHandsome = handsome || isKos; 

// console.log(isKosHandsome);


// const user = {
//     name: 'Kos',
// };

let user;

// null point check
let userName = user && user.name;

// console.log(userName);


// default value
userName = userName || 'KK';

console.log(userName);
```


### class and function constructor 寫法

```typescript
// class syntax is a sugar syntax
class User {
    name: string;

    constructor(name: string) {
        this.name = name;
    }

    sayHi() {
        console.log(`Hi ${this.name}`);
    }
}

const user = new User('Kos'); // instance

// console.log(user);
// user.sayHi();


// 一般的 function 寫法
function printCar() {
    console.log('Car');
}

// printCar();

const name = '123';

// Constructor function
function Car() {
    this.name = 'Kos Car';

    this.printCar = () => {
        console.log(`Your car is ${this.name}`);
    }
}

const car = new Car(); // instance

// console.log(car);
car.printCar();
```

## Git Command
- `git diff` 
  - "-" = Removed data from files
  - "+" = Added data to files
- `git add`
- `git commit`
  - Without -m, will get into VIM, press 'I' to change to Edit mode
    - eg: refactor(component): [App] extract a new component 
    - Meaning: *Category of action (to which item): [Module Name] Details of what you have done*



## How to create your own github website

### Why does Github want to make public usage

- 認同 Open Source 的好處
- 提高認知度，讓用戶接觸並熟悉

### Create Page from Existing Repository
- Link to access: *username*.github.io/*repo-name*
- Steps:
  - Go to the repo
  - Create new branch: `git checkout -b 'gh-pages'`
    - Note: The branch name must be **gh-pages**
  - Commit changes
  - Push to Github

## Linux Shell Command
`>`= Write into
  - Example
    - Write something to new file: `echo "Hi Everyone" > file.txt`
    - Print something in a file to another file: `cat file.txt > secondFile.txt`

`>>` = Append into (file etc)
  - Example: 
    - Append content to a file: `echo "How are you?" >> file.txt`



## References

[Create Github Website](https://pages.github.com/)