# Component Hierarchy

In order to leverage the power of ReactJS and use it to build large web applications, you must learn to break down your applications into smaller pieces, each doing exactly what it needs to do and not more.

This process of dividing up the tasks of your entire application among reusable UI components can be a little challenging at first as the rewards are harder to really observe, however as your application gets larger and larger, having an organized breakdown of your app can be of immense benfit.

It is also important to note that this isn't the only way to build scalable web applications but it is certainly a pattern that is being adopted by Javascript MVC frameworks such as Angular2.


## Components Breakdown

Let's practice this way of thinking about our web applications. 

In a scenario where we have to build a simple feature section of a web page with a video player on the side along the lines of:

![png](https://cl.ly/0m3H2J3Z110S/Image%202016-08-26%20at%2011.07.24%20PM.png "feature_video_highlight")


Now, to build this using ReactJS we first need to breakdown the UI into subsections.

We notice that there are 2 main elements in this mockup:

1. The text content with the title
2. The video player

Since this seems to be a UI component that we can reuse in other pages of our website, we can turn the whole thing into a single component, `<VideoContentHighlight />`. 

If we want to, we can go even further by building 2 more components that correspond to the elements listed above. The first we will call `<TextContent />` and the second '<VideoPlayer />'. 

![png](https://cl.ly/2l0t36261N1S/Image%202016-08-26%20at%2011.15.00%20PM.png "labeled_breakdown")

----

## Resources & Other Links

...