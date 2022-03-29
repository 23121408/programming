===
# Part 2 - Setup
===

To open up the console in browser press `Option + Command + j` on a Mac (or `Control + Shift + J` on Windows and Linux). Another way to get to the console is to right click on the web page, select `Inspect`, and then move to the tab called `Console`.

---

Alerting a message. In the Chrome Console, type the following:

```javascript
alert('JavaScript is sweet!');
```

---

You can also tell JavaScript to log a message directly to the console, using a function called `console.log`. Type `console.log('This is less obtrusive.');`

---

You can change position of console by pressing three vertical dots → and find chapter `Dock syde`.

---

Declare variable `var` called an `instructor` using the var key word and assign it to the string `"Elie"`:

```javascript
var instructor = "Elie";
```

Now if I wanna access that variable I can just type instructor and press enter
`instructor`

Let's try to access that var again, and as u can see I'am typing the console is guessing what command I'am trying to type. Soo I can press `tab` to aftercomplete witch is very helpful.

---

We can also evaluate a math expressions in the console. Soo I can see 25 * 40 is a 1000. Just type:

```javascript
25 * 40
```

---

We also get an immediately feedback if we made mistakes. Soo I declare a variable called wrong and assign it with a string with a small syntax error:

```Javascript
var wrong = "oops
```

When I press enter, the console tells me right away what I did wrong.

---

If you would like to clear the console you can either type in `clear()` and press enter or press `command + k`, or mouse over the ban circle icon.

---

But what about my previos commands, what if I wanna access them? Thankfully we can press `up` my past commands. Soo lets find my syntax error and fix that.

I press `up` to see my last command and necessary close quote to " fix our problem:

```javascript
var wrong = "oops";
```

---

You might wanna right a commands on a multiply lines. Hold `shift` key and press `enter` to make a new line:

```javascript
var x = 2;
var y = 22;
```

Now type x or y in console:

```javascript
x // youll see 2
y // youll see 22
```

===
# Part 2 - Variables and Primitives #
===

# Variables #

The word "variable" may be most familiar to you from math class, when you often use letters like x or y to represent numbers.

---

To see why variables are useful, suppose you want to log a set of greetings to the console:

```javascript
console.log("Hi, Matt!");
console.log("How are you doing, Matt?");
console.log("See you later, Matt!");
```

---

This works fine, but what if we want to change the person's name from "Matt" to something else? We'll have to change three different spots in our text file, and there's a risk that we'll make a typo when fixing any one of these changes.

So let's write our first variable. In JavaScript, you initialize variables using the `let` keyword. Strictly speaking, using this keyword is not necessary, but in practice it should almost always be there (we'll discuss why a bit later).

```javascript
let firstName = "Matt";

console.log("Hi, " + firstName + "!");
console.log("How are you doing, " + firstName + "?");
console.log("See you later, " + firstName + "!");
```

If you enter this code correctly, you should see the same result as before - JavaScript knows that `firstName` corresponds to the name Matt!

---

There are a few different things going on here, so let's unpack the code a bit. On the first line, we're declaring a variable using the `let` keyword. A variable is just a way for us to save some data in JavaScript. When we typed in `let firstName = "Matt"`, JavaScript stored the word `Matt` in the variable `firstName`. From then on, any time you use `firstName` in the console while this window is still open, youll see the value that `firstName` has stored.

---

On the subsequent lines, you'll see there's something else going on too: we're using the `+` operator to combine words made up of characters, or strings, together. In JavaScript, when you combine two strings with the `+` operator, you get a new string which is a combination of the two. You can think of this as adding the strings together; a more formal name for it is concatenation. For example, if you write the expression `"Hello" + " World"` in the console, you should see that the result is the single string `"Hello World"`.

Let's declare some more variables.

```javascript
let firstName = "Matt";
let lastName = "Lane";
let fullName = firstName + " " + lastName;
```

In all of these examples, we have the keyword `let` in front, followed by the variable name, an assignment operator (the `=` sign), and then the value we want to assign to our variable.

---

These examples also illustrate a common convention when writing JavaScript: when declaring variables using multiple words, the standard is to capitalize each word after the first word, and otherwise use lower-case letters (e.g. `firstName`, not `firstname`, `first_name`, `FirstName`, or some other variation). This casing convention is called camel case, and while your JavaScript code will work just fine if you don't abide by this convention, it's good to get in the habit of camel casing your variables.

# The `prompt` function #

Let's revisit our earlier example:

```javascript
let firstName = "Matt";
console.log("Hi, " + firstName + "!");
console.log("How are you doing, " + firstName + "?");
console.log("See you later, " + firstName + "!");
```

Since we've used a variable, if we want to change the name, now we only have to do it in one place. That's great! Try changing the value stored in `firstName` from "Matt" to your name.

---

Now suppose we wanted to ask the user for their name. In JavaScript, you can ask the user to provide some information using the `prompt` function. You won't use this function very often (there are better ways to get information from a user), but when you're first learning it's a helpful tool.

When you use the `prompt` function, a pop-up window will appear on the page and ask the user to fill in a text box. You can then store what the user types into a variable. Try it out with this modification to our example:

```javascript
let firstName = prompt("What is your first name?");

// Now firstName should correspond to whatever the user typed!
console.log("Hi, " + firstName + "!");
console.log("How are you doing, " + firstName + "?");
console.log("See you later, " + firstName + "!");
```

---

See that line in there that starts with two slashes? That indicates a comment.

```javascript
// Now firstName should correspond to whatever the user typed!
```

Javascript ignores comments; they are there purely to make notes about the code and generally help with its readability. You can create single-line comments with `//`; if you want a multiline comment, here's a haiku that shows how it's done:

```javascript
/* this is the start of
a multiline comment, and
this is the ending. */
```

# Primitive Data Types in JavaScript #

So far, we've only used variables to store strings. But JavaScript can work with other types of data as well. Let's take a look at the primitive data types (you don't need to worry about what primitive means just yet).

JavaScript has 6 primitive data types, but we'll only talk about 5 of them. Here's what they look like:
* string - `let greeting = "hello";`
* number - `let favoriteNum = 33;`
* boolean - `let isAwesome = true;`
* undefined - `let foo;` or `let setToUndefined = undefined;`
* null - `let empty = null;`

JavaScript is known as a "weakly" typed language. What this means is that when you create variables and assign them to values, you do not have to specify the type of data you are working with. In statically (or strongly) typed languages, like Java and C++, you do need to specify the type.