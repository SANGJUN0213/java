# java
const [first, second] = [10, 20];
console.log(first, second); 
const person = { name: 'Gyejin', age: 28 };
const { name, age } = person;
console.log(name, age);

const { name: newName = 'Unknown', age: newAge = 0 } = {};
console.log(newName, newAge); 

const combined = [...[1, 2], ...[3, 4]];
console.log(combined); 

const arr = [1, 2];
const newArr = [...arr, 3, 4];
console.log(newArr); 

function sum(...numbers) {
  return numbers.reduce((acc, cur) => acc + cur, 0);
}
console.log(sum(1, 2, 3, 4)); 

function printNumbers(first, ...rest) {
  console.log(first); 
  console.log(rest);  
}
printNumbers(1, 2, 3, 4);

export default function add(a, b) {
  return a + b;
}

import add from './math.js';
console.log(add(3, 5)); 

export function add(a, b) {
  return a + b;
}
export function subtract(a, b) {
  return a - b;
}

import { subtract as minus } from './math.js';
console.log(minus(10, 5)); // 5

async function dynamicImport() {
  const module = await import('./math.js');
  console.log(module.add(1, 2)); 
}
dynamicImport();

class Person {
  constructor(name) {
    this.name = name;
  }
  
  greet() {
    console.log(`Hello, ${this.name}`);
  }
}

const gyejin = new Person('홍길동');
gyejin.greet(); 

const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve('Success'), 1000);
});
promise.then(result => console.log(result)); 


const p1 = Promise.resolve(1);
const p2 = Promise.resolve(2);
Promise.all([p1, p2]).then(values => console.log(values)); 
function* generator() {
  yield 1;
  yield 2;
  return 3;
}
const gen = generator();
console.log(gen.next().value); 
console.log(gen.next().value); 
console.log(gen.next().value); 

const mySet = new Set([1, 2, 3, 3]);
console.log(mySet); 
const myMap = new Map();
myMap.set('key', 'value');
console.log(myMap.get('key')); 
