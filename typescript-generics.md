# Generics in TypeScript

## Introduction

Generics are placeholders for data types. Instead of defining a function for a specific data type, generics allow the same function to work with different types while maintaining type safety.

### How Generics Work

Generics use type parameters. Commonly represented by `<T>`. The type parameter acts as a placeholder that TypeScript replaces with the actual type when the function is called.

Example:

```typescript
function getFirstItem<T>(items: T[]): T {
  return items[0];
}

const firstName = getFirstItem<string>(["Rakib", "Sadia"]);
const firstNumber = getFirstItem<number>([10, 20, 30]);
```

In this example the same function works with both strings and numbers. TypeScript automatically understands the return type based on the input type.

Generics can also be used with asynchronous operations. A Promise uses a generic type to describe the value it will return when successfully resolved.

```typescript
async function getUser(): Promise<string> {
  return "Rakib";
}
```

Here, `Promise<string>` indicates that the Promise resolves with a string value.

## Conclusion

Generics make TypeScript applications more flexible, reusable, and type safe. They are especially useful when building reusable functions, working with collections and handling asynchronous operations.
