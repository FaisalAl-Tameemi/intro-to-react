## Blog Reader Components

Our goal is to build a blog reader which looks like the following:

![png](https://cl.ly/141J1f44033y/Image%202016-07-19%20at%2010.19.45%20PM.png "Blog List Preview")

Let's start by breaking down the end results into several components as a first approach to building the simple app.

![png](https://cl.ly/35193Z0q1f3f/Image%202016-07-19%20at%2010.35.03%20PM.png "Breakdown Skeleton")

You may have noticed that one of the components, `BlogListContainer`, has a dashed border. This is because it won't be displaying anything major to the screen, but rather will be the container for `BlogList` and `BlogContent` to allow them to interact and communicate changes to each other through.
