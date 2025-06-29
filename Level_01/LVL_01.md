# Level 01 A

Congratulations, you completed level 0! 🥳

Before you can work on the next game, let's get you setup so you can write Java on your own computer without having to only use CodePen, which an online code editor.

## Requirements for Offline Development

- install Google Chrome (Firefox, Edge, and Opera are good too, just don't use Safari)
- install [node.js](https://nodejs.org/en/) (includes [npm](https://www.npmjs.com/))
- Windows users need to install [Git](https://gitforwindows.org/)
- macOS users need to use the command `xcode-select --install` in Terminal
- install the [Visual Studio Code editor](https://code.visualstudio.com/)

## Setup

Open the [quintos-template](https://github.com/quintos-org/quintos-template) project on Github. Press the big green button that says "Use this template". Name your project "quintos-projects".

Now open the Git Bash app on Windows or the Terminal app on macOS and copy/paste these commands one line at a time. Replace `!!!your username!!!` with your GitHub username.

```sh
cd ~/Documents
git clone https://github.com/quintos-org/IntroToJava.git
git clone https://github.com/!!!your username!!!/quintos-projects.git
cd quintos-projects
npm i
npm i java2js
```

Don't worry I'm not hacking your computer! The first command `cd`, changes directory (aka folder), which opens your Documents folder inside the terminal (you can choose a different folder if you'd like). The second command downloads my teaching curriculum "IntroToJava". The third command downloads your "quintos-projects" project. The fourth command changes directory into your "quintos-projects" folder. The last command, `npm i`, installs "QuintOS".

Open Visual Studio Code (aka VSCode) and add "IntroToJava" and your "quintos-projects" folder to the workspace.

## Install Extensions for VSCode

In the Activity Bar on the left side of VSCode click the extension icon, which looks like one box being separated from three other boxes. In the Extension sidebar, search for and install Prettier, Live Server, and Language Support for Java.

Prettier is an extension that will automatically format your code for you when you save it so you won't have to worry about doing proper indentation and formatting yourself!

Live Server auto-refreshes the browser when you make changes to your code.

Language Support for Java is a set of extensions from Red Hat. Use them to also install a recommended JDK (Java Development Kit).

## VSCode Settings

Press F1 on your keyboard (hold Fn then press F1 on macOS). Search the menu for "Preferences: Open Settings (JSON)". Use these settings in VSCode's `settings.json` file:

```json
"[java]": {
  "editor.defaultFormatter": "redhat.java"
},
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.guides.bracketPairs": true,
"editor.bracketPairColorization.enabled": true,
"editor.formatOnPaste": true,
"editor.minimap.enabled": false,
"editor.tabSize": 2,
"editor.insertSpaces": false,
"editor.formatOnSave": true,
"editor.wordWrap": "on",
"explorer.confirmDelete": false,
"explorer.confirmDragAndDrop": false,
"files.insertFinalNewline": true,
"files.trimFinalNewlines": true,
"prettier.jsxSingleQuote": true,
"prettier.singleQuote": true,
"prettier.trailingComma": "none",
"prettier.useTabs": true,
"prettier.printWidth": 120,
"diffEditor.wordWrap": "on",
"liveServer.settings.donotShowInfoMsg": true,
"editor.glyphMargin": false,
"editor.folding": false
```

## Loading QuintOS Games

Make a new folder in `quintos-projects` called `games_java`. Copy the `GuessTheNumber` folder from Level_00 in IntroToJava and paste it in `games_java`.

Copy your GuessTheNumber code from CodePen and put it in `GuessTheNumber.java`

Edit the `load.js` in your `quintos-projects` project folder.

```
QuintOS.username = "your username";
QuintOS.gameTitle = "GuessTheNumber";
```

Right click on `QuintOS_live.html` file and select `Open with Live Server`. You should see the calculator show up in your browser. 😄

You've finished the install process! Read the next lesson section before starting PickAPath.

## Special characters

When you make Strings using quotes they can't be on multiple lines of your Java file.

```java
String example = "I want to put something on a new line:
something"; // ERROR!
```

To put part of a String on a newline use `\n` the newline character.

```java
String example = "I want to put something on a new line:\nsomething";
```

```txt
I want to put something on a new line:
something
```

The tab character `\t`, note that the `+` operator is used to add another String to the list on a new line in the Java code.

```java
String list = "Grocery list:\n\n\t"
	+ "Apples\n\tOranges\n\tBananas";
```

```txt
Grocery list:

	Apples
	Oranges
	Bananas
```

## End of Level 01 A

Start your PickAPath game! Follow the instructions in project file `PickAPath.md` located in the same folder as this lesson file.

# Level 01 B

## Boolean Operators

### NOT (aka negation)

```txt
!x is true if x false

Truth Table (0 means false, 1 means true)
x
0 = 1
1 = 0
```

### OR

```txt
(x || y) true if x or y is true
Checking x first, then y if x is false.

Truth Table
x y
0 0 = 0
1 0 = 1
0 1 = 1
1 1 = 1
```

### NOR

```txt
!(x || y) true if both x and y are false

Truth Table
x y
0 0 = 1
1 0 = 0
0 1 = 0
1 1 = 0
```

### AND

```txt
x && y true if x and y are true

Truth Table
x y
0 0 = 0
1 0 = 0
0 1 = 0
1 1 = 1
```

### NAND

```txt
!(x && y) true if any are false

Truth Table
x y
0 0 = 1
1 0 = 1
0 1 = 1
1 1 = 0
```

## Compound Operations

Try it out! What is the solution to this truth table?

```txt
(x || y) && z; // true if x or y is true and z is true
// truth table
x y z
0 0 0 =
1 0 0 =
0 1 0 =
0 0 1 =
1 1 0 =
1 0 1 =
0 1 1 =
1 1 1 =
```

# Level 01 C

## Arrays

[Arrays](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Arrays.html) are lists of variables with numbered indexes.

```java
String[] names = new String[]{"Amy", "Ellie", "Max"};
Integer[] nums = new Integer[]{50, 21, 46, 83};
```

## Array contains

Check if an array contains a number by converting it to an ArrayList using `Arrays.asList` and then using the `contains` method. You'll learn what an ArrayList is in a future lesson.

```java
Intger num = 21;
if (Arrays.asList(nums).contains(num)) {
  // ...
}
```

## Array length

length is a property of Array accessed using a period `.`

```java
System.out.println("The names array has " + names.length + " names");
```

This example code would print "The names array has 3 names" to the console.

## Computer History: Commodore PET

This level's computer was inspired by the 1977 Commodore PET 2001 Series. These computers were some of the first commercially successful personal computers that did not require any assembly by the user. Check out this video about it if you'd like!

https://www.youtube.com/watch?v=eP9y_7it3ZM

PETSCII character set: <https://style64.org/petscii/>

- [Level 01 A](#level-01-a)
  - [Requirements for Offline Development](#requirements-for-offline-development)
  - [Setup](#setup)
  - [Install Extensions for VSCode](#install-extensions-for-vscode)
  - [VSCode Settings](#vscode-settings)
  - [Loading QuintOS Games](#loading-quintos-games)
  - [Special characters](#special-characters)
  - [End of Level 01 A](#end-of-level-01-a)
- [Level 01 B](#level-01-b)
  - [Boolean Operators](#boolean-operators)
    - [NOT (aka negation)](#not-aka-negation)
    - [OR](#or)
    - [NOR](#nor)
    - [AND](#and)
    - [NAND](#nand)
  - [Compound Operations](#compound-operations)
- [Level 01 C](#level-01-c)
  - [Arrays](#arrays)
  - [Array contains](#array-contains)
  - [Array length](#array-length)
  - [Computer History: Commodore PET](#computer-history-commodore-pet)
