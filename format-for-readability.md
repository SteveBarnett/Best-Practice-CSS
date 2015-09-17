# Format for readability

Like many kinds of coding, you'll spend more time reading CSS (and thinking about it) than you will writing it. It really helps to be clear in your formatting.

```css
.fish {
  font: bold 1em sans-serif;
  color: white;
  background-color: orange;
}
```

is much easier to read, understand, and debug than

```css
.fish{font:bold 1em sans-serif;color:white;background-color:orange;}
```

It also helps to be consistent in your formatting. Where do you put spaces or new lines? Where do opening and closing brackets go? Tabs, 2 spaces, or 4 spaces for indentation? When working on a team this becomes especially important: if everyone's code has the same formatting you can focus on the content of the code, not the presenation of it.

Tools like [CSS Lint](http://csslint.net/) can also help readability by fixing errors like duplicate or empty rules, or typos in rules.
