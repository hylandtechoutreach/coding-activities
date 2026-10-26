For a simplified version of the quiz, start from [hytop.onrender.com/e/www-jss](https://hytop.onrender.com/e/www-jss).

Allow students time at the start to update the starter with information about themselves.

End with code like this in the **script.js** file:

```js
function startQuiz() {
  alert("Welcome!");

  let name = prompt("What is your name?");
  alert("Hi, " + name);

  let answer1 = prompt("What is my name?");

  if (answer1 === "Joseph") {
    alert("CORRECT")
  }

  let answer2 = prompt("Where was I born?");
  if (answer2 === "Cleveland") {
    alert("CORRECT")
  }
}
```
