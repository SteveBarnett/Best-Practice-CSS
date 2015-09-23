# Make your CSS smaller

There are three ways to make your CSS file sizes smaller.

## Concatenate

The current Front-end performance bottleneck is [latency rather than bandwidth](https://www.igvita.com/2012/07/19/latency-the-new-web-performance-bottleneck/): the time is takes for a single HTTP request is the toughest contraint. This means that **we prefer fewer, larger, files** over many, smaller, ones. You need to maintain a bit of a balance, but one or two CSS files should be enough: combine smaller files together.

To further decrease the file size of your CSS, you can minify it: remove whitespace and line breaks. The whitespace and line breaks are just for humans: browsers don't need them to read and render the CSS correctly.

The biggest saving you'll get is from using `gzip` on the server. It can dramatically reduce file size. Since it's a compression method looks for repeated character sets, it's particularly good for use with CSS and you frequently see files reducing by more than 50%.
