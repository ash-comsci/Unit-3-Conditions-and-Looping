# Unit 3 - Conditionals and Loops

## 3.6 - Do While

##### ICS3 - Mr. Brash 🐿️

<table>
<tr>
<th>3.6 - In this Lesson:</th>
<th>Unit 3 - Conditionals & Loops</th>
</tr>
<tr>
<td td valign="top" style="height: 100px;padding-right:50px">

- Lesson: [Do...While](#lesson)
- [Examples](#more-examples)
- [Practice Time!](#practice-time)
  - [print_odd(n)](#print_oddn)
  - [negative_only()](#negative_only)
  - [parrot()](#parrot)
  - [factorial(n)](#factorialn)
    
</td>
<td td valign="top" style="height: 100px;padding-right:50px">

- [README](../../README.md)
- [3.1 - If](../1%20-%20Conditionals/1%20-%20IF.md)
- [3.2 - Else-If](../1%20-%20Conditionals/2%20-%20Else-If.md)
- [3.3 - Else](../1%20-%20Conditionals/3%20-%20Else.md)
- [3.4 - While](./4%20-%20While.md)
- [3.5 - Interlude: `Strings`](./5%20-%20Interlude_Strings.md)
- [3.6 - Do...While](./6%20-%20Do-While.md)
- [3.7 - For](./7%20-%20For.md)

</td></tr></table>



## Lesson:

### Recall the While Loop:

The _While_ loop might _never_ run...
```JS
let raining = false;

while (raining) {
  console.log("It's raining, I need an umbrella.");
}

// The loop above will not run. Not even once.
```
Sometimes we _want_ the loop to run _at least once_. For example, when getting input from the user.<br>That's where the **[do...while loop](https://www.w3schools.com/jsref/jsref_dowhile.asp)** can help:
```JS
let input;

do {
  input = +prompt("Please enter a number from 1 to 5");
} while ((isNaN(input)) || (input < 1) || (input > 5));

// The loop above will run at least once
```

- Notice that the _condition_ is at the _end_ of the code block for a **[do...while](https://www.w3schools.com/jsref/jsref_dowhile.asp)**. Conversely, the [while](https://www.w3schools.com/jsref/jsref_while.asp) loop has the condition _at the beginning_.
- It is up to the _developer_ to pick the correct loop. Sometimes a _while_ is better, sometimes a _do while_ is better... 

**Here's another example:**
```JS
do {
  console.log("It's raining! I need an umbrella.");
} while (raining);
```

The above will _always_ print "It's raining! I need an umbrella." at _least_ once. This might not be ideal.

<br>

<div style="text-align:center;"><img src="https://gist.github.com/assets/25152375/a6abb15d-6ef2-4dcb-aa53-34fe95427725" width="350px"></div>

## More Examples

###### [⬆ Top](#36---do-while)

Sometimes you need to use a 'counter' to control the loop. Remember to always *modify* the counter each loop to avoid an infinite scenario!
```JS
// Print "Hi" the given number of times (at least once)
function printHi(num) {
  do  {
    console.log("Hi");
    num--;  
  } while (num > 0);
}
```
Other times you might use a random number, a string, or input to control the loop. It is important to **declare the condition variable outside of the loop**:
```JS
// Ask the user for a number and validate their input
function getNumber() {
  let input;
  do {
    input = Number(prompt("Please enter a number:"));
  } while (isNaN(input));

  return input;
}
```

Here's another example with the variables declared _before_ the loop:
```JS
// Build a string from user input
function build_string() {
  let output = "";
  let input;
  do {
    input = prompt("Enter a string of text or a single 'q' to quit: ");
    output += input;
  
  } while (input.toLowerCase() != "q");

  return output;
}
```

### 🤔
- Why are the variables `input` and `output` declared _outside_ of the loop?
- There is a small bug in the `build_string()` function - can you figure it out?

## Practice Time!

###### [⬆ Top](#36---do-while)

Now it's your turn to practice. The list of functions below is in _no particular order_. Pick what you want to work on based on your own abilities. Having difficulty? There are so many ways to get help!

### `print_odd(n)`

###### [⬆ Top](#36---do-while)

Given some number, `n`, as a parameter to the function, print the _odd_ numbers from 1 to `n`. If `n` is less than 1 or _not a number_, nothing should print.  
**For Example:**
```JS
print_odd(7);
// Prints:
1
3
5
7

print_odd(-7);
// Nothing is printed

print_odd("s'up?");
// Nothing is printed
```

### `negative_only()`

###### [⬆ Top](#36---do-while)

Write the function `negativeOnly()` that asks the user for _a negative number_ and _keeps asking for one_ as long as they enter something _other_ than a negative value. If a negative number is entered, the function ends and returns the negative value they entered.

### `parrot()`

###### [⬆ Top](#36---do-while)

Prompt the user to enter some text _or_ the word 'quit'.
  - If the input is not _**quit**_ print their input back out to them in all caps and then prompt them again.
  - If the input is any variation of **quit**, print "GOODBYE! 🦜" and the program ends.  
  **Example:**
  ```text
  parrot();
  
  [prompt]"Please enter some text or the word 'quit' to exit:" Hello!
  HELLO!

  [prompt]"Please enter some text or the word 'quit' to exit:" I wish to quit
  I WISH TO QUIT

  [prompt]"Please enter some text or the word 'quit' to exit:" QuIt
  GOODBYE! 🦜
  ```


### `factorial(n)`

###### [⬆ Top](#36---do-while)

In mathematics, the *factorial* of a number is written like this:<br> n! = n x (n-1) x (n-2) x (n-3) x ... x 2 x 1

For example, 5! = 5 x 4 x 3 x 2 x 1 = 120

Write the function `factorial(n)` that calculates and *returns* the factorial of the given number.  

**Fun fact:** you can only take the factorial of positive whole values and the factorial of zero is one (`0! == 1`).

**For Example:**
  ```JS
  factorial(5);
  120
  factorial(3);
  6
  factorial(10);
  3628800
  factorial(0);
  1
  ```

<br><br>

🐿️

