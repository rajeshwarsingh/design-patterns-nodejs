# design-patterns-nodejs

```markdown
# Node.js Design Patterns

This repository contains a collection of design patterns commonly used in Node.js applications. Each design pattern is explained with examples and code snippets to help in understand and implement them in the projects.

## Table of Contents

1. [Core Pattern](#singleton-pattern, #factory-pattern)
2. [Control Flow Patterns](#Avoiding Callback Hell, #Using Promises, #Using Async/Await, #Generators)
3. [Module Patterns](#Revealing-module-pattern, #dependencies-injection)
4. [Structural Patterns](#Proxy, #Adapter Pattern, #Decorator, #Composite)
5. [Behavioral Patterns](#Strategy, #Command, #Observers, #Middleware, #Template)
6. [messaging Patterns](#Request – Reply, #Publisher – Subscriber)

## Singleton Pattern
The Singleton pattern ensures that a class has only one instance and provides a global point of access to it.

```javascript
// Example implementation
class Singleton {
  constructor() {
    // ...
  }

  static getInstance() {
    if (!Singleton.instance) {
      Singleton.instance = new Singleton();
    }
    return Singleton.instance;
  }

  // ...
}
```

## Factory Pattern
The Factory pattern provides an interface for creating objects without specifying their concrete classes.

```javascript
// Example implementation
class Product {
  constructor() {
    // ...
  }

  // ...
}

class ConcreteProductA extends Product {
  constructor() {
    super();
    // ...
  }

  // ...
}

class ConcreteProductB extends Product {
  constructor() {
    super();
    // ...
  }

  // ...
}

class Factory {
  createProduct(type) {
    switch (type) {
      case 'A':
        return new ConcreteProductA();
      case 'B':
        return new ConcreteProductB();
      default:
        throw new Error('Invalid product type.');
    }
  }
}
```


