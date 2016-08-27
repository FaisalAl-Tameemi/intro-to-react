# Starter Kit Setup

Follow the steps below to setup your local copy of the starter kit that we will use:

* Step 1 - clone the repo

        git clone https://github.com/lighthouse-labs/react-simple-boilerplate

* Step 2 - Install the required dependencies
    
        cd react-simple-boilerplate
        npm install

* Step 3 - Run the app

        npm start

* Step 4 - Visit `http://localhost:3000` in your browser to view the page


If you're up and running, you should now see a webpage with the text "Hello React :)".

Once you've opened the boilerplate code in your code editor, go ahead and open up the `index.html` file.

In there you will notice that it doesn't actually content the "Hello World" message you previously saw by running the app. This is because the content is being dynamically attached to the DOM.

The ReactJS code is attaching the entire app to the following `div`:

```html
<div id="react-root"></div>
```

And through the JS tool, Webpack, the entire app is being bundled into a single file when your run `npm start`.
