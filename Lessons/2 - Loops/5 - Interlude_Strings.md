# Unit 3 - Conditionals and Loops

## 3.5 - Interlude: `Strings`

##### ICS3 - Mr. Brash 🐿️

<table>
<tr>
<th>3.5 - In this Lesson:</th>
<th>Unit 3 - Conditionals & Loops</th>
</tr>
<tr>
<td td valign="top" style="height: 100px;padding-right:50px">

- Lesson - [Remember Strings?](#lesson---remember-strings)
- [Examples](#examples)
- [Practice Time!](#practice-time)

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

---

### Lesson - Remember Strings?

A single letter is called a **character** (`char` for short).

Each character is a symbol (drawing) tracked by a number in the computer's memory. The computer looks-up the symbol, based on that number.
- [ASCII Characters](https://ss64.com/ascii.html)
- [Unicode Characters](https://en.wikipedia.org/wiki/List_of_Unicode_characters)

Multiple characters together is called a `String` of characters. Like a string of Christmas lights.

<img src="../images/string_of_lights.png" width="400px">

- Ex: The word hello is a string made of the chars `'h' 'e' 'l' 'l' 'o'`.
- Strings have a `.length` that returns the _number of characters in the string_.
- Each `char` has a **position** or **index**.
  - The left-most or first `char` is at **position zero** [0].
  - To get a character in the string we can use the shortcut `[#]` where "#" is an address or index of the character.
    - Ex:  `"Hello"[1]` is the character "e" and `"Mr. Squirrel"[2]` is the character "."
    - Also works on variables:
    ```JS
    let my_string = "Strings are powerful!";
    let one_char = my_string[my_string.length - 1];
    console.log(one_char);
    ```
    🤔 What will print in the example above?
- It is very important to remember that "a" and "A" are considered *different*. `"Hello" != "hello"`
- **Note**: JavaScript treats single letters as a `String` with length 1, not a `char`.

**Recall:** We can "build" a `String` using the _concatonate_ feature of the `+` operator:
```JS
let my_output = "";
let t = "third";

my_output += "First" + " " + "second" + t;

return my_output;    // returns "First secondthird"
```

That will become very handy later.

## New Information

###### [⬆ Top](#35---interlude-strings)

A _property_ is a fact about an object.
- _Strings_ have a very important property that we've seen before: `.length`
  ```JS
  let myString = "Hello World!";
  console.log(myString.length);   // Prints 12 to the screen
  ```

A _function_ - also known as a _method_ - is something that an object can _do_ to manipulate data or give a result.

- Strings have [lots of useful functions](https://www.w3schools.com/js/js_string_methods.asp) but the ones we might focus on are:  
  - `.toUpperCase()` and `.toLowerCase()`  
  - `.charCodeAt()`  
  - `.substring()`  
... and _many more_, with [awesome examples at w3schools](https://www.w3schools.com/js/js_string_methods.asp)!

- Another very useful tool is the ability to get a _character_ based on its [numeric code](https://ss64.com/ascii.html). For that we use `String.fromCharCode()` and give the Unicode number.
  ```JS
  let my_char = String.fromCharCode(64);   // the @ character
  console.log(my_char);  // @
  ```

## Examples

###### [⬆ Top](#35---interlude-strings)

**Don't forget!** To get a single character from the string we can use `var.charAt(index)` **or the easier shortcut of `var[index]`.**

Now that we know while loops, we can *loop* through a string and print one character at a time!
```JS
let longText = "Supercalifragilisticexpialidocious";
let current_letter = 0;

while (current_letter < longText.length) {
  console.log(longText[current_letter]);
  current_letter++;
}
```

We can also _**build**_ a String, if necessary:

**Simple Example:**
```js
// duplicate the string as many times as requested
function duplicate(str, number_of_times) {
  let output = "";    // Empty string for building
  let n = 1;

  while (n <= number_of_times) {
    output += str;
    n++;
  }

  return output;
}

// What will repeated_string be if we call this:
let repeated_string = duplicate("Yay Code!", 100);
```

**Slightly More Complicated Example:**
```JS
// Build a new string that does not have any spaces
let output = "";
let sample_text = "This is a typical sentence.";
let n = 0;
// The character code for a space is 32
const SPACE = 32

while (n < sample_text.length) {
  if (sample_text.charCodeAt(n) != SPACE) {
    output += sample_text[n];
  }
  n++;
}

console.log(output);    // Thisisatypicalsentence.
```

## Practice Time!

###### [⬆ Top](#35---interlude-strings)

Try creating the following functions:
- `print_reverse(str)` _Print_ the reverse of the given string to the console.
  <br>Examples:
  ```JS
  print_reverse("Hello");
  "olleH"
  print_reverse("Coding's great!");
  "!taerg s'gnidoC"
  ```

- `dragons_and_goblins(str)`
  For this function a string of random letters (`str`) is passed in (for example `dragons_and_goblins("dbhfghfgdbchdnwjdg")`). Your job is to count how many dragons ("d") and goblins ("g") are encountered. _Print_ the result to the console as shown in the examples below:
  ```JS
  dragons_and_goblins("dbhfghfgdbchdnwjdg");
  "Dragons: 4 Goblins: 3"
  dragons_and_goblins("pgoggl45j6ng jk*&j3 h^gg%h");
  "Dragons: 0 Goblins: 6"
  ```

- `add(str)` You will be given a string of _all_ single-digit numbers. Add them up and _return_ the result.
  <br>Examples:
  ```JS
  console.log(add("9350701"));
  25
  console.log(add("11111111112222255"));
  30
  ```
- `add_subtract(str)` The same as the `add()` function (add single digits) _except_ if you encounter a "-" symbol, the next single digit value is _subtracted_ from the total. _Return_ the result.
  <br>Example:
  ```JS
  console.log(add_subtract("543-36-9"));
  6
  console.log(add_subtract("0-102-53-3-1-5"));
  -10
  ```

## Extra Practice

Don't like the above tasks or maybe they were too easy? Here's a few more to try:

- `substring(mainstring, start, stop)`  
  - The `substring()` function extracts characters from start to end (exclusive) from the `mainstring` String.
  - The `substring()` function does not change the original String.
  - If `start` is greater than `stop`, arguments are swapped: (4, 1) = (1, 4).
  - `start` or `stop` values less than 0, are treated as 0.  

  **Example:**
  ```JS
  let sub = substring("ABCDEFGHIJKLMNOPQRSTUVWXYZ", 6, 11);
  // sub == "GHIJK"
  ```
- `fix_pronoun(str)`  
Pronouns are supposed to start with a single capital letter and be followed with all lowercase letters (with some exceptions but we'll ignore the exceptions for this).
  - The `fix_pronoun(str)` function will _assume_ the provided string is a single word.
  - This function returns the given string with the first letter capitalized (uppercase) and all other letters lowercase.  

  **Examples:**
  ```JS
  console.log(fix_pronoun("gabriel"));
  "Gabriel"

  console.log(fix_pronoun("HAM SanDWiCh!"));
  "Ham sandwich!"
  ```

<br><br>
🐿️
