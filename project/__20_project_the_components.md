## Components Walk Through

Before going through this section, try to build the components on your own and see how far you can get.

Research the parts you don't know how to do and use this section as your reference from one approach.

### App.jsx


This is the main component that render on the page. From it, we will render everything else.


We can call this the a root node or root component.


```javascript
class App extends Component {
  render() {
    return (
      <div className='app-container'>
        <Toolbar title={this.state.title} />
        <BlogListContainer />
      </div>
    );
  }
}
```


In this component, we are simply calling `Toolbar` and passing it the app title which we have stored in this component's state.


We are also calling the `BlogListContainer` which in turn will handle displaying both the contents and the sidenav list.



### Toolbar.jsx


The `Toolbar` is a simple functional component which requires a title as a prop and nothing else.


Its render method is straight forward.


```javascript
render() {
  // in ES6
  const { title } = this.props;
  // in ES5
  // var title = this.props.title;
  return (
    <div className='rp-main-toolbar'>
      <h1 className='rp-toolbar-title'>
        { title }
      </h1>
    </div>
  );
}
```


### BlogListContainer.jsx


This is where the some of the magic will be happening.


As we discussed earlier, we will be using this component to communicate changes triggered by one component but effect another.


Before moving forward, let's have a look at the initial state of this components:


```javascript
{
  selected_item: null,
  items: []
}
```


The `selected_item` will hold the object that is being displayed in the main content area. The `items` array will hold the entire list of items being displayed in the sidenav.


**Remember:**
<small>If we are using the ES6 way of creating classes (i.e. using `extends React.Component`), then we only ever set the state with `this.state = {...}` in the `constructor` method. Otherwise, we will use `this.setState` which works the same way no matter how you're creating your React classes / components.</small>


For example, once we click an item on the sidenav, the content in the main area should change to reflect that interaction between the user and this app.


To achieve this, we will create a function `_onItemSelected` in the `BlogListContainer` class. Given an item object, this function is responsible for setting the state with the new `selected_item`.


```javascript
_onItemSelect(item){
  this.setState({
    selected_item: item
  });
}
```


We will then pass that function as a prop to the sidenav, `BlogList`, such that when an item is clicked, the function gets called.


In **BlogListContainer.jsx**:

```javascript
const list = (
  <div className='rp-bloglist-container'>
    <BlogList
      itemsList={this.state.items}
      selectedItem={this.state.selected_item}
      onItemSelect={(item) => this._onItemSelect(item)}
      onItemDelete={(item) => this._onItemDelete(item)}
    />
  </div>
);
```


In **BlogList.jsx**:

```javascript
render(){
  return (
    <ul className='rp-bloglist'>
      {
        this.props.itemsList.map((item) => {
          return (
            <li
              key={item.id}
              className='rp-bloglist-item'
              onClick={() => this.props.onItemSelect(item)}
            >
              { item.title }
            </li>
          )
        })
      }
    </ul>
  );
}
```


This will in turn change the state of the container and refresh the content as the selected item has now changed, illustrated below:


![Blog List Preview][bloglist_container_steps]


### BlogList.jsx

In this component we will simply `.map` over all the items that are being pass as the `itemList` prop and turn each item into an `li` element.


### BlogContent.jsx

A functional component that simply renders the item that is passed to it as a prop.