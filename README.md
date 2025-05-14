# My TypeScript Blog

In this blog, I've written about two TypeScript topics. I've tried to explain them in a simple way.

---

## 1. What is Type Inference in TypeScript and Why Is It Helpful?

Type inference is a smart feature in TypeScript where it automatically guesses the type of a variable based on the value you give it. You don’t have to write the type yourself every time.

### Example:

```ts
let name = "John"; // TypeScript thinks it's a string
name = 123; // Error: Can't give a number to a string variable
```

In this example, TypeScript sees that `name` is a string. So if you try to change it to a number later, it will show an error.

### Why Is It Helpful?

* Makes code cleaner and easier.
* You don’t need to write types again and again.
* Still gives you the safety of static typing.

---

## 2. Using Union and Intersection Types in TypeScript

TypeScript lets you combine types using Union (`|`) and Intersection (`&`) types. These help make your code more flexible and reusable.

### Union Types (`|`)

Union types mean a value can be one type or another.

```ts
function printId(id: number | string) {
  console.log("ID:", id);
}

printId(101);
printId("abc123");
```

### Intersection Types (`&`)

Intersection types mean a value must match all the combined types.

```ts
interface Name {
  name: string;
}

interface Age {
  age: number;
}

type Person = Name & Age;

const user: Person = {
  name: "Alice",
  age: 30
};
```
