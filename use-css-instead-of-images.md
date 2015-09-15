# Use CSS instead of images

On most sites, images make up a large portion of the page weight: something like 65% of the total number of bytes. There are lots of things you can do to optimise your images (check out [Designing for Performance: Optimising Images](http://designingforperformance.com/optimizing-images/) by [Lara Hogan](https://twitter.com/lara_hogan)), like choosing the right format and compressing the files, but the best solution is to remove as many images as you can.

Lots of graphical flourishes can be replaced with CSS. Geometric shapes are especially easy to do with, and if you use CSS3 with its fancy gradients and drop shadows and rounded corners you can achieve even more. You can also convert images to Data URIs and embed them directly in your stylesheet.

Be wary of performance with the super fancy CSS3 features, and with Data URIs, though: both have been shown to perform less well on lower-spec devices.
