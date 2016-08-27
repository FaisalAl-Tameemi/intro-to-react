# Building Components With JSX


## What Is JSX?

JSX is React's way of writing HTML-ish code (in reality it's a form of XML) within our Javascript code. 

This is different because Javascript MVC frameworks and templating engines (ex: EJS) can be thought to bring your Javascript code into the HTML. Similar to what ERB templates do for Ruby code.

It may feel awkward to write JSX in the beginning but once you get started, it's almost as though you can't go back.

This also goes back to the "React way of thinking" about your components. They are reusable entities that could have their own logic as well as visual representation (UI elements).

You can think of this as a way to build custom HTML tags and superpower them with their own logic (i.e. JS code).


### Why Do We Need It?

The reality is that you don't actually have to use JSX to build your UI but the alternative (writing it entirely in JS) isn't a pleasant experience. 

To render a simple `<h1>` tag

```html
<h1>Hello!</h1>
```

while using vanilla (pure) JS in React:


```javascript
React.render(React.createElement('h1', null, 'Hello!'),
             document.getElementById('myDiv'));
```

Now imagine building an entire application like that. 

It would be way too much writing to represent the simplest UI elements.

**The great part is that all valid HTML code is valid JSX.**

We will practice writing JSX code as we get started with building our first React component.

Tools such as **Babel** (see resources below) are then used to transpile (aka fancy convert) JSX code into valid Javascript (ES5 to be specific).

----

## Resources & Other Links

- #### [JSX In Depth - Facebook](https://facebook.github.io/react/docs/jsx-in-depth.html)
- #### [Babel for JSX](https://babeljs.io/docs/plugins/transform-react-jsx/)
- #### [React Dev Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
