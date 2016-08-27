# The Virtual DOM

Ok so you keep reading that React has this concept called **Virtual DOM** but what is it? and what's so special about it?

To understand this, we must first make sure that we understand the problem it is solving.


## The DOM Challenge

The challenge when building interactive web applications is that **the DOM**, the actual Document Object Model that lives in the browser, **was never built for dynamic user interfaces** (UIs).

While we can use libraries such as jQuery to manipulate it and create nifty user interactions, these libraries aren't built to optimize larger web applications.

The bigger your web app, the more nodes there are in the DOM Tree. As the number of nodes grow (i.e. as more content is loaded onto the page - think of Twitter or Facebook), the less performant your app gets when trying to make changes to the DOM Tree.

There are a couple of approaches to solving this problem, but the one we're interested in for now is the Virtual DOM.



## Enter The Virtual DOM

Instead of updating the DOM directly and frequently, often without the need to, we could use a Virtual DOM which represents a replica of the original DOM with the added bonus of being able to make changes to it without slowing down the browser.

Once we update the virtual DOM, we can then use efficient diffing (aka difference checking) algorithms that tell us if we actually need to update the real DOM and thus showing new content on the browser window.


![virtual_dom](https://cl.ly/1g2l300L0i2J/Image%202016-08-26%20at%209.42.12%20PM.jpg "virtual_dom")

Image From: _`http://www.toobler.com/blog/reactjs-a-powerful-javascript-library-for-incredible-user-interface`_


This is implemented out of the box with ReactJS.


----

## Resources & Other Links

- #### [Article: What Is Virtual DOM](https://medium.com/tony-freed-consulting/what-is-virtual-dom-c0ec6d6a925c#.8o84lcn6i)
- #### [Slides: Exploring The Virtual DOM](http://slides.com/brandonkonkle/exploring-virtual-dom/#/1)