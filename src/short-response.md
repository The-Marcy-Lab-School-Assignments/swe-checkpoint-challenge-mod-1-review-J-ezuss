# Short Responses

For this assessment, aim to write a response with the following qualities:

- [ ] Addresses all parts of the prompt
- [ ] Accurately uses relevant technical terminology
- [ ] Is free of grammar and spelling mistakes
- [ ] Is easy to comprehend

For each prompt below, write your response in the space provided. Aim to answer each prompt in 2-5 concise sentences. Make sure to preview your markdown to check how it is rendered before submitting.

## Prompt 1

Consider the code below which has a bug. Instead of printing the correct letter grade, it always prints `"Your grade is: undefined"`.

```js
const getLetterGrade = (score) => {
  let letter;
  if (score >= 90) {
    let letter = 'A';
  } else if (score >= 80) {
    let letter = 'B';
  } else if (score >= 70) {
    let letter = 'C';
  } else {
    let letter = 'F';
  }

  return 'Your grade is: ' + letter;
};

console.log(getLetterGrade(95)); // This should print "Your grade is: A"
console.log(getLetterGrade(82)); // This should print "Your grade is: B"
console.log(getLetterGrade(74)); // This should print "Your grade is: C"
console.log(getLetterGrade(65)); // This should print "Your grade is: F"
```

**Part A**: Explain why this bug is occurring. Use proper technical terminology.

**Part B**: Then, explain how you would fix it.

### Response 1

**Part A:**

Your response...
this bug is occurring because we are using `let` inside of the if and else statements instead of returning `letter` therefore resulting in the `undefined` output
**Part B:**

Your response...
How I would fix this would be to change all the `let` inside all the if else statements and writing the `return` keyword instead.

---

## Prompt 2

Read the following code:

```js
const originalSettings = { volume: 50, brightness: 80 };
const newSettings = originalSettings;
newSettings.volume = 75;
console.log(originalSettings.volume);
```

**Part A:** What will be logged to the console? Why does this happen? Be sure to use precise technical terminology in your answer.

**Part B:** How would you modify the code so that changing `newSettings.volume` does NOT affect `originalSettings.volume`? Write the corrected code below your explanation.

### Response 2

**Part A:**

Your response...
What will be logged is 75 because
**Part B:**

Your response...
correct me if I'm wrong but what I would do is make a new array using the spread syntax an example would be

```js
const originalSettings = { volume: 50, brightness: 80 };
const newSettings = {...originalSettings};// line 83
newSettings.volume = 75;
console.log(originalSettings.volume);
**Corrected Code:**
```

basically what I did was on line 83 I used the spread syntax to make a new array in order to not affect the `originalSettings.volume`.

```js
// Fix this code so newSettings is a true copy
const originalSettings = { volume: 50, brightness: 80 };
const newSettings = originalSettings;
newSettings.volume = 75;
console.log(originalSettings.volume);
```

---

## Prompt 3

Given this array of products and the code using `filter`:

```js
const products = [
  { name: 'Laptop', price: 1000, inStock: true },
  { name: 'Phone', price: 700, inStock: false },
  { name: 'Watch', price: 300, inStock: true },
  { name: 'Tablet', price: 500, inStock: true },
];

const itemsInStock = products.filter((product) => {
  return product.inStock;
});
```

Walk through what happens in the first iteration of filter:

- What is the value of `product`?
- What gets returned from the callback?
- What happens with that returned value?

### Response 3

Your response...
The value of product is

What gets returned from the callback is the products that are `inStock` and wether it's true or false.

when the value is returned you will get wether the product is in stock or not in a true or false statement and it will just show you the products that are in stock only
