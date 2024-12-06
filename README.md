# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1
Flexbox is one-dimensional, used for arranging items in a row or column with control over the shifting and moving of items in relation to each other over either the main or cross axis. Grid is two-dimensional, using numerical coordinates for positioning in both rows and columns. Flexbox is most suitable when elements are in either a row or column and need to be aligned consistently. An example would be a navigation bar of evenly spaced elements in a row at the top of a page. Grid is most suitable when elements need to be arranged in both rows and columns, with some elements overlapping or of different sizes.

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2
`justify-content` is used to align flex items horizontally when not using all available space on the main axis. This can be used to position items at the start, end, or center of a container and can position items evenly with equal space between them or around them or with all extra space divided evenly to create a balanced layout. `align-items` is used to align flex items vertically when not using all available space on the cross axis. This can be used to align items to the start, end, or center of a container or to stretch items to fill a container.

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

The grid-template-areas property allows you to define the grid layout in a more visual way by naming specific areas of the grid. This is especially useful when you want to see the page layout in a more visual style that mirrors the webpages layout. 

On the other hand, grid template columns and rows are two properties that define the size of the said portions within a CSS grid. They're used together to create a grid layout.

You would prefer to use grid template areas when you have a complex layout with more clearly defined portions. This option can also be more useful when you need to rearrage the layout by changing the names of areas instead of adjusting the line numbers of the grid. On the contrary, you'd want to use grid template columns and rows whenever you need a finer say over the sizes of individual columns and rows. Doing so would allow you a more flexible layout which can also be more manageable when there isn't clear regions that need to be named.

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

 The `min-width` querie targets devices that have a viewing port equal or greater than the specified value which is mainly used for larger screen sizes. On the other end, `max-width` targets devices that have a viewport width that's less than or equal to the specified value. This is typically used for adding styles with smaller screens.

 The min and max width queries assist in creating more responsive breakpoints for different screen sizes by allowing a web application to adapt to different screen sizes without breaking the layout of the webpage which is essential for offering an amazing user experience. 

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

* An explanation of mobile first design and a few of the benefits of this approach
* A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
* An explanation of the code example.

### Response 5

