# modulo operator in Javascript
The modulo operator, often denoted as %, is used to find the remainder of a division between two numbers.


## 1. Understanding the Modulo Operator

Defination :- The modulo operator `%` returns the remainder of the division of one number by another.

```javascript

a % b

```
`a` is the dividend (the number to be divided).
`b` is the divisor (the number by which `a` is divided).


eg :- 

```javascript

7 % 3 = 1

```
 7 divided by 3 is 2 with a `remainder` of 1.


## Rules and Properties of the Modulo Operator

1. if a is more and b is less return remainder

```javascript
//when we divide 13 by 2 then we will get 1
13 % 2 = 1

//when we divide 15 by 4 then we will get 3
15 % 4 = 3

```

2. if a is less then b (return a)

```javascript

//when we divide 5 by 7 then we will get 5 , because 7 is greater then 5
5 % 7 = 5

//when we divide 13 by 15 then we will get 13 
13 % 15 = 13

```

3. if a is negative value ( return the remainder with -ve sign)

```javascript

-13 % 5 = -3

```

4. if b is negative then return positiove (because sign is determined by a only)


```javascript

13 % -5 = 3

```

5. If both are negative (because it takes sign from a only)

```javascript

-13 % -5 = -3

```

6. If we have decimal value

```javascript

//a is less then b thts why returning a
4.5 % 5 = 4.45

//-5 * n is always negative that why returning a
4.5 % -5 = 4.5

//its not considering -ve sign and just doing normal mod and in result it is adding -ve sign

-4.5 % 4 = -0.5

```

When a is a decimal and b is positive, the result is a if a < b.



## Example


1. Determining Even or Odd Numbers

```javascript

function isEven(num) {
  return num % 2 === 0;
}

console.log(isEven(4)); // true
console.log(isEven(7)); // false

```

2. Circular Indexing


```javascript

const colors = ['red', 'green', 'blue'];
let index = 0;

function getNextColor() {
  const color = colors[index % colors.length];
  index++;
  return color;
}

console.log(getNextColor()); // 'red'
console.log(getNextColor()); // 'green'
console.log(getNextColor()); // 'blue'
console.log(getNextColor()); // 'red' (loops back to the beginning)

```

3. Clock Arithmetic

```javascript

function to12HourClock(hour24) {
  return (hour24 % 12) || 12; // Convert 0 to 12
}

console.log(to12HourClock(13)); // 1
console.log(to12HourClock(23)); // 11
console.log(to12HourClock(0));  // 12


```
4. Randomization

```javascript
function getRandomInRange(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(getRandomInRange(1, 10)); // Random number between 1 and 10
```


5. . Check if a Number is Divisible by Another Number

```javascript
function isDivisibleBy5(num) {
  return num % 5 === 0;
}

console.log(isDivisibleBy5(10)); // true
console.log(isDivisibleBy5(7));  // false

```

6. Calculate the Remainder

```javascript
let dividend = 29;
let divisor = 5;
let remainder = dividend % divisor;

console.log(`The remainder of ${dividend} divided by ${divisor} is ${remainder}.`); // 4
```
7. Determine the Day of the Week

```javascritp

function dayOfWeek(dayNumber) {
  const daysOfWeek = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
  return daysOfWeek[dayNumber % 7];
}

console.log(dayOfWeek(1));   // 'Monday'
console.log(dayOfWeek(8));   // 'Monday' (cycling through the week)
console.log(dayOfWeek(15));  // 'Monday'

```

8. find the sum of all the digits of a number

```javascript

function sumOfDigits(number) {
  // Convert number to string and split into individual characters
  const digits = number.toString().split('');
  
  // Use reduce to sum up the digits after converting them to numbers
  const sum = digits.reduce((accumulator, digit) => accumulator + Number(digit), 0);
  
  return sum;
}

const number = 1456;
console.log(`The sum of the digits of ${number} is ${sumOfDigits(number)}.`); // 16

```

```javascript

function sumOfDigits(number) {
  let sum = 0;
  
  // Ensure the number is positive
  number = Math.abs(number);

  while (number > 0) {
    // Extract the last digit
    const digit = number % 10;
    
    // Add the digit to the sum
    sum += digit;
    
    // Remove the last digit from the number
    number = Math.floor(number / 10);
  }
  
  return sum;
}

const number = 1456;
console.log(`The sum of the digits of ${number} is ${sumOfDigits(number)}.`); // 16

```






























