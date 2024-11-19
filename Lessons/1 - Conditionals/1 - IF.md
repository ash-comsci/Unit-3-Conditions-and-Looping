# Unit 3 - Conditionals and Loops

## 3.1: If-Statements

##### ICS3 - Mr. Brash 🐿️

<table>
<tr>
<th>
3.1 - In this Lesson:
</th>
<th>
Unit 3 - Conditionals & Loops
</th>
</tr>
<tr>
<td td valign="top" style="height: 100px;padding-right:50px">
<ul>
<li><a href="#lesson">If-Statement Syntax</a></li>
<li><a href="#examples">Examples</a></li>
<li><a href="#logical-operators">Logical Operators</a></li>
<li><a href="#practice-time">Practice Time!</a></li>
<ul>
<li><a href="#part-1">Part 1</a></li>
<li><a href="#part-2">Part 2</a></li>
<li><a href="#part-3">Part 3</a></li>
<li><a href="#part-4">Part 4</a></li>
</ul>
</ul>
</td>
<td td valign="top" style="height: 100px;padding-right:50px">

- [README](../../README.md)
- [3.1 - If](./1%20-%20IF.md)
- [3.2 - Else-If](./2%20-%20Else-If.md)
- [3.3 - Else](./3%20-%20Else.md)
- [3.4 - While](../2%20-%20Loops/4%20-%20While.md)
- [3.5 - Interlude: `Strings`](../2%20-%20Loops/5%20-%20Interlude_Strings.md)
- [3.6 - Do...While](../2%20-%20Loops/6%20-%20Do-While.md)
- [3.7 - For](../2%20-%20Loops/7%20-%20For.md)

</td></tr></table>

---

### Lesson:


Mom says:
> "I will let you go to the mall _**if**_ you vacuum your room."

This is a _conditional_ statement. `Visit the mall` depends on `vacuum your room`.

The same can be accomplished in code with an `if-statement`:  
```js
if (vacuum == true) {
    let money = ask_mom_for_cash(40);
    go_to_the_mall(money);
}
```

The example above is silly but it is the JavaScript syntax for a condtional statement that allows you to run code _only if something is true_.

```JS
// Conditional (if-statement)
if (condition_is_true) {
    // As much code as you want
}
```

### Examples:

##### [Top ⬆](#31-if-statements)

```JS
/* 
A function that takes two numbers and if they are negatives of each other, return "Negatives", if they aren't return "Not Negatives"
*/
function take_two(a, b) {
    
    if (a == -1*b) {
        return "Negatives";
    }

    return "Not Negatives";
}


// Use the logical "AND" operator && to see if multiple things are true
function check_game(game_running, lives) {

    if (game_running == true && lives == 0) {
        // Update the screen
        display("Game Over!");

        // Stop the game
        game_running = false;

        // Return -1 because the game is over
        return -1;
    }

    // Return 0 because the game is still going
    return 0;
}

// Use the logical "OR" operator || to see if at least one thing is true
function snow_day(snow, temperature, buses_running) {

    if (snow >= 20 || temperature < -35 || buses_running == false) {
        return "SNOW DAY!!!";
    }
    
    return "Not a snow day...";
}
```

### Logical Operators

##### [Top ⬆](#31-if-statements)

Did you see the **double**-equal sign? `==`

- A *single* equal sign is the *assignment* operator:  `x = 5` ***makes*** `x` the number 5.
- A *double* equal sign is the *check* operator to ask the question "Is it true"?

| Operator | Meaning | Example |
| :---: | :---: | :---: |
| = |**Assignment**|`let name = "Mr. Squirrel"`|
| == | **Is Equal**<br>Returns `true` or `false` | `name == "Mr. Squirrel"`|
| != | **Is NOT Equal**<br>Returns `true` or `false` | `name != "Mr. Brash"` |
| >| **Is Greater**<br>Returns `true` or `false` | `x > 10` |
| >= | **Is Greater or Equal**<br>Returns `true` or `false` | `x >= 10` |
| <| **Is Less Than**<br>Returns `true` or `false` | `Math.PI < 10` |
| <=| **Is Less Than or Equal**<br>Returns `true` or `false` | `Math.PI <= 3.15` |

<br>

## Practice Time!

Use the [main.js](../../main.js) file to write your code.

### Part 1

##### [Top ⬆](#31-if-statements)

This will all be one function, run from the dev console:

- Create the function `user()` that takes _no_ parameters but does the following:  

    - Ask the user for their age using the [`prompt()`](https://www.w3schools.com/jsref/met_win_prompt.asp) function.
    - Don't forget that keyboard input is a *String*, not a number, so [you'll have to convert it](https://www.sitepoint.com/convert-string-to-number-javascript/#:~:text=The%20unary%20plus%20(%2B)%20operator,a%20number%2C%20it%20returns%20NaN.).
    - **if** they are 60 years old _or older_, print to the console "You qualify for the senior discount!"
    - **if** they are _younger_ than 16, print "You're not old enough to drive yet."
    - **if** they are 44, print "So is Mr. Squirrel!"  
    (Please note - these are all separate if-statements)

    - Now ask the user for their **name** and store the answer in a variable called `user_name`
    - if the `user_name` is "Mr. Squirrel" print the squirrel emoji: "🐿️"
    - if the `user_name` is longer than 7 characters print "You have a long name."
        - **You can read how to get the length of a string [here](https://flexiple.com/javascript/javascript-string-length)**.

    - Now ask the user how long they think their name is (how many characters)
    - If the number they enter **matches** the length of `user_name` print "That's correct! ✔️"
    - If the number they enter is *higher* than the length of the name, print "Too high ✖️"
    - If the number they enter is *lower* than the length of the name, print "Too low ✖️"


### Part 2:

##### [Top ⬆](#31-if-statements)

We've seen the basic math operators `+`, `-`, `*`, `/` but there are more. One **important** one is the *modulo* operator `%`. This gives the *remainder* of a division statement.

**For Example:**
```JS
let x = 5 % 2
console.log(x)   // The output will be 1

x = 19 % 5
console.log(x)   // The output will be 4

x = 20 % 2
console.log(x)   // The output will be 0
```

We can use *modulo* to determine if a value is `even` or `odd` by checking the remainder when dividing by 2.

- Determine if the user's age is an `even` or `odd` number and print that to the screen.<br>
For Example:  "Your age is an even number."  or  "Your age is an odd number."

### Part 3:

##### [Top ⬆](#31-if-statements)

Create the function `longer_string(str1, str2)` which _returns the longer of the two strings_.  
**For example:**  `longer_string("Happy", "Birthday")` returns "Birthday"

> 🤔 What should you return if they're both the same length?

### Part 4:

##### [Top ⬆](#31-if-statements)

Create the function `discriminant(a, b, c)` which _returns how many zeros the quadratic will have based on the values of `a`, `b`, and `c`_. This requires your knowledge of [the descriminant](https://www.khanacademy.org/math/algebra-home/alg-quadratics/alg-solving-quadratics-using-the-quadratic-formula/a/discriminant-review) from grade 10 math.

<br><br>

🐿️
