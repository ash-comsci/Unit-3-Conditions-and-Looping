# More Conditionals and Looping Practice

##### ICS3 - Mr. J 🐧

❔ Are you fully caught up on `while`, `do while` and `for` loops? Looking for more practice? Try some of the following...

- Skip to [a REALLY hard challenge](#looking-for-a-really-hard-challenge)

### Try these challenges out (no particular order):

- `count_char(str, char)`<br>
  Write the function `count(str, char)` - given the string `str` count _how many times_ `char` is found in the string and return that number. If you never find the character, return -1.  
  **For Example:**
  ```JS
  > count_char("Mr. Squirrel", "r");
  3
  > count_char("Mr. Squirrel", ".");
  1
  > count_char("Mr. Squirrel", "s");
  -1
  ```
  
###### [⬆ Top](#more-conditionals-and-looping-practice)

- `print_codes(str)` - print the character codes of the given string, each on a new line.  
**For Example:**
  ```JS
  > print_codes("What codes?")
  87
  104
  97
  116
  32
  99
  111
  100
  101
  115
  63
  ```
  
###### [⬆ Top](#more-conditionals-and-looping-practice)

- `determine_case(c)` - All uppercase letters are character codes 65-90 (inclusive) and lowercase letters are character codes 97-122 (inclusive). The digits 0 to 9 are codes 48-57 (inclusive). Everything else is considered a "special" character. Determine _and return_ whether a given character, `c`, is uppercase "U", lowercase "L", a number "N", or special "S". Assume `c` is a single character.  
**For Example:**
  ```JS
  > determine_case("k")
  "L"
  > determine_case("G")
  "U"
  > determine_case("&")
  "S"
  > determine_case("7")
  "N"
  ```  

###### [⬆ Top](#more-conditionals-and-looping-practice)

- `print_case(str)` - Given a string, `str`, create a return a _new_ string that replaces all uppercase letters with "U", lowercase letters with "L", numbers with "N", and special characters with "S". If you wrote the `determine_case(c)` function, above, you should use it to help.  
**For Example:**
  ```JS
  > print_case("Mr. Squirrel - what a HAM!")
  "ULSSULLLLLLLSSSLLLLSLSUUUS"
  ```
  
###### [⬆ Top](#more-conditionals-and-looping-practice)

- `tail(str, n)` - return the last `n` characters of the given string `str`. If `n` is negative, a non-number, or too large, return -1. _You are not permitted to use any built-in functions similar to `.subtring()` or `.slice()`, etc..._  
**For Example:**  
  ```JS
  > tail("This is the end!", 4)
  "end!"
  > tail("What?", 1)
  "?"
  > tail("Hello", 15)
  -1
  > tail("Goodbye", -9)
  -1
  ```
  
###### [⬆ Top](#more-conditionals-and-looping-practice)

- `print_line(char, width)` that _prints_ a single line of `char`'s of length `width`. _You will use a for-loop to accomplish this_.  
**For Example:**
  ```JS
  > print_line("H", 5)
  HHHHH
  > print_line("🤯", 10)
  🤯🤯🤯🤯🤯🤯🤯🤯🤯🤯
  > print_line("👻", 3)
  👻👻👻
  ```
  
###### [⬆ Top](#more-conditionals-and-looping-practice)

- `print_rectangle(char, height, width)` that _prints_ a rectangle of `char`'s with the given `height` and `width`. You could use your `print_line()` function from above to help (if you wrote it).  
**Example:**
  ```JS
  > print_rectangle("@", 4, 6)
  @@@@@@
  @@@@@@
  @@@@@@
  @@@@@@
  ```
  

###### [⬆ Top](#more-conditionals-and-looping-practice)
- `fib_sequence(n)` - **Read this one _carefully_, especially the return format**. The [Fibonacci Sequence](https://www.mathsisfun.com/numbers/fibonacci-sequence.html) is a series of numbers. **The first two numbers are 0 and 1**. The next numbers are found by adding up the two numbers before.

  For example: 0, 1, 1, 2, 3, 5, 8, 13, 21. The next number in this series is 13+21 = 34.

  Write the function `fib_sequence(n)` that returns a _**String**_ containing `n` values of the Fibonacci Sequence. Each value in the return String is separated by a comma and a space `", "`<br><br>**For Example:** `fib_sequence(5)` returns the string `"0, 1, 1, 2, 3"` meanwhile `fib_sequence(11)` returns the string `"0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55"`. If the parameter `n` is a non-number or is a value less than 0, return the string "-1".

  <br>



### Looking for a REALLY hard challenge?

###### [⬆ Top](#more-conditionals-and-looping-practice)

- `squirrel_crypt(str)`<br>
  Mr. Squirrel has developed an [encryption algorithm](https://en.wikipedia.org/wiki/Encryption) that he's pretty sure nobody has every used before. It's so good that it can _encrypt_ **and** _decrypt_ a message when you use it.
  - Each letter is replaced with its reflective partner in the alphabet (A becomes Z, B becomes Y, M becomes N, O becomes L, S becomes H, etc). Huge hint - M and N are the middle of the alphabet.
  - Each letter is changed from UPPERcase to lowercase and from lowercase to UPPERcase
  - Spaces " " are replaced with commas "," and commas are replaced with spaces
  - All other special characters are left alone
  - The string is _reversed_  (Hello <> olleH)
  - The new string is returned!
  <br>**Examples:**
    ```JS
    squirrel_crypt("Here's a simple test.");
    // returns:  .GHVG,VOKNRH,Z,H'VIVs

    squirrel_crypt(".GHVG,VOKNRH,Z,H'VIVs");
    // returns:  Here's a simple test.

    squirrel_crypt("The FBI agent's CSIS friend doesn't believe in UFO's!");
    // returns:  !H'luf,MR,VEVROVY,G'MHVLW,WMVRIU,hrhx,H'GMVTZ,ryu,VSg
    
    squirrel_crypt("!H'luf,MR,VEVROVY,G'MHVLW,WMVRIU,hrhx,H'GMVTZ,ryu,VSg");
    // returns:  The FBI agent's CSIS friend doesn't believe in UFO's!
    ```
<br><br>
🐧
