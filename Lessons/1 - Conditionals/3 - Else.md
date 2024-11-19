# Unit 3 - Conditionals and Loops

## 3.3 - Else

##### ICS3 - Mr. Brash 🐿️

<table>
<tr>
<th>3.3 - In this Lesson:</th>
<th>Unit 3 - Conditionals & Loops</th>
</tr>
<tr>
<td td valign="top" style="height: 100px;padding-right:50px">

- [The `Else` Statement](#lesson)
- [Examples](#examples)
- [A Note about `prompt()`](#a-note-about-prompt)
- [Practice Time!](#practice-time)
    - [Part 1 - is_number](#part-1---is_number)
    - [Part 2 - Validate](#part-2---validate)
    - [Part 3 - Guess](#part-3---guess)
    
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

Here's the scenario: 
> You ask the user to select from a menu by entering a _number_ between 1 and 5.  
They don't select from the proper range or they enter a _word_. Perhaps they don't enter anything at all and just click OK.

❓ How would you handle that in code? 

---

### Lesson:

> **Recall:** An if-statement can only have _one_ `if` but several optional `else if` pieces.

So far, we know how to handle the _correct_ responses:

<table>
<tr>
<td width="60%">

```JS
if (selection == 1) {
    // Code here
} else if (selection == 2) {
    // Code here
} else if (selection == 3) {
    // Code here
}
```

</td>

<td>

**But what about all the other possibilities?**
</td>
</tr>
</table>

In the event that the `if` and `else if` statements do not find a true evaluation, `else` can handle _all other possibilities_. It's like saying "otherwise". **Note:** there can be only _one_ `else` and it needs to be at the end.


```JS
if (selection == 1) {
    // Code here
} else if (selection == 2) {
    // Code here
} else if (selection == 3) {
    // Code here
} else {
    alert("Invalid selection/input.");
}
```

<p style="text-align:center;font-size:larger;color:red">
This completes the <code>if-statement</code> package, creating a <b>powerful</b> tool!
</p>

---

### Examples

##### [Top ⬆](#33---else)

1. You need a given value to be even and positive _or_ below zero:
```JS
if ((value > 0) && (value % 2 == 0)) {
    return Math.sqrt(value);
} else if (value < 0) {
    return "Cannot take the square-root of a negative";
} else {
    return `${value} is neither even nor positive`;
}
```

2. You have a guessing game and the user needs to guess between 1 and 6:
```JS
// Is the input valid?
if (user_guess >= 1 && user_guess <= 6) {
    // The input is valid, check their guess
    if (user_guess == hidden_number) {
        alert("Correct! Congratulations!");
    } else {
        alert("Sorry, guess again.");
    }
} else {
    alert("Error. The guess has to be from 1-6.");
}
```

Do you understand the example above? Remember - `else if` is _optional_. 

---

### A Note About `prompt()`

##### [Top ⬆](#33---else)

> Ever wonder what happens if the user clicks "Cancel" on a prompt?

It actually returns `null`.

```JS
let menu_selection = prompt("Select 1 for Play...");

if (menu_selection == null) {
    // Deal with the user having clicked "Cancel"
}
```

---

### Practice Time!

##### [Top ⬆](#33---else)

#### Part 1 - `is_number()`

It can be really handy to have a function that tells you if a given value is a number or not. 

We can check that a value or variable is a real `'number'` by using `typeof`. This has been demonstrated in class in passing, but here's a reminder: `if (typeof my_variable == "number")` 

Create the function `is_number(num)` that will return `true` if `num` is, in fact, a real number and `false` otherwise.

#### Part 2 - Validate

##### [Top ⬆](#33---else)

Whenever a user interacts with our program(s), we need to validate that what they've done makes sense. This is particularly important if they're typing something in.

Let's validate part of a date. The day of the week.

Create the function `which_day(n)` which takes a **number** and _returns_ the **string** representation of the day of the week where 1 == "Sunday" and 7 == "Saturday".  

Here's how it will work:

1. The number will _not_ come from a prompt. It will be passed to the function when you call it - like this: `which_day(4)`  

2. First, check that the value coming in (`n`) is a number (convenient that you just created the `is_number()` function. If `n` not a number, _return_ "Invalid type".  

3. Next you will setup your code to _return_ the string representation of the day of the week ("Sunday", "Monday", "Tuesday", etc).

4. In all other cases, _return_ "Invalid value".


#### Part 3 - Guess!

##### [Top ⬆](#33---else)

In your [main.js](../../main.js) code file, you will see the `randInt()` function. It creates a random number from `min` to `max`.

1. Add a button to your [index.html](../../index.html) page that says "Guess 1-10"  
Reminder:  `<button id="guess">Guess 1-10</button>`

2. Add an event-listener in your [main.js](../../main.js) code file for the button to call the function `guess_10()` when the button is _clicked_.  
Reminder: `document.getElementById("guess").addEventListener("click", guess_10);`  

3. When the `guess_10()` function is called, it should do the following:
    1. Create a _hidden_ <u>random</u> number from 1 to 10 (inclusive)
    2. Ask the user (prompt) to select a number from 1 to 10.
    3. Compare their number to the hidden number.
        - If they have guessed the correct number, tell them.
        - If their guess was outside of the correct range (1-10), tell them this _and_ what the hidden number was.
        - If their guess was too low, tell them this _and_ the correct number.
        - If their guess was too high, tell them this _and_ the correct number.
        - For all other cases, tell the user there was an error.




<br><br>

🐿️