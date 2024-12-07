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

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

* An explanation of mobile first design and a few of the benefits of this approach
* A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
* An explanation of the code example.

### Response 5
Mobile-first design is designing programs for the smallest screen size first and evenutally adapting that design to larger screen sizes. Mobile-first design practices prioritize content in the context of user experience, signifying significance with element types such as paragraphs and headings. By avoiding the use of hover effects and large, complex images that cannot be easily adjusted for viewing across screen sizes, developers can ensure their applications are useable on mobile devices where hovering over elements is not possible and complex images can make pages harder to understand or to read. By decluttering a page and including less elements, developers can increase the likelihood their pages load faster and make the pages more accessible.

```css
.flex-container {
    display: flex;
    flex-direction: column;
    background-color: red;
}

@media (min-width: 800px) {
    .flex-container {
        flex-direction: row;
        background-color: green;
    }
}
```

This CSS file first sets the `display` of elements of the `flex-container` class to `flex`, creating a flexbox. The `flex-direction` value of `column` ensures that all elements in this flexbox will initially be positioned in a column. On mobile devices, the flexbox's elements will be in a column and the background color of the container will be red. On devices of 800px or more, the `background-color` is now set to `green` and the `flex-direction` value is now `row`, changing the direction of the elements given how there is a greater horizontal width for the elements of the flexbox to fit along the main axis.
