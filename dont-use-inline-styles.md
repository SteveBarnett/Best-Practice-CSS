# Don't use inline styles

Don't use inline styles in your HTML. They're harder to maintain, harder to debug, and will give you plenty of specificity nightmares when those rules fight against your CSS that lives in other places.

```html
<!-- Don't do this! -->

<p style="color: red;">I hate future me.</p>
```

Don't use a `style` block in the head of your `html` document. Styles there are harder to maintain, harder to debug, and will give you plenty of specificity nightmares when those rules fight against your CSS that lives in other places. (Sound familiar?)

```html
<!-- Also don't do this! -->

<style>
  h1 {
    color: green;
  }
</style>
```

The best way to use CSS is via a link element in the head of your document. This lets you share one CSS document across all your pages. It's easier to maintain and easier to debug

```html
<!-- Do this! -->
<link rel="stylesheet" href="style.css">
```

## Fancy Critical CSS

The exception to this rule is an initial, tiny, bit of CSS that gets put in the head of your document for the first page load, while the rest of your CSS is sneakily loaded asynchronously in the background.

Have a look at [Prioritize Critical CSS](https://developers.google.com/speed/pagespeed/service/PrioritizeCriticalCss) for more information.
