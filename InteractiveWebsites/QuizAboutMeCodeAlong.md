# Quiz About Me: JavaScript Code-Along
In this activity, start building a quiz about yourself! Other people will be able to go to your website, and test their knowledge of YOU!

## Getting Started
You can start by forking [this template](https://hytop.onrender.com/e/www-js) to jump right in.

### Starting from Another Project
If you're starting from a different project, you will need these two things:

ONE: A **script.js** file with a stub `startQuiz` function defined as such:

```js
function startQuiz() {
  // lots of lines
}
```

TWO: An **index.html** that includes a link to the **script.js** file, like this:

```html
<script src="script.js"></script>
```

Optionally, feel free to update other HTML or CSS before beginning as well!

## Displaying a Message
The first thing to do is make the `startQuiz` function display a message! Under the `function startQuiz() {` line, above the `}`, add a new `alert` statement:

1. `alert` keyword
2. Parentheses `()`
3. Quotation Marks `""` within the `()`
4. A message within the `""`
5. A semi-colon `;`

The code in the **script.js** file should look something like this!

```js
function startQuiz() {
  alert("Welcome to my quiz!");
}
```

## Commanding the Function
So that's great, but how do we actually get the `startQuiz` function to _run_? It's time to add a button!

1. Open the **index.html** file
1. Add a new `<button></button>` element
1. Put your cursor between `<button>` and `</button>`
1. Give the button some text, like `Click Me`
1. Add an `onclick` attribute
1. Set the `onclick` attribute to `=` something in `""`
1. In the `""`, call the `startQuiz` function by saying its name followed by `()`

The added code in the **index.html** file should look something like this:

```html
<button onclick="startQuiz()">Start Quiz</button>
```

Save the project, click the button, and see what happens! The message should appear in a pop-up.

## Adding a Greeting
>_**NOTE:** Everything below here will be in the **script.js** file!_

Next, we should welcome the quiz taker to our quiz. We can ask for their name using `prompt`, store their answer in a variable, and reply.

1. Under the `alert` (still above `}`), make a new line
1. Use a `prompt` to ask the user for their name
  1. `prompt` keyword
  2. Parentheses `()`
  3. Quotation Marks `""` in the `()`
  4. A question in the `""`

Save the project and click the button to see the prompt appear! Now we just have to save the answer.

1. Put your cursor to the _left_ of the `prompt` line
1. There, create a new variable named `name`
   1. `let`
   2. `name`
   3. `=`
3. Set the `name` variable to equal to the `prompt`

Now the user's name is stored in the `name` variable. We can use it to say hi!

1. Make a new line under the `prompt` (still above `}`)
1. Add an `alert` that says `"Hi, "`
1. Between the `(` and `)`, add `+ name` to add the `name` variable value to the end of the message

Save, click, and see what happens! It should respond based on the user input, saying "Hi, Person" for Person.

The added code should look something like this:

```js
let name = prompt("What is your name?");
alert("Hi, " + name);
```

## Quiz Variables
We will want to keep track of a couple things for the quiz: the number of `points` (starting at `0`), and the total number of questions (we will make our quiz `2` questions long). We can make two new variables for this!

1. `let` keyword
2. Variable name
3. `=` Equals sign
4. Variable value

We want to make a `points` variable set to `0`, and a `numberOfQuestions` variable set to `2`. Note that capitalization matters, and no spaces are allowed in variable names.

The added code in the `startQuiz` function should look something like this:

```js
let points = 0;
let numberOfQuestions = 2;
```

## Asking a Quiz Question
Okay okay okay. We have added a lot of stuff, but what does any of this have to do with a quiz about me? NOTHING!

Well, it's time to change that! Let's ask our first quiz question :)

We can use `prompt` to ask the question, and create a new variable named `answer1` to store the user's answer.

1. `let` keyword
2. Variable name (`answer1`)
3. `=` Equals sign
4. `prompt` keyword
5. `()` Parentheses
6. `""` Quotation Marks within the `()`
7. Message within the `""`
8. `;` Semi-colon at the end

The added code should look something like this:

```js
let answer1 = prompt("What is my name?");
```

Click the button and see what happens - it asks the question, but doesn't do anything!

## Checking the Answer
Now that we have their answer, we should check to see **if** it's correct. If it is, they can increase their `points` by `1`.

We can do this with an `if` statement!

1. `if` keyword
2. `()` Parentheses
3. Condition inside of the `(` and `)`
   1. Left value `answer1`
   2. `===` Triple equals
   3. Right value `"YOUR NAME"`
4. `{}` Curly brackets
5. Body between `{` and `}` - set `points` to itself plus one
   2. `points`
   3. `=` equals
   4. `points`
   5. `+` plus
   6. `1`

The added code should look something like this:

```js
if (answer1 === "Joseph") {
  points = points + 1;
}
```

It still doesn't do much, but we _can_ `alert(points)` at the bottom of the function to make sure it's working!

## Asking Another Question
Now, a quiz with one question isn't very interesting. Luckily, we can do basically the exact same thing we just did to add one more question!

1. Create a `prompt` asking the question
2. Store the users answer in a new variable
3. Use an `if` statement to check if their answer `===` the correct one
4. If it's correct, set `points` to `points + 1`

The added question might look something like this:

```js
let answer2 = prompt("Where was I born?");
if (answer2 === "Cleveland") {
  points = points + 1;
}
```

Again, using `alert(points)` is one way to test that the points are stacking up properly. But there's a better way!

## Calculating the Final Score
Let's count up the user's points, and display their final score.

1. Create a new variable named `score`
2. Set it equal to the number of points divided by the number of questions
   1. `points / numberOfQuestions`
   2. _This can be alerted to test if desired_
1. Create _another_ new variable, named `percentage`
2. Set it to equal the score times 100
   1. `score * 100`
3. Use an `alert` to tell the user their final percentage
   1. Add it in between `"Final Score: "` and `"%"` to make it look nice 

Test it out by clicking the button, and answering different answers to make sure your quiz properly displays the score at the end!

The added code should look something like this:

```js
let score = points / numberOfQuestions;
let percentage = score * 100;
alert("Final Score: " + percentage + "%");
```

And that's it!

## Code
By the end of the activity, your code should look something like this:

**index.html**
```html
<script src="script.js"><script>
<button onclick="startQuiz()">Start Quiz</button>
```

**script.js**
```js
function startQuiz() {
  alert("Welcome to my quiz!");

  let name = prompt("What is your name?");
  alert("Hi, " + name);

  let points = 0;
  let numberOfQuestions = 2;

  let answer1 = prompt("What is my name?");

  if (answer1 === "Joseph") {
    points = points + 1;
  }

  let answer2 = prompt("Where was I born?");
  if (answer2 === "Cleveland") {
    points = points + 1;
  }

  let score = points / numberOfQuestions;
  let percentage = score * 100;
  alert("Final Score: " + percentage + "%");
}
```

## Next Steps
Try adding more questions in the same way! Make sure to update `numberOfQuestions` and use new variable names (e.g., `answer3`).

### Template Project
[Click here to make a fancy quiz.](TemplateProject.md)
