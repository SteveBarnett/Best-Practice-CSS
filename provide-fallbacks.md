# Provide Fallbacks

Not all browsers are created equal. Support for different CSS features can vary a lot between devices. Thankfully, because CSS is designed to be fault-tolerant, there is a way we can provide a simple version and an enhanced version of each bit of fancy CSS that we want to use.

```css
  .article {
    background-color: rgb(80, 80, 80);
    background-color: rgba(0, 0, 0, 0.7);
  }
```

Every browser applies the first rule. Browsers that understand `rgba` will apply the second rule, overriding the first. Browsers that don't understand the second rule ignore it, and keep the style that comes from the already applied first rule.

[Can I Use](http://caniuse.com/) is an excellent resources for checking support for a particular CSS (or JavaScript) feature. [Modernizr](https://modernizr.com/) is a excellent JavaScript library that provides a set of tests for CSS (and JavaScript) support of features.

TODO: change this to always supply `background-color`? More of a design for failure of CSS them (e.g. animations)?

Karen says:

> cool, some thoughts on this one, a short table summary of which browsers/versions to care about? Maybe which are easy to cater for, which are a pain (I'm sure IE is in there ;)
