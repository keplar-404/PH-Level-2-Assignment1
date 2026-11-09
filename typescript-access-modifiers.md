# Access Modifiers in TypeScript OOP

## Introduction

Access modifiers are an important part of object-oriented programming in TypeScript. They control how class properties and methods can be accessed from different parts of an application. TypeScript provides three main access modifiers: `public`, `private` and `protected`. It also provides `readonly` to prevent properties from being reassigned.

### Types of Access Modifiers

**1. Public**

The `public` modifier allows properties and methods to be accessed from anywhere, including outside the class.

**2. Private**

The `private` modifier restricts access to the class where the property or method is declared. It cannot be accessed directly from outside the class or its subclass.

**3. Protected**

The `protected` modifier allows access within the declaring class and its subclasses. However, it cannot be accessed directly from outside the class.

**4. Readonly**

The `readonly` modifier prevents a property from being reassigned after initialization. It can be assigned when declared or inside the constructor.

Example:

```typescript
class Employee {
  public id: number;
  protected name: string;
  private salary: number;
  readonly department: string;

  constructor(id: number, name: string, salary: number, department: string) {
    this.id = id;
    this.name = name;
    this.salary = salary;
    this.department = department;
  }

  getSalary(): number {
    return this.salary;
  }
}

class Manager extends Employee {
  getName(): string {
    return this.name;
  }
}
```

In this example, `id` is publicly accessible, while `salary` is only accessible inside the Employee class. The Manager subclass can access `name` because it is protected. The department property cannot be reassigned because it is readonly.

## Conclusion

Access modifiers help developers control data access, organize classes, and build more maintainable TypeScript applications.
