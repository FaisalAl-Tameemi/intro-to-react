# Component State & Props

## State

Every component in ReactJS has a `state` object. The goal of this state is to represent the data that the component is using in its display.

The state can be set as follows:

```javascript
import React from 'react';

class App extends React.Component{
    constructor(){
        this.state = {
            title: 'My App'
        };
    }

    render(){
        return(
            <h1>{this.state.title}</h1>
        );
    }
}

export default App;
```

Now, let's say we wanted to change the title of the app and have it automatically change the text of our `h1` tag, we can do the following:

```javascript
this.setState({
    title: 'New Title'
});
```

Running the code above would change the state which would automatically trigger another call to the `render` method.

Always remember, changing the state updates the component view (i.e. calls `render` again).


## Properties 

...

----

## Resources & Other Links

...