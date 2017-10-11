# Primitive Data Types

JavaScript, like any other programming language, has built in data types. However, JavaScript is a loosely typed (or dynamic) language. This means that you won't need to declare your variable type; instead it will be determined while the code is being processed.

* Number
* Boolean
* String
* Null
* Undefined
* Symbol (new in ECMAScript 6)

You can find some more details on these types at [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures) and [w3schools](https://www.w3schools.com/js/js_datatypes.asp).

Other languages may include additional types, like...

* Floats

## Example Time!

### Numbers

A *number* is pretty self explanatory. We can do things like `5 + 5` with numbers and get a result of **10**.

JavaScript only has one type of number. You can write it with or without decimals.

```javascript
100 === 100.00
```

### Strings

A *string* is a collection of characters (single letters, numbers, symbols). You can create a string using double- or single-quotes.

```javascript
"Doctor Who";                       // Using double quotes
'Doctor Who';                       // Using single quotes
"Donna's an important person";      // Single quote inside double quotes
"They called her 'Doctor-Donna'";   // Single quotes inside double quotes
'They called her "Doctor-Donna"';   // Double quotes inside single quotes
```

Now what if we do this?

```javascript
1 + "2"
```

If you said the answer would be **3**, you're wrong. The result is actually **12**!

A string can't be added mathematically, so the `+` operator instead concatenates. It treats the `1` as a string instead of a number.

```javascript
"Hello" + "World"         // "HelloWorld"
"Hello" + " " + "World"   // "Hello World"
```

### Booleans

A *boolean* result has only two values: **true** or **false**. These can be used in conditional testing.

```javascript
100 > 200  // true  (100 is greater than 200)
100 < 200  // false (100 is less than 200)
2 == 2.0   // true  (2 equals 2.0)
2 != 3     // true  (2 does NOT equal 3)
2 == "2"   // true
2 === "2"  // false
```

Notice that `==` behaves differently from `===`. This is because `===` does NOT perform the type conversion.

```javascript
2 === "2"                  // false
typeof(2) === typeof("2")  // false
"number" === "string"      // false
```

### Checking Types

These code snippets that we've been writing are **expressions**. An **expression** will return a **value** and very value has a **type**.

```javascript
let x;
typeof(x);    // undefined

x = 999;
typeof(x);    // number

x = "Donna";
typeof(x);    // string
```

# Objects

An *object* is a collection of keys and values surrounded by curly brackets.

```javascript
{
  name:"Bree",
  species:"dog",
  size:"big",
};
```

# Arrays

An *array* is a collection of items separated by commas and surrounded by square brackets.

```javascript
["cat","dog","bunny"];
[1,2,3,4]
```

You can even create an array of objects!

```javascript
[
  {
    name: "Bree",
    species: "dog",
    size: "big",
    personality: "lovable",
    age: 5.5
  },
  {
    name:"Ziva",
    species:"cat",
    size:"small",
    personality: "adventurous, entitled"
    age: 6
  },
  {
    name:"Tesni",
    species:"cat",
    size:"small",
    personality: "aggressive cuddler",
    age: 6
  },
];
```

# GAME TIME!

Moderator go to [the game](https://play.kahoot.it/#/k/1f4c54c0-0e7e-4bda-90a6-1ab96b0d9a54) and project it on a large screen.

Players go to [kahoot.it](https://kahoot.it/) or open the app on your phone.
