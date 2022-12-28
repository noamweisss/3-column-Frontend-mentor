# 3 Column Layout with Responsive Design

> 1. [Challenge](#challenge)
> 2. [Solution](#solution)
> 3. [Final Result](#final-result)
> 4. [Furter Development](#further-development)
> 5. [Links](#links)

I built this 3 column layout as a solution to a challenge from [Frontend Mentor](https://www.frontendmentor.io). The layout includes icons, headings, paragraphs, and buttons; and is designed to be responsive, with the columns stacking vertically on small screens.

## Challenge

One of the main challenges I faced was getting the layout to be responsive. Since I was not very familiar with CSS grid, I had to learn and experiment with different techniques to achieve the desired result. I also found it a little tricky to get the spacing between the different elements to look good on all screen sizes.

## Solution

To make the layout responsive, I used a combination of media queries and CSS grid. Here is the relevant HTML code that sets up the layout:

```html
<main class="container">
  <section class="sedans">
    <!-- content goes here -->
  </section>
  <section class="suv">
    <!-- content goes here -->
  </section>
  <section class="luxury">
    <!-- content goes here -->
  </section>
</main> 
```

And here is the CSS that styles the section elements and makes the layout responsive:

```css
section {
  padding: 4rem 3rem;
  display: grid;
  gap: 1.5rem;
  transition: all 200ms ease;
}

@media(min-width: 800px) {
  .container {
    position: relative;
    margin: auto;
    max-width: 60%;
    flex-direction: row;
    top: 50%;
    transform: translatey(-50%);
    font-size: 1.125rem;
  }

  section {
    padding: 3rem;
    justify-items: space-between;
    gap: 2rem;
  }
}
```

The section elements are initially styled with padding and a `grid` display, with a gap of 1.5rem between them. This creates a 3 column layout with some space between the elements.

The `media query` targets screens with a minimum width of `800px` and applies styles to the container and section elements to change the layout to a row. The container element is given a `flex-direction` of row and is positioned in the middle of the page with `position: relative`, `top: 50%`, and `transform: translatey(-50%)`. The section elements are given a `justify-items` value of space-between and a gap of 2rem to create some space between the columns.

To achieve proper spacing between the elements within each section, I used padding and margin properties in the CSS. For example, to add some space between the heading and the paragraph in each section, I used the following styles:

```css
h2 {
  margin-bottom: 1rem;
}

p {
  margin-bottom: 1.5rem;
}
```

I experimented with different values to find the right balance that looked good on all screen sizes.

## Final Result

In the end, I was able to create a 3 column layout that is responsive and looks good on all screen sizes. I am happy with the result and feel like I learned a lot in the process.

![](./screenshot.png)

## Further Development

To continue developing my skills in layout design and responsive design, I plan to:

* Practice building more layouts using CSS grid and media queries.
* Explore other layout techniques such as Flexbox and CSS floats.
* Experiment with different values for padding, margin, and other spacing properties to find the right balance for my designs.
* Consider using a CSS preprocessor such as Sass or Less to simplify the process of writing and maintaining CSS.

## links
- [The solution page in Frontend Mentor](https://www.frontendmentor.io/solutions/3column-preview-card-component-5QK6Hp7bB5)
- [The live site I deployed using Github Pages](https://noamweisss.github.io/3-column-Frontend-mentor/)

