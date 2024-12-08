# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

**_Flexbox_** and **_Grid_** layouts are display options that developers use to customize websites to have a certain design with the containers. With **_Flexbox_**, if you're looking to just work with one dimensions layouts, that is the display option you would want to go with. Any complex, 2 dimensional designs, you would want to use **_Grid_** to control how may rows or columns you want to keep as the screen resolution decreases or increases.

An example of when you would want to use **_Flexbox_** is when you are making simple portfolio website to display all of your work/projects and things of that nature. However, If you are trying to create something like a responsive magazine website, you would want to use **Grid**

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

**_justify-content_** and **_align-items_** both control where the flexbox will be located on a document. It just changes which axis the flexbox will move on.

**_justify-content_** moves the flexbox on the main axis. When flexbox is set to the default direction, **_justify-content_** axis runs from left to right and **_align-items_** moves the flexbox vertically (up or down).

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

**_grid-template-areas_** and **_grid-template-columns/rows_** a both related to the display option **Grid**, but they give you access to different things.

**_grid-template-areas_** gives you complete control over how many columns and rows you want, the names of those columns and rows and even gives you the ability to 'draw' out the layout using the names you've provided. On the other hand, **_grid-template-columns/rows_** allows you to just create rows and columns without the ability to give them a name or custom layout.

You would want to use **_grid-template-columns/rows_** if you just want a table looking organizer for holding information or something less complex. You would want to use **_grid-template-areas_** if you want to have a unique layout like a catalog for the NYFS (New York Fashion Show).

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

when working with Media queries, **_min-width_** and **_max-width_** set the size of containers and items to be a certain size once the screen resolution gets to a set screen size.

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

- An explanation of mobile first design and a few of the benefits of this approach
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5

Mobile-first design is the idea that starts designs and layouts for small screens and then builds on-top of that design as the screen size gets bigger. The main idea is to make the 'app' in the most constrained setting first then add more complex elements later for bigger screens.

The benefit in doing this is primarily for the user. The user could experience better performance, user experience, etc. As the programmer you can get better scalability since your building on top of the small baseline screen size. This ultimately makes this method future proof.

`HTML`

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

`CSS`

```css
.container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
@media (min-width: 768px) {
  .container {
    flex-direction: row;
    flex-wrap: wrap;
  }
}
```

this was an example of using the screens sizes, 768px is an industry practice for the size of tablets. We started with a base design for mobile (typically 320px but iphone is typically around 375px) and changed the design/layout for tablets, and we could go further and change it again for larger screens!!
