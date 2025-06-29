# Level 00 A

## What is Computer Science?

Why is this field of study called "Computer Science" and not "Program Writing" or "Code Mathematics"? It's because coding requires research and experimentation! You'll often need to test your programs to learn from unexpected errors, then make changes to get the results you want.

These lessons will teach you how to code in Java as part of the AP Computer Science A curriculum. You will have to memorize some vocabulary, grammar, and syntax to learn this new language. However, learning to code isn't what programming is all about, you will also learn how to think like a programmer!

## What is QuintOS?

Issac Newton, a famous 17th century scientist, once said, "we stand on the shoulders of giants". Newton was humbly acknowledging that great advancements made by people in his day were built upon a giant foundation laid by our ancestors.

To become a software developer today it's good to learn a bit about the history of computers and computer games.

QuintOS contains a set of retro computer simulations. During each lesson you'll develop a game or program that runs on a virtual computer displayed in the Google Chrome web browser. As you level up your coding skills, the virtual computer will get upgraded too. Since you're just starting out, the first program you make will be for... a programmable calculator. 😜

This first lesson will require you to learn a lot of information before we can even make a simple game. It may be a bit overwhelming for you but don't worry! You'll get a lot of practice with these concepts so that you will fully understand them. Let's get started! 🥳

## Creating Variables 🔡

First of all, what is a variable? Variables in Java store data in your computer's memory.

```java
int a = 0;
```

In the example code `a` is the names of the variable. `a` is assigned the number `0`. `int` is used to create the variable and specifies what type of variable it is.

In Java a semicolon `;` must be used to end each line of code. 👁👅👁

## Types of Variables 🔡

To create a variable in Java, you must specify the type of data it stores.

### Numbers

```java
int x = 2;
float y = -49.8;
double z = 9504.159392000393888;
```

`int` (integer) is for whole numbers. `float` (floating point) is for decimal numbers. `double` should be used when a higher degree of precision is needed for decimal numbers. All of these types of numbers can be positive or negative.

### Boolean

Booleans are either `true` or `false`

```java
boolean codingIsFun = true;
```

### Character

```java
char letter = 'a';
```

The variable `letter` stores the single character `a`.

### String

Strings are text, contained within "quotes".

```java
String story = "The dog went to the dog park on 3rd Avenue.";
```

ERROR! If you don't use quotes, Java will think the words are variables!

```java
String story = The dog went to the dog park on 3rd Avenue.;
```

To remember that the data type for text is called String, you can think of lettered beads on a charm bracelet string.

### functions

functions are a reference to other sections of code which you can run using `()` parenthesis. Input parameters to a function go in the parenthesis.

```java
powerOn();
turn("left");
moveForward(10);
turn("right");
moveForward(2);
```

This code for a robot remote control makes the robot power on, turn left, move forward ten steps, turn right, and then move forward two steps. Note that functions can do different things depending on their input values!

## Globals 🌐

Globals are special variables that are already available for you to use anywhere in your code.

### System

`System` is an important global variable. Use `System.out.println()` to display text to the user. Usually this would make text appear in the standard output (just a list of any text printed out) but with QuintOS the text will appear on a virtual computer in an alert window.

### Scanner

Scanner can be used for user interaction with `System.in` for user input.

```java
// create a new Scanner of the system input
Scanner sc = new Scanner(System.in);

// waits for the user to type something and press enter
// the user's response to the prompt is assigned to favColor
System.out.println("What's your favorite color?");
String favColor = sc.nextLine();

System.out.println(favColor + " is my favorite color too!");
```

With QuintOS, printing to the console using `System.out` and then using a Scanner object to get user input will cause a prompt window to appear on the virtual computer's screen.

## Comments

Double slash `//` is for making a comment, any text behind it on the same line will not be considered part of the code's instructions. Comments are used to describe what is happening in the code. You might want to make comments so other people can understand your programs or so that you can understand it yourself in case you forget what you did.

## End of Level 00 A

Now you're ready to start making your first game! 🥳 [Click here for the GuessTheNumber instructions.](https://github.com/quintos-org/IntroToJava/blob/main/Level_00/GuessTheNumber.md)

# Level 00 B

Did you complete `GuessTheNumber` part A and are ready to learn more? Before we can finish the game we have to learn a bit more stuff!

## Camel Case 🐫

Variables in Java can't have spaces, 🙅‍♂️ so for variables that have multiple words, use camel case! Capitalize the first letter of the words after the first word.

```java
String apple = "🍎";
String applePie = "🍎 π";
String applePieIceCream = "🍎 π 🍨";
```

Note that using this naming convention isn't required for Java to run, it's just something that most professional Java programmers do to make variable names easier to read. Camel case is a naming convention specific to Java, other programming languages have their own conventions.

## if/else statements

`if` statements use a boolean condition, which goes in parenthesis after the keyword `if`. If the boolean condition is `true`, the code block `{}`, whatever's inside the squiggly brackets, is run.

Check out this coin toss example code. Coin tosses are used in many sports to decide which of two teams goes first. One team picks which side of the coin they think will land facing up, "heads" or "tails". Hypothetically, the `coinFlip` function performs a coin flip and returns true if the result of the coin flip was what the user picked. The code in the `if` statement code block will be run. If the result was "tails", then the code in the `else` block is run.

```java
System.out.println("Heads or Tails?");
String pick = sc.nextLine();

if (coinFlip(pick)) {
	System.out.println("You won the coin toss!");
} else {
	System.out.println("You lost the coin toss!");
}
```

## Checking Equivalence ✅

Single equals `=` is for assigning values to variables. Double equals `==` is a boolean operator used for checking equivalence. What is a boolean operator? It performs an operation that results in either a true or false (boolean) value.

