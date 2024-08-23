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
3. Check for Existing Properties: Before adding a new key, you can check if the key already exists to avoid overwriting.


## 4. What are the differences between using an object and a `Map` as a hash table in JavaScript?

1. Key Types: `Map` allows keys of any type (objects, functions, etc.), whereas object keys are strings or symbols.
2. Iteration Order: In a `Map`, keys are iterated in the order they were added. In an object, the iteration order is more complex, often depending on whether the keys are integer-like or strings.

3. Built-in Methods: `Map` has methods like `set`, `get`, `has`, and `delete`, making it more versatile for certain use cases. Objects don’t have these built-in methods, and you must use operators like `in` or `delete`.
4. Prototype Pollution: `Map` doesn’t have inherited properties like objects do, so there’s no risk of key conflicts with inherited properties

## How do you safely check if a key exists in an object used as a hash table?

1. Use the `in` operator

```javascript
let hashTable = { key1: 'value1' };
console.log('key1' in hashTable); // true

```

2. Alternatively, use `Object.hasOwnProperty()` to check if a property exists directly on the object and not on its prototype chain:

```javascript

console.log(hashTable.hasOwnProperty('key1')); // true

```

3. In modern JavaScript, you can also use `Object.hasOwn()`:

```javascript

console.log(Object.hasOwn(hashTable, 'key1')); // true

```

## 6. Can you use an object as a hash table with non-string keys in JavaScript?
Answer: In JavaScript objects, non-string keys are automatically converted to strings. For instance, if you use a number or an object as a key, it will be converted to a string:

```javascript

let hashTable = {};
hashTable[1] = 'value1';      // Key is '1' (string)
hashTable[{a: 1}] = 'value2'; // Key is '[object Object]' (string)

```
If you need to use non-string keys (e.g., objects), a `Map` would be a better choice because it preserves the original type of the key.


## 7. What is the significance of the `__proto__` property when using objects as hash tables?

Answer: The `__proto__` property is part of an object’s prototype chain. If you accidentally use `__proto__` as a key, it might lead to unexpected behavior because it can modify the prototype of the object, potentially causing issues with property inheritance and lookup:

```javascript

let hashTable = {};
hashTable['__proto__'] = 'someValue';

console.log(hashTable.__proto__); // Still points to Object.prototype, not 'someValue'

```
To avoid this, you can use `Object.create(null)` to create an object without a prototype:


```javascript

let hashTable = Object.create(null);
hashTable['__proto__'] = 'someValue';

console.log(hashTable.__proto__); // 'someValue'

```



























