# Theme Toggle
 <h3>An isolated dark theme toggle using CSS & JavaScript</h3>

Feel free to implement this in your own website! 

To do so you would first want to define the colors you are using in each theme. You may need to add/remove color variables as you see fit. These are located at the top of style.css

```css
/*--------------------Reusable Variables--------------------*/
:root {
    /*--------------------Light Theme Variables (Default)--------------------*/
    --light-theme-background-color: #eee;
    --light-theme-darker-background-color: #ccc;
    --light-theme-text-color: #333;
    --light-theme-link-color: #ff6347;
    --light-theme-link-hover-color: #fa2600;

    /*--------------------Dark Theme Variables--------------------*/ 
    --dark-theme-background-color: #333;
    --dark-theme-darker-background-color: #111;
    --dark-theme-text-color: #eee;
    --dark-theme-link-color: #00fa9a;
    --dark-theme-link-hover-color: #00955b; 

    /*--------------------Other Variables--------------------*/ 
    --link-hover-timing: all 0.25s ease-in-out;
    --theme-change-timing: all 1s ease-in-out;
}
```

In theme-toggle.js you will see the following code:

```js
var body = document.querySelector('body');
var bodyClass = body.classList;
var themeToggle = document.querySelector('#theme-toggle');
var footer = document.querySelector('.footer');
var light = document.querySelector('.light');
var dark = document.querySelector('.dark');

themeToggle.addEventListener('click', () => {
    body.classList.toggle("light");
    body.classList.toggle("dark");
    themeToggle.classList.toggle("btn-light");
    themeToggle.classList.toggle("btn-dark");
    footer.classList.toggle("footer-light");
    footer.classList.toggle("footer-dark");
});
```

You can of course change these whichever way you see fit, however, if you'd like.
