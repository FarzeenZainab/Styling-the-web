# CSS Grid

CSS grid is an alternative of flexbox and is used to layout elements across the page.

With flexbox you can create a one dimensional layout. It can be either row or column. But, with grid you can create two dimensional layouts and can manage rows and columns at the same time.

When to use Flexbox and when to use Grid?
A golden rule is to use grid when you are setting the overall page layout i.e header, main footer etc. If there are inner items you can use flexbox to align items.

## Creating a grid

In a grid we have grid container and grid items similar to flexbox. Any direct children of a grid container will be grid items.

All direct children of a grid container are called grid items. To specify gap between items you should always use gap property instead of margins.

set display: grid on the div you want to use as a grid. Setting the display property to grid will not give any result on the screen. We have to specify how many columns the grid will have and big we want those columns to be

### grid-template-columns

This property creates columns which will have specifies width

Example:
grid-template-columns: 200px 250px (can use % but, most commonly you will be using fractions)
This will give us 2 columns, the first column will be 200px wide and the second column will be 250px wide.

grid-template-columns: 1fr 1fr
This will give 2 columns with the exact same width

This property is for a grid-container only.

### repeat()

when defining equal columns instead of doing
grid-template-columns: 1fr 1fr 1fr 1fr

we can do
grid-template-columns: repeat(4, 1fr)
this gives us 4 columns of 1fr each

## Space between items

### column-gap

column-gap: 10px will give 10px space between columns only

### row-gap

row-gap: 10px will give 10px space between rows only

### gap

gap: 10px will give 10px space between rows and columns so, we donot have to use 2 different properties to give space

## How height works of grid items in a grid

grid items in a row will have the height same as the tallest item on that row

## Properties that deals with row and heights

### grid-auto-rows

This property sets the height of all grid items to same specified height
Ex: Let's say we have 9 grid items with some content in them. If we set grid-auto-rows to 300px all items will have the height of 300px regardless the amount of content in it. If the content takes more height than 300px, it will be cropped

minmax() inside grid-auto-rows
It takes a minimun and maximum value

grid-auto-rows: minmax(300px, auto);
All grid items will have a minimum height of 300px and if the content takes more than 300px space the height will be set to auto of that row

## grid-template-rows

It is similar to grid-template-columns but instead of columns it defines rows in a grid

grid-template-rows: 400px 500px 100px
This will set the height of all grid items inside the first row to 400px, second to 500px and third to 100px

You can use repeat() here

## Alignment Properties in CSS grid

### align-items:

This aligns/sets the height of grid items inside a row to the tallest grid item. The default value is stretch that gives us this behavior

If you donot want this behavior you can set this is start, center, end

### justify-content:

This aligns the grid items on x-axis. To view the result reduce grid-template-columns to a lower value 200px

## Spanning items across rows and columns

### Spanning Columns (span across)

grid-column-start -> column starts from the specified number
grid-column-end -> column ends on specified number

grid-column-start: 1
grid-column-end: 3

Shorthand
grid-column: 1 / 3 (starts at 1 and end at 3)

### Spanning Rows (span down)

grid-row: 1 / 3 (starts at 1 and end at 3)

## Responsivness in CSS Grid

You can use media queries to stach the columns on top of each other to make the grid responsive

### using auto-fill in grid-template-columns

grid-template-columns: repeat(auto-fill, minmax(200px, auto))
It will wrap the item to the next row if there is not enough space to fit item of 200px
