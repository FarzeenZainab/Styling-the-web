# What is a Flexbox

The flexbox is a one dimensional layout model that provides a method to offer "space distribution" and powerful alignment capabilites

before flexbox we aligned items using floats and tables.

- Another option for alignment is CSS grid
- Flex container is the tag which holds all flex childs/items
- Flex items are direct children of flex container

Both Flex container and flex item have different CSS properties which we can use to layout our page

Flex Container Properties:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

Flex Items:

- order
- flex-grow
- flex-shrink
- flex-basis
- align-self

## The Axes

The axes are important when using certain alignment properties that you understand how the axes goes

There are two Axes

- The Main Axis
- The Cross Axis

If flex-direction property is set to row (by default it is row)

- The Main Axis (goes on x-axis)
- The Cross Axis (goes on y-axis)

If flex-direction property is set to column

- The Main Axis ( goes on y-axis)
- The Cross Axis (goes on x-axis)