## else if chaining

`else if` can be used after if statements, they form a chain of different paths the code can take if the previous if statements were false.

Take a look at the example below which assigns the name of the coin to the variable `coin` based on the value of `value`.

```java
System.out.println("What's the value of your lucky coin?");
double value = sc.next();

String coin; // variables can be created without a value assigned to them

if (value == 1.00) {
  coin = "Dollar";
} else if (value == 0.50) {
  coin = "Half-Dollar";
} else if (value == 0.25) {
  coin = "Quarter";
} else if (value == 0.10) {
  coin = "Dime";
} else if (value == 0.05) {
  coin = "Nickel";
} else if (value == 0.01) {
  coin = "Penny";
} else {
  coin = "Unknown";
}

System.out.println("Your lucky coin is a " + coin + " and has a value of " + value);
```

## Boolean operators 🐰

```txt
Equivalence:              ==
Less than:                <
Less than or equal to:    <=
Greater than:             >
Greater than or equal to: >=
```

Boolean operations evaluate to either true or false. Use them in the boolean conditions (inside the parenthesis) of `if` and `else if` statements.

# Level 00 C

## Changing a variable's value

Don't create variables twice!

```java
int x = 10;
int x = 5; // ERROR! x already exists
```

Here's how to change the value of the variable `x`

```java
int x = 10;
x = 5; // good :)
```

## Code Execution Order

Note that you can not use a variable before you create it. You will get an error saying the variable is not defined, meaning that Java doesn't have a variable with that name in its memory.

```java
System.out.println(message); // ERROR: message is not defined
String message = "Hi!";
```

Create variables before you use them.

```java
String message = "Hi!";
System.out.println(message); // good!
```

## Scopes

Note that if you declare a variable in a code block it will only be available from the beginning to the end of the block. This is the scope of a variable. The code block/scope begins with this opening squiggly bracket (aka curly brace) `{` and ends with a closing squiggly bracket `}`

```java
if (orderNumber == 163) {
	String message = orderNumber + " your order is ready!";
}

System.out.println(message); // ERROR: message is not defined
```

Fix this by initializing `message` outside of the if statement.

```java
String message;
if (orderNumber == 163) {
	message = orderNumber + " your order is ready!";
}

System.out.println(message); // good!
```

## while loops

Need to loop some code? Use a while loop! `if` statements run the code in their code block once if their boolean condition is true. `while` loops repeat the code in their code block as long as their boolean condition remains true.

Take a look at the following example. Imagine that the `pickACard` function returns a String with the name of the card taken from the top of the deck, such as "Two of Hearts" or "Nine of Clubs".

```java
String card; // no card picked yet

while (!card.equals("Ace of Spades")) {
	card = pickACard();
}

System.out.println("Found the Ace of Spades!");
```

# Level 00 D

## Mathematical operators 🔢

```txt
Addition:       +
Subtraction:    -
Multiplication: *
Division:       /
```

The multiplication symbol is the asterisk, NOT the letter `x`!

```java
int x = 5 * 8; // x -> 40
```

## Math functions

At this point you should also know about the global Class [Math](https://docs.oracle.com/en/java/javase/15/docs/api/java.base/java/lang/Math.html), which has many useful functions. You will use `.random()` and `.ceil()` to make this game.

```java
// Math.random() returns a random decimal number between 0 and 1 (not including 1)
// note that this function does not accept input parameters!
double x = Math.random(); // x could be .2364 or .928279 or 0.45398, it's random!

double a = Math.round(30.1); // -> 30
double b = Math.round(30.7); // -> 31
// Math.round() rounds the number to the nearest integer

double y = Math.floor(22.9); // y -> 22 (y gets assigned the value 22)
// Math.floor() always rounds down

double z = Math.ceil(15.3); // z -> 16
// Math.ceil() always rounds up (ceil for ceiling)

// casting to int forces a decimal number to become an int
// drops the decimal (effectively rounding down)
int castedValue = (int) (39.8); // casted -> 39
```

## Computer History: Casio FX-720P

This level's computer was inspired by the Casio FX-720P, released in 1986, which could run programs in a programming language called BASIC. Portable programmable calculators were limited by their small button keyboards and displays, but when slotted into a dock that had little printer, they could be used to print out graphs and many lines of text. The calculator could also load programs from tape cassettes.

<https://youtu.be/d3NIe1jTZMc?t=760>

- [Level 00 A](#level-00-a)
  - [What is Computer Science?](#what-is-computer-science)
  - [What is QuintOS?](#what-is-quintos)
  - [Creating Variables 🔡](#creating-variables-)
  - [Types of Variables 🔡](#types-of-variables-)
    - [Numbers](#numbers)
    - [Boolean](#boolean)
    - [Character](#character)
    - [String](#string)
    - [functions](#functions)
  - [Globals 🌐](#globals-)
    - [System](#system)
    - [Scanner](#scanner)
  - [Comments](#comments)
  - [End of Level 00 A](#end-of-level-00-a)
- [Level 00 B](#level-00-b)
  - [Camel Case 🐫](#camel-case-)
  - [if/else statements](#ifelse-statements)
  - [Checking Equivalence ✅](#checking-equivalence-)
  - [else if chaining](#else-if-chaining)
  - [Boolean operators 🐰](#boolean-operators-)
- [Level 00 C](#level-00-c)
  - [Changing a variable's value](#changing-a-variables-value)
  - [Code Execution Order](#code-execution-order)
  - [Scopes](#scopes)
  - [while loops](#while-loops)
- [Level 00 D](#level-00-d)
  - [Mathematical operators 🔢](#mathematical-operators-)
  - [Math functions](#math-functions)
  - [Computer History: Casio FX-720P](#computer-history-casio-fx-720p)
