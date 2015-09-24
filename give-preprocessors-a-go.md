# Give preprocessors a go

Using a preprocessor can make your life much easier. You can make your CSS [more readable](format-for-readability.md). You can use the preprocessor to lint your CSS, and to do [minification and concatenation](make-your-css-smaller.md) for you.

The particular preprocessor you use isn't too important, but popular ones are [Sass](http://sass-lang.com/), [PostCSS](https://github.com/postcss/postcss), and [Less](http://lesscss.org/).

You don't have to dive in and use all the features at once. In fact, it's better to make one small change at a time. [I built up to using Sass in a couple of steps](http://naga.co.za/2015/03/20/getting-into-sass/).

## Change the file names

First I changed all my existing CSS files to be Sass files and made sure that I could do the processing from Sass to CSS.

## Use variables

Then I stating using variables: making changes to colours, margins, and padding became much easier.

## Use nested selectors

Then I looked at nesting selectors, tidying up some of the longer selector rules. This can be especially useful for [media queries](/Users/steve/Documents/Sites/Best-Practice-CSS/use-media-queries-the-right-way.md). Preprocessors let you write media queries in a way that makes more sense. Here's an example:

The css version:

```css
h1 {
  font-size: 2em;
}

@media (min-width: 30em) {
    h1 {
        font-size: 2.5em;
    }
}

@media (min-width: 60em) {
    h1 {
        font-size: 3em;
    }
}
```

The Sass version:

```sass
h1 {
  font-size: 2em;
  @media (min-width: 30em) {
    font-size: 2.5em;
  }
  @media (min-width: 60em) {
    font-size: 3em;
  }
}
```

It's much shorter, and more readable: you can see all the things that happen to the `h1` over different screen sizes.

## Use partials

Then I started using partials. Regular CSS `@imports` mean another HTTP request for that file (and we've seen that [we prefer to have as few files / requests as we can](/Users/steve/Documents/Sites/Best-Practice-CSS/make-your-css-smaller.md)). Preprocessors do that import before spitting out the final CSS file: that means you can have your CSS in multiple files, logically divided to make sense while developing, but have them complied into one file for the final version.

## Further reading

[Sass for Web Designers by Dan Cederholm](http://abookapart.com/products/sass-for-web-designers) is an excellent introduction to a particular preprocessor, Sass, and will give you a great launching point for further research.
