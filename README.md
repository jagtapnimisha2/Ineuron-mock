# Ineuron-mock
Mock test 25 june 2023

question.    

Implement a stack using an array in JavaScript. Include the necessary methods such as push, pop, and isEmpty.


code.  
class Stack {
  constructor() {
    this.items = []; // Array to store stack elements
  }

  // Add an element to the stack
  push(element) {
    this.items.push(element);
  }

  // Remove the top element from the stack
  pop() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items.pop();
  }

  // Check if the stack is empty
  isEmpty() {
    return this.items.length === 0;
  }

  // Get the top element of the stack without removing it
  peek() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items[this.items.length - 1];
  }

  // Get the size of the stack
  size() {
    return this.items.length;
  }

  // Clear the stack
  clear() {
    this.items = [];
  }
}

// Usage example:
const stack = new Stack();

stack.push(10);
stack.push(20);
stack.push(30);

console.log(stack.size()); // Output: 3

console.log(stack.pop()); // Output: 30

console.log(stack.peek()); // Output: 20

console.log(stack.isEmpty()); // Output: false

stack.clear();

console.log(stack.isEmpty()); // Output: true
