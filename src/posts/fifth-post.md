---
title: Inheritance in Javascript Classes
description: Object Oriented Programming.
date: "2023-7-15"
categories:
  - JavaScript
  - OOP
published: true
---

## Table of Contents

## Introduction:

In JavaScript, inheritance is a powerful concept that allows us to create new classes based on existing ones. It enables code reuse and promotes the organization of related functionalities. In this blog tutorial, we will dive into the world of class inheritance in JavaScript. We will explore how to extend classes, inherit properties and methods, and leverage the benefits of this object-oriented programming technique with practical code examples.

## Defining the Parent Class:

To begin with, let's define a parent class, also known as a superclass or base class, which will serve as the blueprint for our derived classes. Here's an example of a simple parent class called Animal:

```ts
class Animal {
  constructor(name) {
    this.name = name;
  }

  eat() {
    console.log(`${this.name} is eating.`);
  }

  sleep() {
    console.log(`${this.name} is sleeping.`);
  }
}
```

In the above code, the Animal class has a constructor that initializes the name property of each animal. It also defines two methods: eat() and sleep().

## Creating a Derived Class:

Now, let's create a derived class, also known as a subclass or child class, that inherits from the Animal class. We'll call it Dog:

```ts
class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }

  bark() {
    console.log(`${this.name} is barking.`);
  }
}
```

In the code snippet above, the Dog class extends the Animal class using the extends keyword. The super() function is called in the constructor to invoke the parent class constructor and pass the name argument. The Dog class also introduces its own property breed and a unique method bark().

## Creating Instances and Using Inherited Functionality:

Now that we have defined the parent and derived classes, let's create instances and observe the inheritance in action:

```ts
cconst cat = new Animal('Mittens');
cat.eat();   // Output: Mittens is eating.
cat.sleep(); // Output: Mittens is sleeping.

const goldenRetriever = new Dog('Buddy', 'Golden Retriever');
goldenRetriever.eat();   // Output: Buddy is eating.
goldenRetriever.sleep(); // Output: Buddy is sleeping.
goldenRetriever.bark();  // Output: Buddy is barking.

```

In the code above, we create an instance of the Animal class called cat and invoke the inherited methods eat() and sleep(). Then, we create an instance of the Dog class called goldenRetriever and observe how it inherits the properties and methods from the Animal class while also adding its own unique method bark().

## Conclusion:

Inheritance is a fundamental concept in JavaScript that enables code reuse and promotes modularity in object-oriented programming. By extending classes, we can create derived classes that inherit properties and methods from parent classes, while also introducing their own unique functionalities. In this blog tutorial, we explored how to define parent and derived classes, create instances, and leverage inherited functionality. With a solid understanding of inheritance, you can build more flexible and scalable JavaScript applications.
