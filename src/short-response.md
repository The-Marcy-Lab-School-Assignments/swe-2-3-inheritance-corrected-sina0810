# Short Responses

For this short response assignment, aim to write a response with the following qualities (your instructor will give you feedback on these areas):
- [] Addresses all parts of the prompt
- [] Accurately uses relevant technical terminology
- [] Is free of grammar and spelling mistakes (double check with grammarly!)
- [] Uses markdown to enhance readability (preview in VS Code with Command/Control + Shift + V)
- [] Is easy to comprehend

For each prompt below, write your response in the space provided. Aim to answer each prompt in 2-5 concise sentences. Make sure to preview your markdown to check how it is rendered before submitting.

## Prompt 1

In your own words, define what **inheritance** is in object-oriented programming. Then, explain what benefits it provides to developers who use it. Consider what problem it solves — what would be harder or messier without inheritance?

## Response 1

- **inheritance** is when a subclass gets access to the methods and properties of another class by using extends on the subclass.
- The benefits of using **inheritance** are that it prevents repeating code and keeps the code organized.
- It would’ve been harder without it because we would have to repeat the code for each class, which would be very confusing and harder to understand.
- But with **inheritance**, it becomes easy because the subclass can simply extend the parent class to reuse its functionality.
---

## Prompt 2

Consider these classes:

```js
class Animal {
  eat() { return "eating"; }
}

class Dog extends Animal {
  bark() { return "woof"; }
}

class Puppy extends Dog {
  play() { return "playing"; }
}

const rex = new Puppy();
```

Explain what happens when `rex.eat()` is invoked. In your answer, describe the role of **inheritance** and the **prototype chain**.

## Response 2
- If we were to invoke `console.log(rex.eat())` then we would invoked `eating` to the console. That is because we are calling the parent class of **Animal**
- Also, the prototype of **Puppy** has been extended from the **Dog** class and **Dog** class is a subclass of **Animal** class.
- We have a method called `eat()` that returns *eating* when that method is invoked. 

--- 

## Prompt 3

Look at these classes:

```js
class Employee {
  constructor(name, salary) {
    this.name = name;
    this.salary = salary;
  }
  getDetails() {
    return `${this.name} earns $${this.salary}`;
  }
}

class Manager extends Employee {
  constructor(name, salary, department) {
    // YOUR CODE HERE
    super(name, salary)
    this.department = department
  }
  getDetails() {
    // YOUR CODE HERE - should include both the Employee details 
    // AND the department info
    return `${super.getDetails} works at ${this.department}`
  }
}
```

Complete the `Manager` class by filling in the `constructor` and `getDetails` methods. Explain why you need to use `super` in each method and what would happen if you didn't use it.

## Response 3

- We need to refer to `super` method because **Employee** is an extension from **Manager** class, otherwise we can't use the properties or the methods that are invoked in the **Manager** class. 
- If we didn't use it there, we would've gotten a *ReferenceError*. 