# 📘 TypeScript Concepts Blog

This repository explores two advanced TypeScript topics:

1. Use of `keyof` keyword
2. Differences between `any`, `unknown`, and `never` types

---

## 🔑 1. Understanding the `keyof` Keyword

The `keyof` keyword returns a union of all property names of a given type.

### ✅ Example:

```ts
interface Person {
  name: string;
  age: number;
}
type PersonKeys = keyof Person; // "name" | "age"
