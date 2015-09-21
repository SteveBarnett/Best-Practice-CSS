# Use Media Queries the right way

With the advent of Responsive Web Design, lots of sites are using media queries to adjust their content and layout to better serve users of devices with different screen sizes. Applying your media queries with an additive, [Mobile First](http://www.lukew.com/resources/mobile_first.asp), approach will give you best results, and keep your sites and apps lean and mean.

## Apply base styles

Start by serving a base stylesheet without any media queries. All browsers will get these styles, including those that don't understand media queries (like older version of Internet Explorer, featurephones, and console browsers).

```html
<link rel="stylesheet" href="style.css" />
```

## Apply enhanced styles

Try and use media queries to apply additive changes: each additional set of media query-qualifed CSS rules should add extra styles rather than trying to undo existing styles. If we start Mobile First, we can treat screen size as an enhancement. You can also use "this browser understands media queries" as a rough proxy for "fancier browser".

```html
<link rel="stylesheet" media="(min-width: 30em)" href="enhanced.css" />
```

Note that we use `min-width` rather than `max-width` (because we're thinking Mobile First), and use `em`s instead of `pixels` (because we want to [be fluid](be-fluid.md)).

You can either add further link elements for larger screens, or put more media queries inside your `enhanced.css`. Since [latency trumps bandwidth as a perfomance concern](https://www.igvita.com/2012/07/19/latency-the-new-web-performance-bottleneck/), we prefer fewer, larger, files to many, smaller, ones: putting more media queries in `enhanced.css` is often the way to go.

---

TODO: talk about greedy download and [eCSSential](https://github.com/scottjehl/eCSSential).
TODO: Use content-based breakpoints, not mobile, tablet, desktop
