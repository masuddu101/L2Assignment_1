# any, unknown and never in TypeScript

## Introduction

TypeScript has a type hierarchy. At the top there are two types, `any` and `unknown`, which can hold every kind of value. At the bottom there is `never`, which holds no value at all. Let us understand each of them in a simple way.

## The Three Types

The `any` type turns off type checking. You can do anything with it, even wrong things, and TypeScript will not complain.

```ts
let a: any = "hello";
a.toFixed(); // no error, but crashes at runtime
```

The `unknown` type also accepts every value, but it is safe. Before using it, you must check its type.

```ts
let u: unknown = "hello";
if (typeof u === "string") {
  console.log(u.toUpperCase());
}
```

The `never` type is used for things that never happen, like a function that always throws an error.

```ts
function fail(message: string): never {
  throw new Error(message);
}
```

## Why unknown is Better than any

With `any`, mistakes hide until the program runs. With `unknown`, TypeScript forces us to check first, so bugs are caught early.

## Conclusion

Use `unknown` when you do not know the type, and avoid `any`. Use `never` for impossible cases. This keeps your code safe and easy to trust.