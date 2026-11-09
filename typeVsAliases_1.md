# Type Alias vs Interface in TypeScript

## Introduction

In TypeScript, we often need to describe the shape of an object. We can do this with a type alias or with an interface. They look very similar, but they are not exactly the same. Let us learn the core differences in a simple way.

## Differences

An interface is mainly used to describe objects and classes. It can be extended using the `extends` keyword. It can also be declared twice with the same name, and TypeScript will merge both into one.

```ts
interface User {
  name: string;
}
interface User {
  age: number;
}
```

A type alias is more flexible. It can give a name to a union, a tuple, or a simple type like a string. An interface cannot do this.

```ts
type Id = string | number;
```

A type alias can be combined with the `&` symbol, but it cannot be declared twice with the same name. TypeScript will show an error if you try.

## When to Choose Which

Use an interface when you describe an object or a class, because it is simple and easy to extend. Use a type alias when you need a union, a tuple, or another special shape.

## Conclusion

Both type and interface are useful tools in TypeScript. Choose interface for object shapes and type alias for everything else. If you follow this simple rule, your code will stay clean and easy to read.