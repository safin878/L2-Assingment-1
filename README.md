## 🎯 TypeScript for Beginners: Interfaces vs Types & What the Heck is `keyof`?

If you’re just diving into TypeScript, you might be scratching your head over some of its features. Trust me, I’ve been there. Two things that confused me at first were the difference between `interface` and `type`, and what `keyof` is even used for. So in this blog, I’ll break these down in plain English (and a bit of code, of course).

---

### 💡 Interfaces vs Types in TypeScript — What's the Difference?

At first glance, `interface` and `type` seem to do the same thing — they both let you define the shape of an object.

Here’s a simple example:

 <pre>
// Using interface
interface User {
  name: string;
  age: number;
}

// Using type
type UserType = {
  name: string;
  age: number;
};
</pre>


## 🔑 What is the use of the `keyof` keyword in TypeScript?

In TypeScript, the `keyof` keyword is used to **get all the property names (keys)** of an object **as a union type**.

---

### 📌 Basic Example

```ts
type User = {
  name: string;
  age: number;
};

type UserKeys = keyof User;
// Result: "name" | "age"
