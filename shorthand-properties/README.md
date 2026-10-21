<h1>
  <span class="headline">Intro to CSS</span>
  <span class="subhead">Inline and Internal CSS</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to recognize three ways of adding CSS to a web page and explain why external stylesheets are usually preferred.

## Where can we write CSS?

We have already connected a `style.css` file to our HTML document. But did you know we can also write CSS directly inside HTML?

There are three common ways to add CSS to a web page:

1. **Inline CSS** — inside an HTML element.
2. **Internal CSS** — inside the HTML document's `<head>`.
3. **External CSS** — inside a separate `.css` file.

## Inline CSS

**Inline CSS** uses the `style` attribute on an HTML element:

```html
<h1 style="color: purple;">Welcome to our website</h1>
<p style="font-size: 18px;">Our office is in Bahrain.</p>
```

The browser applies each style directly to that element. Notice that we write CSS declarations, such as `color: purple;`, without a selector or curly braces.

However, inline CSS is difficult to maintain. If we want to change ten headings, we may need to edit ten HTML elements individually.

## Internal CSS

**Internal CSS** puts CSS rules inside a `<style>` element in the HTML document's `<head>`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Company Website</title>
    <style>
      h1 {
        color: purple;
      }

      p {
        font-size: 18px;
      }
    </style>
  </head>
  <body>
    <h1>Welcome to our website</h1>
    <p>Our office is in Bahrain.</p>
  </body>
</html>
```

This is easier to manage than inline CSS because one rule can style multiple elements. But the CSS is still stored in the HTML file, making it harder to share the same styles across different pages.

## External CSS: Our recommended approach

For most projects, we write CSS in a separate file, such as `css/style.css`, and connect it to HTML using a `<link>` element inside `<head>`.

**index.html**

```html
<head>
  <link rel="stylesheet" href="./css/style.css">
</head>
```

**css/style.css**

```css
h1 {
  color: purple;
}

p {
  font-size: 18px;
}
```

This helps us keep our **structure** (HTML) separate from our **styling** (CSS). We can also reuse the same stylesheet on several pages.

> 💡 Inline and internal CSS are older techniques that browsers still fully support. They are **not invalid or obsolete**, and they can be useful in certain situations. However, for the projects in this course, we will normally use **external stylesheets** because they are easier to organize and maintain.

## 🎓 You Do

Using the `index.html` and `css/style.css` files from Setup:

1. Add `style="color: teal;"` to the `<h1>` element in `index.html`. Refresh the browser and observe the text color.
2. Remove the inline `style` attribute.
3. Add a `<style>` element inside `<head>` and use it to give the `h1` a `color` of `teal`. Refresh the browser again.
4. Remove the `<style>` element. Add the same `h1` rule to `css/style.css` instead.
5. Refresh the browser and confirm the heading is still teal.

**Check:** Your final solution should style the heading using only the external CSS file.

## How Do Inline, Internal, and External CSS Affect the Cascade?

When more than one CSS rule tries to style the same element, the browser uses the CSS cascade to decide which style wins.

For now, remember these two important rules:

1. Inline CSS usually takes priority over internal and external CSS.
2. Internal and external CSS have the same priority when their selectors have the same specificity. If they conflict, the rule that appears last wins.

### Example

Imagine we have the following external stylesheet:

style.css

```
h1 {
  color: blue;
}
```

We also have internal CSS and inline CSS in our HTML:

index.html

```
<head>
  <link rel="stylesheet" href="style.css">

  <style>
    h1 {
      color: green;
    }
  </style>
</head>

<body>
  <h1 style="color: red;">Hello World!</h1>
</body>
```

What color will our heading be?

The heading is red because its inline style takes priority over the other two rules.

If we remove the inline style, the heading becomes green because the internal CSS appears after the external stylesheet.

> 💡 Remember: The cascade considers more than where CSS is written. Specificity, source order, and `!important` can also affect which styles win. We'll explore these concepts in more detail later.

For most projects, we should continue using external stylesheets because they keep our HTML and CSS organized and easy to maintain.
