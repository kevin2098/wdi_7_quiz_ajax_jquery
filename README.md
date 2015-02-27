# JQuery/Ajax Quiz

Write your answer below each question.

### Question 1
(a) What is a click handler?
-A click handler executes a function each time event is triggered

(b) Where in your JS file should you put it, and WHY?
-You should put it with the document ready so that it will only work once the all the JS is loaded and the DOM is ready

### Question 2
If you get the error `$ is undefined`, what does that mean and what could you do to fix it?
-You haven't referenced the JQuery properly...add the CDN reference in a src tag in the html

### Question 3
What should go in the `$(document).ready()` part of your JS file?
-Everything

### Question 4
In an AJAX GET request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent?

```
$.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  });

```
-It represents the users

### Question 5
In an AJAX POST request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent? (Hint: it's not the same as in Question 4.)

```
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'POST',
    dataType: 'JSON',
    data: { user: { name: "Anna", about: "instructor", email: "hi@gmail.com" } },
  })
  .done(function(data) {
    console.log("success!");
  });
```
-The user hash?

### Question 6
Suppose you had the following form in your HTML file. Use jQuery to write a single line of code that takes whatever the user entered in the textbox and saves it to the variable `user_input`.

```
  <form>
    <p>The dress is:</p><input type="text" id="color">
    <input type="submit" value="Submit" id="submit">
  </form>
```
-var user_input =  $('#color').val()

### Question 7
This code looks like it works, but when you run it, you see that the `UserApp.add_all_users()` function executes but `console.log` displays `undefined`. What's wrong with the code?

```
UserApp.get_all_users = function() {
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  });
  UserApp.add_all_users(data);
};

UserApp.add_all_users = function(data) {
  console.log(data);
};
```

-I know we just went over this but I'm having a massive brain fart, it has something to do with "users" and "data"

