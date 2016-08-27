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

export default App;
```


----

## Resources & Other Links

...