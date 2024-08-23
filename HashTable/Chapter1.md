## 1. How do you use an object as a hash table in JavaScript?

Answer: In JavaScript, objects can be used as hash tables where the keys are strings (or symbols) and the values can be of any type. You can store, retrieve, and delete key-value pairs using the following syntax:

```javascript

let hashTable = {};

// Setting a value
hashTable['key1'] = 'value1';

// Getting a value
console.log(hashTable['key1']); // 'value1'

// Deleting a key
delete hashTable['key1'];

```
## 2. What are the limitations of using an object as a hash table in JavaScript?

1. Prototype Inheritance: Objects in JavaScript inherit properties from their prototype. This means that an object might have keys like `toString`, `valueOf`, etc., which could potentially conflict with your own keys.

2. Key Type: The keys in a JavaScript object are always strings or symbols. If you need to use other types (e.g., numbers or objects) as keys, they will be converted to strings.

3. No Direct Control over Hashing: JavaScript does not provide direct control over how keys are hashed, which might lead to performance issues if many keys hash to the same value.



## 3. How can you avoid key collisions when using an object as a hash table?

1. Use Unique Strings: Ensure that your keys are unique and not likely to overlap with existing object properties or methods.
2. Use Symbols: If you want to guarantee that your keys won’t collide with any other properties, use `Symbol` for keys:

```javascript

let uniqueKey = Symbol('key');
let hashTable = {};
hashTable[uniqueKey] = 'value';

```












