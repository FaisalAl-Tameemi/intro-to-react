# Your First ReactJS Component

To see where the page is being rendered from, use your code editor to open the `/src/index.jsx` file. You will notice that we are importing a JSX file called App which contains the main component of our page.

```javascript
import App from './App.jsx';
```

We are also calling the `<App />` component and rendering it within the the `div` which has an ID `react-root`.

```javascript
ReactDOM.render(<App />, 
                document.getElementById('react-root'));
```

----

## The App Component

By inspecting the `/src/App.jsx` file

```javascript
// load the react library
import React from 'react';

// create a class which inherits 
// from React's component class
class App extends React.Component{
    // a react component method
    render(){
        // return what you want to display
        return(
            <h1>Hello React :)</h1>
        );
    }
}

// allow import of this component in other files
// aka export the component
export default App;
```

Spend a bit of time writing regular HTML code within the `render` method in this component and see how your page changes.

As we previously discussed, all valid HTML is valid JSX.

You may notice that if you tried to write the following in your render method

```javascript
render(){
    return(
        <h1>Hello React :)</h1>
        <p>Some more text here</p>
    );
}
```

then you will get an error from React complaining about the fact that you have 2 sibling nodes (2 tags with the same level of depth and the same parent). 

This happens because React treats each component as a single tag to be called from other components.

The way to get around this is by wrapping up all of the contents of your component in a `div` or another tag:

```javascript
render(){
    return(
        <div>
            <h1>Hello React :)</h1>
            <p>Some more text here</p>
        </div>
    );
}
```


