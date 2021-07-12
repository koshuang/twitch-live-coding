# 2021-07-11 Twitch Streaming

Subject: [Coding] Refactoring Rage's code & Introduce Jest - TypeScript / React.js / Next.js / Monorepo

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

- Refactoring for https://github.com/koshuang/transform-object-keys-to-camel-case
- Jest
  - jest.config.js
    - notify
    - watch
  - expect functions
    - toBe
    - toEqual
    - ...

example

```js
describe("when toCamelCase is called with", () => {
  test("snake_to_c, it should return snakeToC", () => {
    // Todo: This one fails, do you want to fix it?
    const result = toCamelCase("snake_to_camelCase");

    expect(result).toStrictEqual("snakeToCamelCase");
  });

  test("snake_to_camelCase, it should return snakeToCamelCase", () => {
    // Todo: This one fails, do you want to fix it?
    const result = toCamelCase("snake_to_camelCase");

    expect(result).toStrictEqual("snakeToCamelCase");
  });

  test("snake_case, it should return snakeCase", () => {
    const result = toCamelCase("snake_case");

    expect(result).toStrictEqual("snakeCase");
  });

  test("snake_to_camel_case, it should return snakeToCamelCase", () => {
    // Todo: This one fails, do you want to fix it?
    const longTest = "this_is_a_very_long_snake_case_key"
    const result = toCamelCase(longTest);

    expect(result).toStrictEqual("thisIsAVeryLongSnakeCaseKey");
  });
})
```

## References














