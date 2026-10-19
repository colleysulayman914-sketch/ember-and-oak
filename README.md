# Ember & Oak Café — CSS Grid and Flexbox Website Project

A one-page website for a fictional neighbourhood café, built with HTML and CSS only.

- **Live site:** https://colleysulayman914-sketch.github.io/ember-and-oak/
- **Repository:** https://github.com/colleysulayman914-sketch/ember-and-oak

## File structure

```
index.html        Page markup (semantic HTML)
css/styles.css    All styles, grouped by section
README.md         Project note and reading check
```

## Reading check (Part 1)

1. **What is CSS Grid useful for?** Two-dimensional layouts, where I need to control rows and columns at the same time, such as whole-page regions, galleries or card grids.
2. **What is Flexbox useful for?** One-dimensional layouts: lining up and spacing items in a single row or column, such as navigation links, buttons or the contents of a card.
3. **Where I expect to use Grid:** The menu card grid, and the "specials" section with one large feature beside two smaller ones.
4. **Where I expect to use Flexbox:** The header (logo on the left, links on the right) and the dish name/price row inside each menu card.
5. **How I will check phone screens:** Use the browser developer tools at about 375px wide and check for no horizontal scrolling, readable text, usable navigation, and cards that stack.

## Planning (Part 3)

- **Audience:** Local residents, office workers and visitors looking for breakfast or coffee nearby.
- **Purpose:** Show the menu, opening hours, location and how to book.
- **Content:** About, Menu, Specials, Visit (hours, address, reservations).
- **Visual style:** Warm browns and terracotta to suggest a wood fire, a serif heading font with a sans-serif body font, generous spacing, and rounded cards. The only image is a simple SVG coffee cup drawn inline, so there are no external images to credit.

## Project note

Ember & Oak is a one-page website for a small café. It is for local customers who want to check the menu, opening hours and location before they visit.

I used **CSS Grid** for the larger layouts. The menu uses `repeat(auto-fit, minmax(260px, 1fr))`, so the cards fill as many columns as fit and drop to one column on a phone without extra media queries. The specials section uses `grid-template-areas` to place one large featured dish next to two smaller items. Grid suited both because they need control over rows and columns together.

I used **Flexbox** for one-dimensional components: the header (logo and navigation pushed apart with `justify-content: space-between`), the button groups, the name-and-price row on each menu card, and the opening-hours list. Flexbox suited these because each is a single row whose items need aligning and spacing.

To **support small screens**, a media query at 800px collapses the hero, about, specials and visit grids into one column and redefines the template areas as a single stack. At 520px the navigation is centred, buttons become full width, and the footer stacks. Headings use `clamp()` so they scale with the screen.

**Challenge:** On narrow screens the header links overflowed and caused horizontal scrolling. I fixed this by adding `flex-wrap: wrap` and a `gap` to the header and navigation so the links move onto a new line instead.

## Publishing (GitHub Pages)

1. Create a public repository and push these files to the `main` branch.
2. In the repository go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. Open the published link and check it loads, then submit both links and this note on Google Classroom.
