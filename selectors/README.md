<h1>
  <span class="headline">Intro to CSS</span>
  <span class="subhead">Selectors</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to target specific HTML elements with CSS element, id, class, and combinator selectors, to style HTML elements with greater specificity.

## What selectors do

We've already used element selectors like `p` and `h2` to target specific HTML elements on a web page. This allowed us to style those elements in any way we wanted. ID and class selectors let us narrow down the elements we want to select. For example, instead of selecting every `<div>` in our HTML, we can select only the `<div>` elements that have specific `id` or `class` attributes.

## ID selector

ID selectors are the most specific type of selector. They target elements with a specific `id` attribute.

Add the `#` symbol followed by the `id` value to use an `id` selector.

Let's change our `<p>` tag with the `id` of `about`:

```css
#about {
  font-style: italic;
  color: hotpink;
}
```

The ID selector is more specific than the class and element selector. If there are conflicts between a rule using either of those selectors and the ID selector, the ID selector will be used.

> 🚨 An element's ID should always be unique. An element should only ever have a single ID.

## Class selector

We use the class selector to grab one of the values within the `class` attribute. A single element can belong to multiple classes because the `class` attribute accepts multiple space-separated values! The same class can be used for multiple elements; for example, multiple elements have both the `important` and `super-cool` classes in our starter code.

Add a `.` period followed by the class name to use a class selector.

```css
.important {
  color: red;
  font-weight: bold;
}
```

The class selector has a greater specificity than the element selector. If there are conflicts between the rule of an element selector and a class selector, the class selector will be used.  But if there are conflicts between class and id, the id selector will be used.

## ♻️ Creating Reusable CSS Classes

Many websites use classes to create cards to organize information. For example, a website for a training center might use cards to display its available courses.

### 1. Update our HTML

Find the empty `<section>` inside your `<main>` and replace it with:

```
<main>
  <section class="card">
    <h2>Web Development</h2>
    <p>Learn to build websites using HTML and CSS.</p>
    <button>View Course</button>
  </section>

  <figure></figure>
</main>
```

### 2. Style our card

In `style.css`, add:

```
.card {
  background-color: lightblue;
  border: 1px solid gray;
  border-radius: 10px;
  padding: 20px;
  margin: 20px;
}
```

Our card will look something like this:

## Web Development

Learn to build websites using HTML and CSS.

View Course

### 3. Reuse our class

Add another section inside `<main>`:

```
<section class="card">
  <h2>Python Programming</h2>
  <p>Learn to write programs using Python.</p>
  <button>View Course</button>
</section>
```

Both cards share the same styling because they use the `.card` class.

### 🎓 You Do

1. Add a third card for a course of your choice.
2. Change the `.card` background color to `bisque`.
3. Notice how all three cards change.
4. Add a shadow to the `.card` class:

```
box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
```

> 💡 Remember: Classes are reusable! We can apply the same class to multiple HTML elements to keep our website's design consistent.

## Combinators

Combinators provide a powerful way to select elements based on their relationship to other elements.

The most common combinator is the descendant selector, but there are many more.

We use the descendant selector to target elements nested within another element, ***regardless of the depth of the nesting***.

A descendant selector is defined by using a space character between two other selectors:

```css
.card h2 {
    color: maroon;
}
```

Note that this rule does not target `.card` class elements, only `<h2>` elements. The last item in the combinator receives the styling.
