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



















