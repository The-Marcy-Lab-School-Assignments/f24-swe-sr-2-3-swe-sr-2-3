# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

Flexbox is used to arrange html elements along a single axis, either into a row or a column, while grid allows us to arrange html elements along 2 dimensions simultaneously, using grid we can specify how many html elements we want per row.

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

The difference in justify-content and align-items lies in the axis they control in positioning elements in FlexBox. Justify-content, aligns items along the main axis. On the other hand, align-items arranges items along the perpendicular axis. An important detail to consider is the direction their aligned is dependent on the flex-direction of the container.

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

`grid-template-areas` is used to define named areas within the grid for easier item placement, with `grid-template-rows` you can arrange different HTML elements using their name attribute, This is definitly a great tool for structuring the basic lay out of your website.

EXAMPLE:

```css
body {
  grid-template-areas:
    'header header header'
    'sidebar content content'
    'footer footer footer';
}

.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.content {
  grid-area: content;
}

.footer {
  grid-area: footer;
}
```

In the example above we can already deduce by basic reasoning that each string represents a page element, and that our three strings resemble a layout telling us what element and where do we want to place it in our pages body.

Now `grid-template-columns` and `grid-template-rows` specifically handles how we want to format other grid items either along the y-axis if we're using `grid-template-columns` or along the x-axis if we're using `grid-template-rows`

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

The `min-width` and `max-width` keywords are used to apply styles based on the width of the viewport i.e screen size of the device. They are crucial in enabling responsive breakpoints for various screen sizes because they give you the ability to adapt your CSS styling based on defined a range of screen sizes.

The example below demonstrates the key differences between the two keywords.

```
@media (min-width: 500px) {
    body {
        background-color:red
    }
}
```

In the CSS code above, the `min-width` keyword is used to apply background styling to screen sizes equal to or greater than the specified width. In this case, the body will have a background color of red on all screen sizes greater than 500px wide.

```
@media (max-width: 1200px) {
    body {
        background-color:blue
    }
}
```

The `max-width` keyword is used to apply the background styling to screen sizes equal to or less than the specified width. In this instance, the background color of the body will be set to blue.

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

- An explanation of mobile first design and a few of the benefits of this approach
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5

Mobile-first design means that when creating a website or app, you start by focusing on how it will look and work on mobile phones. Since more and more people use their phones to browse the internet, this approach ensures that the website is easy to use and fast on mobile devices first. Once that’s done, the design is then adapted to look good on bigger screens like tablets and computers.

Some of the benefits of mobile-first design are:

- Mobile-first design forces you to keep things simple and load quickly. Websites that load faster make users happy and are less likely to be abandoned. This also helps if your users have slower internet connections.

- Google prefers websites that are mobile-friendly. Since Google now checks the mobile version of your site first when deciding how to rank it in search results, a mobile-first approach can help your site show up higher in searches.

- Mobile screens are small, so when designing for mobile first, you need to focus on the most important content. This means that visitors will see what really matters right away, with no distractions.

In short, mobile-first design is all about making sure that your website works great on phones before adding extra features for bigger screens. It leads to a better experience for users, faster load times, better SEO, and ultimately, a website that works well no matter what device you're on.

Example of Mobile-first design on CSS:

```css
/* Base styles: Mobile-first layout */
.container {
  display: grid;
  grid-template-columns: 1fr; /* Single column on mobile */
  gap: 20px; /* Space between items */
  padding: 10px;
}

.item {
  background-color: lightblue;
  padding: 20px;
  text-align: center;
  border: 1px solid #ccc;
}

/* Tablet and larger devices (600px and up) */
@media (min-width: 600px) {
  .container {
    grid-template-columns: 1fr 1fr; /* Two columns on tablets and larger */
  }
}

/* Desktop and larger devices (1000px and up) */
@media (min-width: 1000px) {
  .container {
    grid-template-columns: 1fr 1fr 1fr; /* Three columns on desktop */
  }
}
```

Here our mobile design is our default lay out and as the screen size of device increases then our media query comes into play, by changing the way we arrange the grid items in our page. For mobile design we can see that we are arranging all gridf items in a single vertical line `grid-template-columns: 1fr;` which changes for tablets to a two column format `grid-template-columns: 1fr 1fr;` and then to a three column format for desktops in our last media query example `grid-template-columns: 1fr 1fr 1fr;`
