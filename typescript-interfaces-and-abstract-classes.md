# TypeScript Exercises: Interfaces & Abstract Classes

### Exercise 01 — Interface Speaker
```typescript
interface Speaker {
  speak(): void;
}

class Person implements Speaker {
  speak() {
    console.log("Hello, I can speak!");
  }
}

const p = new Person();
p.speak();
```
Exercise 02 — Interface Greeter

```typescript
interface Greeter {
  greet(): void;
}

class Student implements Greeter {
  greet() {
    console.log("Hi, I'm a student");
  }
}

class Teacher implements Greeter {
  greet() {
    console.log("Hello, I'm a teacher");
  }
}

const s = new Student();
const t = new Teacher();

s.greet();
t.greet();
```
Exercise 03 — Interface Animal + função

interface Animal {
  makeSound(): void;
}

class Dog implements Animal {
  makeSound() {
    console.log("Woof!");
  }
}

class Cat implements Animal {
  makeSound() {
    console.log("Meow!");
  }
}

function playSound(animal: Animal) {
  animal.makeSound();
}

const dog = new Dog();
const cat = new Cat();

playSound(dog);
playSound(cat);

Exercise 04 — Abstract class


abstract class Vehicle {
  move() {
    console.log("The vehicle is moving");
  }

  abstract makeNoise(): void;
}

class Car extends Vehicle {
  makeNoise() {
    console.log("Vroom vroom!");
  }
}

const car = new Car();
car.move();
car.makeNoise();

Exercise 05 — Abstract class 

abstract class Employee {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  clockIn() {
    console.log(`${this.name} clocked in`);
  }

  abstract work(): void;
}

class Developer extends Employee {
  work() {
    console.log(`${this.name} is writing code`);
  }
}

const dev = new Developer("Alex");

dev.clockIn();
dev.work();