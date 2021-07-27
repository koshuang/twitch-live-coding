# 2021-07-26 Twitch Streaming


> Subject: [Coding] use next-auth to do server side auth - TypeScript / React.js / Next.js / Monorepo

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

### redirect to login page if not logged in

> 方法一: 在 server side check

- 優點: UX 較好、速度較快
- 缺點: 程式共用較麻煩

如果要做 server side check 的話，那每一頁都需要使用 getServerSideProps ，會造成很多重複的 code。如果想避免的話，大概也只能把共用的邏輯寫到 HOC 


> 方法二: 在 client side check 

- 優點: UX 較不好、速度較慢
- 缺點: 程式共用較容易

follow the same way of `@next-auth/react-query` to use swr instead of react-query to do client side check, if it's not logged in, redirect to login page

## References

- Custom Login Page: https://next-auth.js.org/configuration/pages
- Redirect on getServerSideProps: https://nextjs.org/docs/basic-features/data-fetching#getserversideprops-server-side-rendering
- 3 ways to redirect user if not logged in: https://github.com/vercel/next.js/discussions/14945
- use client side to check auth: https://next-auth.js.org/getting-started/client#provider