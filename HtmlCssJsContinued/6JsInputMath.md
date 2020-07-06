# JavaScript Inputs & Math Lesson
In this activity, use JavaScript to create a website that can calculate the total cost of a restaurant bill. Use variables, `prompt`s, and math to ask the user for information and find the total!

## Starter CodePen
Students should navigate to [bit.ly/calcstarter](https://codepen.io/jmaxwell/pen/QWygJeW?editors=1010) to get the starter code. Display the link in very large font so they can see it, and make sure they type it in exactly like that (it is case-sensitive).

So far, the page has some HTML and CSS. There is a `table`, which is a new element, but there is no need to dive deep on that; the important thing is the `button` element. The goal of the activity is to define a function in JavaScript that will run when someone clicks the button!

## Defining the Function
To make something happen when someone clicks the button, define a function with the proper name in the JavaScript.

1. Expand the JS section
1. Type the first thing needed to define a function: the word `function`
1. Ask the students what the name of the function should be
    - In this case, the HTML button is already _calling_ it: `calculateBill`
1. After `function`, type in the function name followed by parentheses
1. After the parentheses, add curly brackets, and press Enter in between them
1. In the _body_ of the function, ask the students how to show a message
1. Use `alert`, with parentheses and quotes, to say "Welcome!"
1. Click the button, and make sure the message pops up!

```js
function calculateBill() {
    alert("Welcome!");
}
```

## Saying Hello
Next, the function should say hello to the user, but not just a general hello. First, ask the user for their name, and then say hello to them by name!

> **Note: Variables and `prompt`**  
> `prompt` lets JavaScript ask a question and remember the answer. The answer is stored in a **variable**. In computer science, variables are containers for data.

1. On the line under the `alert`, _before_ the closing curly bracket, type in `var`
    - This will create a new variable
1. After `var`, make a space and type in `answer`
    - This is the name of the variable
1. After `answer`, type in an equals sign
    - This is how the variable value will be set
1. After the equals sign, type in `prompt`, then parentheses and quotes
    - This is a lot like the `alert` command!
1. Type in a message _between_ the quotes: "What is your name?"
1. End the line with a semi-colon
1. Click the button, and see that the question appears and lets the user type in an answer
    - All that's left is doing something with the user's answer!
1. Make a new line, and type in `alert`, parentheses, and quotes
1. In the quotes, type in "Hello", then a comma and a space
1. After the closing quote, type in a plus and then `answer`
    - This will add whatever the user answered to the end of the message!
1. End the line with a semi-colon
1. Test out the button again, and verify that it will say hello to whatever name is entered!

```js
var answer = prompt("What is your name?");
alert("Hello, " + answer);
```

## Getting the Item Counts
Now it's time for the function to find out how many of each item to purchase. Use `prompt` to ask the user how many items, and store their answers in variables!

1. Make a new line under the `alert` in the JavaScript
1. Make a new variable using `var`, and name the variable `pizzas`
1. Set the variable equal to a `prompt` asking "How many pizzas?"
1. Ask the students to help make a new variable for hotDogs
    - What is the first thing needed? (`var`)
    - What should the variable name be? (`hotDogs`)
    - What comes after the variable name? (an equals sign)
    - How is it possible to ask the user a question? (`prompt`)
    - What does `prompt` need? (parentheses and quotes)
    - What should the message be? (How many hot dogs?)
1. Test out the button again, and verify that the new questions are asked

```js
var pizzas = prompt("How many pizzas?");
var hotDogs = prompt("How many hot dogs?");
```

## Calculating the Total Price
Now, the JavaScript will remember how many pizzas and how many hot dogs the user wants. It's time to calculate their bill based on those numbers!

1. Ask the students how to calculate the total price based on the price of the pizza and hot dogs, and the number of each item
    - It should be something like this: `total price = (number of pizzas times 4) plus (number of hot dogs times 2)`
1. Make a new variable using `var`, and name the variable `totalBill`
1. Use an equals sign to set the variable value to something
1. To get the total price of the pizzas, use `4*pizzas`
1. To add something else, use `+`
1. To get the total price of the hot dogs, use `2*hotDogs`
1. End the line with a semi-colon
1. On the next line, make an `alert` with parentheses and quotes
1. In the quotes, type the message: "Your total is: $"
1. Ask the students how to add something to the end of the message
    - Using `+`
1. After the ending quote, type in a `+` and `totalBill` to append the total to the end of the message
1. Click the button, and verify that the calculation works properly!

```js
var totalBill = 4*pizzas + 2*hotDogs;
alert("Your total is: $" + totalBill);
```

## Final Code
At the [end of the activity](https://codepen.io/jmaxwell/pen/yLeXJbB), the JavaScript code should look like this:

```js
function calculateBill() {
  alert("Welcome!");

  var answer = prompt("What is your name?");
  alert("Hello, " + answer);
  
  var pizzas = prompt("How many pizzas?");
  var hotDogs = prompt("How many hot dogs?");
  
  var totalBill = 4*pizzas + 2*hotDogs;
  alert("Your total is: $" + totalBill);
}
```

## Individual Work
With remaining time after the activity, give the students some time to work individually. Here are some ideas for challenges:

- Add food images to the HTML
- Update the page styles in CSS
- Add more items to the restaurant's menu
    - Create another `tr` with some `td` elements in the HTML `table`
    - In the JavaScript, use another `prompt` to ask how many of the new item someone would like
    - Add the new item count, multiplied by the item price, to the total price calculation

As the students work individually, be available to answer any questions they may have.