# Conditionals

By implementing **control flow** we can run bits of code only under certain circumstances.

If/Else statements, also called "conditionals", are the most common way to control flow. These statements allow us to run a bit of code only *if* a certain condition is met.

```javascript
const answer = prompt("What is the name of Harry Potter's red-headed friend?");

if(answer === "Ron"){
  alert("Woohoo! You're right!")
}
```

 We can additionally add an *else* option to run if that condition is not met.

 ```javascript
 let answer1 = prompt("What is the name of Harry Potter's red-headed friend?");

 if(answer1 === "Ron"){
   alert("Woohoo! You're right!");
 } else {
   alert("Bummer. You should sit down and do some reading.");
 }
 ```

Or we can have additional checks.

```javascript
let answer2 = prompt("What is the name of one of Harry Potter's friends?");

if( answer2 === "Ron" ){
  alert("Woohoo! You're right!");
} else if ( answer2 === "Hermoine" ) {
  alert("Great job!");
} else {
  alert("Bummer. You should sit down and do some reading.");
}
```

## Switch

https://www.w3schools.com/js/js_switch.asp

# Let's Play!

## FizzBuzz

1. Generate a random number between 0 and 5
2. If it's divisible by 3, alert "fizz"
3. If it's divisible by 5, alert "buzz"
4. Otherwise print the number to the console.
